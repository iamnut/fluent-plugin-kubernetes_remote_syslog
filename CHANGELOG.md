## 0.3.5

* Switched syslog ruby gen to one that easily supports TCP logging AND larger packet sizes

## 0.3.4

* Switched syslog ruby gen to the one which supports TCP logging

## 0.3.3

* Forked from https://github.com/dlackty/fluent-plugin-remote_syslog to add specific parsing for kubernetes.

## 0.3.2

* Rewrite plugin to make rewrite tag function work properly [#4](https://github.com/dlackty/fluent-plugin-remote_syslog/pull/4)

## 0.3.1

* Fix errors in last release [#3](https://github.com/dlackty/fluent-plugin-remote_syslog/pull/3)

## 0.3.0 (yanked)

* Integrate with `Fluent::Mixin::RewriteTagName` [#2](https://github.com/dlackty/fluent-plugin-remote_syslog/pull/2)

## 0.2.1

* Fix encoding issue

## 0.2.0

* Integrate with `Fluent::Mixin::PlainTextFormatter`
* **BREAKING**: Remove `key_name` config, use `output_data_type` instead

## 0.1.0

* Initial release
