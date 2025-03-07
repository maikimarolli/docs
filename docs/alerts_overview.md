---
title: Overview
description: Alerts - Overview
---

import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
import useBaseUrl from '@docusaurus/useBaseUrl';

## About

With Alerts you can be notified when something happens or changes instead of needing to repeatedly query for changes. 
Leaf Alerts support events that happen within Leaf and events that happen within supported 3rd party software. 

Webhooks are user-defined HTTP callbacks. You send us a server URL (the address of
the callback) specifying what things you want to know about so when they do happen,
we tell you on that URL, by means of a HTTP request.

Those things are called "events", for example: "there's a new satellite image",
"the processing of an operations file finished", or "these credentials expired".

The following image shows how events are sent to your webhook. On the left, its
the representation of a webhook registration. On the right, a satellite image
is processed at any time, then the webhooks system sends a POST request to the
registered webhook.

<img alt="Field example" src={useBaseUrl('img/alerts_flow.png')} />

Check the "Overview" page of a specific service, section "Events", to know what
events from that service are available to webhooks.

See the [Alerts API Reference][alerts_endpoints] for information on how to
register, get and delete webhooks.

To understand how to verify if an incoming request comes from Leaf, see the [Authentication section][alerts_auth].


[alerts_endpoints]: alerts_endpoints.md
[alerts_auth]: alerts_authentication.md
