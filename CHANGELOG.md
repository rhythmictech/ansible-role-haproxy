# Changelog

## v1.0.0

Modernize for current platforms and haproxy versions:

- Drop CentOS 6 and 7 support
- Add Amazon Linux 2023, AlmaLinux 9 and 10 support
- Support haproxy 2.8 (alma9) and 3.0 (al2023, alma10)
- Update Ansible syntax to 2.10+ (FQCN, dnf module, loop)
- Add TLSv1.3 ciphersuite support
- Replace deprecated reqadd with http_request_rules
- Replace external haproxy_exporter with native Prometheus exporter (`haproxy_prometheus_enabled`, `haproxy_prometheus_port`)

## v0.5.0

Support haproxy_exporter for Prometheus

## v0.4.0

- Move Graylog logging to UDP
- Correct issues with Graylog logging

## v0.3.0

Support custom server options for backends

## v0.2.0

- Fixes for haproxy RPM
- Support Graylog exports via syslog

## v0.1.3

Support https redirect on frontends

## v0.1.2

Remove deprecation warnings

## v0.1.1

Syntax fixes.

## v0.1.0

- Added a veryhigh tls level
- Updated medium cipher lists to remove weak ciphers
- Refactored all cipher lists to use a more modern, dynamic string
- Added support for two vars to override the cipher list or tls protocols regardless of the tls level
  - haproxy_ciphers
  - haproxy_ssllist
- Update rsyslog configuration file to remove the stop verb in favor of the ~ action for wider compatibility

## v0.0.11

Made the medium cipher set more strict than the low cipher set. Previously, they were
the same.

## v0.0.10

Add rsyslog support. Because rsyslog does not listen on UDP by default, at the moment this will set the listener
and then redirect logs to /var/log/haproxy. In the future, we may want to make the listener be optional.

## v0.0.9

Reconfigure SSL settings to use one of low,med,high, defaulting to low.

Removed vars:
- haproxy_enable_strict_tls
- haproxy_enable_reallystrict_tls

Added vars:
- haproxy_tls_level

## v0.0.8

Added more stringent SSL settings

## v0.0.7

Fixed ACL enforcement issue

## v0.0.6

Fixed "check" command when cookie validation isn't enabled

## v0.0.5

Added support for back-end mode

## v0.0.3

Added support for generic frontend block rules defined as a list

## v0.0.2

Substantial changes to add additional capabilities from other projects. May not be compatible with previous version.

## v0.0.1

Initial Commit - working version
