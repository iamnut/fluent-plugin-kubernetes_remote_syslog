# fluent-plugin-kubernetes_remote_syslog

[Fluentd](http://fluentd.org) plugin for output to remote syslog serivce (e.g. [Papertrail](http://papertrailapp.com/))

This repo was forked from https://github.com/dlackty/fluent-plugin-remote_syslog

## Installation

```bash
 fluent-gem install fluent-plugin-kubernetes_remote_syslog
```

## Usage

```
<match foo>
  type remote_syslog
  host example.com
  protocol udp
  port 514
  severity debug
  tag fluentd
</match>
```

This plugin makes use of [Fluent::Mixin::PlainTextFormatter](https://github.com/tagomoris/fluent-mixin-plaintextformatter) and [Fluent::Mixin::RewriteTagName](https://github.com/y-ken/fluent-mixin-rewrite-tag-name), please check out their documentations for more configuration options.

## License

Copyright (c) 2014-2015 Richard Lee, George Goh. See LICENSE for details.
