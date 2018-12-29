---
title: How does DNS work?
subtitle: A primer for software developers who want to know more.
layout: post
categories: ["How Things Work"]
comments: true
---

Whether you realize it or not, DNS is a workhorse of the internet ecosystem. It provides the glue that allows someone like your grandma, (who knows that you want a pair of Adidas Ultraboost from footlocker.com for Christmas) to talk TCP with a server on the other side of the world.

It's amazing when you think about it...

Your grandma really is quite kind.

So, let's start from first principles and dig in to understand DNS a bit more.

## What exactly is DNS?

> DNS, or the *Domain Name System* is an abstraction layer that maps the human-readable web addresses that we know and love to IP addresses.

For a long time, that was about the extent of my knowledge of DNS. I knew that there were servers out in the ether of the internet that contained those mappings.  Later on, I learned that one could use `nslookup` to find existing mappings. Beyond that, I knew very little. The majority of the time this was enough, but every now and then I would hear someone mention an `A` record or a `CNAME` record and I couldn't contribute much to the conversation other than "Ah yes, that has something to do with DNS".  If you are like me, the things that you know that you don't know serve as bread crumbs for the things that you want to learn.  Let's follow those breadcrumbs a bit.

## The lifecycle of a DNS query

Interview questions like "Tell me everything that happens when I navigate to google.com" are quite fun to answer for me.  This is mainly because there are endless ways to tell the story of all the things that go on when a user does x.  At some point though, we have to limit the detail of our explanations in order to actually provide value. Be forewarned: the explanatory lifecycle of a DNS query below is not exhaustive! Exhaustive references can be useful but not so much in didactic contexts.

So what happens when a domain name query is issued to DNS?

1. Someone named Jeffrey asks their computer to go to google.com
2. The operating system of Jeffrey's computer consults its own cache to see if the IP address for the requested name is already known. If it is, life is good! If not...
3. Jeffrey's operating system reaches out to a DNS cacher/recursor which we will refer to as the *local DNS server* from here onward. The local DNS server is very often provided by your ISP, but sufficiently advanced LANs will often have their own local DNS server.
4. The *local DNS server* will check its cache. If it has an answer to the query, life is good! If not...
5. The local DNS server will recursively contact other DNS servers until it can provide an authoritative answer.  The recursive DNS request looks something like:
	* Local DNS server asks a root DNS server where to find the .com TLD (top level domain) server. The root DNS server provides the answer.
    * Local DNS server then asks the .com TLD DNS server for the "google" name server. The .com TLD DNS server provides the answer.
    * Local DNS server asks the "google" DNS server for the google.com IP. The "google" name server provides an answer.
6. The local DNS server returns the IP address provided by the "google" name server to Jeffrey's computer. (and hopefully caches the answer!)

## What is a DNS record?

The response provided by a DNS server represents a *record* that exists in the Domain Name System. One might find that the responses representing records are referred to as a *record* themselves. YMMV.

Below I explain a few of the common DNS record types. There are many more. For more details you may want to consult this [helpful and complete list](https://en.wikipedia.org/wiki/List_of_DNS_record_types) of DNS record types.

### `CNAME` Records

A `CNAME` record is said to be "the canonical name for an alias" in [RFC 1035](https://tools.ietf.org/html/rfc1035).  `CNAME` records map an alias to another name. Upon receiving a `CNAME` response, the  computer issuing a DNS query will restart the query using the value that the `CNAME` record points too. Note: While DNS is actually resolving the IP of the canonical name, the original name request (the alias) is what users will see in their browser.

`CNAME` records are intended to point to a canonical name, but there is nothing that prevents one from creating a CNAME record that point to another alias. One could even create an infinite loop if they so desired.

### `DNAME` Records

A `DNAME` record "provides redirection for a subtree of the domain" accord to its RFC ([RFC 6672](https://tools.ietf.org/html/rfc6672)). For this reason is it known as a *delegation* record.

### `A`  Records

`A` records are described as providing "a host address" in [RFC 1035](https://tools.ietf.org/html/rfc1035). `A` records are the meat and potatoes(?) of DNS. The provide a simple mapping from a name to an IP address.

---

Did I get something wrong? Is there another subset of DNS functionality that needs to be explained? Let me know in the comments.
