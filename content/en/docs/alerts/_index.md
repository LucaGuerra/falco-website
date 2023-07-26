---
title: Falco Alerts
description: Integrate Falco and send Falco Alerts in your desired platform
linktitle: Falco Alerts
weight: 40
---

Falco can send alerts to one or more channels:

* Standard Output
* A file
* Syslog
* A spawned program
* A HTTP/HTTPS endpoint
* A client via the gRPC API

The channels are configured via the falco configuration file `falco.yaml`. See the [Falco Configuration](/docs/reference/daemon/config-options/) page for more details.

Find further information about how to configure each of those channels under [Alert Channels](/docs/alerts/channels/).

## Integration with third parties

Falco alerts can easily be forwarded to third-party systems like off-host SIEM, databases, or Faas. While many tools can natively connect to the generic alert channels that Falco provides such as files and standrd output, a forwarder proxy, [Falcosidekick](/docs/alerts/forwarding), was created to facilitate integration with more than 50 different systems.
