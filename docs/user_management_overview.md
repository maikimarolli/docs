---
title: Overview
description: Usermanagement - Overview
---

For Leaf to be able to access, standardize, process and return files, you just
have to create a Leaf User and connect them to a data provider.

Connecting a Leaf User to a data provider means that you will be attaching the user
token to the Leaf User so that Leaf can access their data on a given provider.
To get said token, we will need to go through the data provider's authentication
flow, which varies by data provider.

To make things easy, we have created a section for the data providers
authentication flow. After the end this section, the goal
is to have the user's token, so you can attach to the Leaf User and Leaf can
return clean, aggregated, and standardized data in a simple JSON response.

The same Leaf User can be attached to as many providers as they have accounts in.

A simple use-case: typically, a Leaf User is a grower. So let's say your
application wants to use Leaf to access the grower data in a standardized way.
Your application, the grower and Leaf will go through the provider authentication
flow so the grower can grant rights to access their data.

This authentication flow has to be done only once, since Leaf will manage the
tokens and refresh them when needed.

<!-- Another use-case would be an agronomist that has access to more than one grower's -->

So, choose the provider's you want to connect your users to and let's see how
each these providers authentication flow is.

After that, you can create a Leaf User, attach the tokens and start querying for
standardized data in a simple JSON response.


## Integrate with John Deere

We made this very easy on one of our blog posts.

Check our blog post on [John Deere authentication with Leaf][jd]
[jd]: https://blog.withleaf.io/en/john-deere-authentication-with-leaf


## Integrate with Climate Field View

We made this very easy on one of our blog posts.

Check our blog Post on [Climate Field View authentication with Leaf][cfv]
[cfv]: https://blog.withleaf.io/en/climate-fieldview-authentication-with-leaf

## Integrate with AgLeader 

We made this very easy on one of our blog posts.

Check our blog Post on [AgLeader Authentication with Leaf][agleader]
[agleader]: https://blog.withleaf.io/en/agleader-authentication-with-leaf

## Integrate with CNHi

We made this very easy on one of our blog posts.

Check our blog Post on [CNHi authentication with Leaf][cnhi]
[cnhi]: https://blog.withleaf.io/en/cnhi-authentication-with-leaf
