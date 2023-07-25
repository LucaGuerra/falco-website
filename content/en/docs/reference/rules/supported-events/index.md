---
title: Supported Events
linktitle: Supported Events
description: Find out which events Falco supports
aliases: ["/docs/rules/supported-events"]
weight: 40
---

Here are the system call event types and args supported by the [kernel module and BPF probe](/docs/event-sources/drivers) via `libscap` included in the Falco libs. Note that, for performance reasons, by default Falco will only consider a subset of them indicated in the table below with "yes". However, it's possible to make Falco consider all events by using the `-A` command line switch.

Note that several event types exist:
* [Syscall events](#syscall-events) correspond to Linux system calls. Most of them have parameters, documented below, while some are detected as generic and they only offer the syscall ID.
* [Tracepoint events](#tracepoint-events) represent internal kernel events that may be significant but don't directly translate to any syscall.
* [Metaevents](#metaevents) are internal Falco events. They are generally not available for rules.
* [Plugin events](#plugin-events) are internal Falco events. They act as an envelope for actual plugin event data and are not available to rules. In order to write rules that use plugins use the fields documented in the individual plugin.

<!--
generated with:
falco --list-syscall-events --markdown
-->

{{< markdown_inline
    contentPath="/docs/reference/rules/supported-events/supported-events.md"
>}}
