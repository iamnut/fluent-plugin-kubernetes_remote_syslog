# fluent-plugin-kubernetes_remote_syslog

[Fluentd](http://fluentd.org) plugin for output to remote syslog serivce (e.g. [Papertrail](http://papertrailapp.com/))

This repo was forked from https://github.com/dlackty/fluent-plugin-remote_syslog

## Installation

```bash
 fluent-gem install fluent-plugin-kubernetes_remote_syslog
```

## Typical Usage

```
<match foo>
  type kubernetes_remote_syslog
  host example.com
  port 514
  severity debug
  tag fluentd
</match>
```

## TCP Usage
UDP logs are limited to 1024 bytes which can truncate your logs. If you need to log larger entries then switch to TCP logging and increase the packet size.

```
<match foo>
  type kubernetes_remote_syslog
  host example.com
  protocol tcp
  port 514
  severity debug
  tag fluentd
  packet_size 65535
</match>
```

This plugin makes use of [Fluent::Mixin::PlainTextFormatter](https://github.com/tagomoris/fluent-mixin-plaintextformatter) and [Fluent::Mixin::RewriteTagName](https://github.com/y-ken/fluent-mixin-rewrite-tag-name), please check out their documentations for more configuration options.

## License

Copyright (c) 2014-2015 Richard Lee, George Goh. See LICENSE for details.
