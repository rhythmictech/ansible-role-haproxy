
v0.1.1
---------------------------
Syntax fixes.

v0.1.0
---------------------------
Added a veryhigh tls level
Updated medium cipher lists to remove weak ciphers
Refactored all cipher lists to use a more modern, dynamic string per https://medium.com/@davetempleton/tls-configuration-cipher-suites-and-protocols-a01ee7005778
Added support for two vars to override the cipher list or tls protocols regardless of the tls level
  - haproxy_ciphers
  - haproxy_ssllist
Update rsyslog configuration file to remove the stop verb in favor of the ~ action for wider compatibility

v0.0.11
---------------------------
Made the medium cipher set more strict than the low cipher set. Previously, they were
the same.

v0.0.10
---------------------------
Add rsyslog support. Because rsyslog does not listen on UDP By default, at the moment this will set the listener
and then redirect logs to /var/log/haproxy. In the future, we may want to make the listener be optional.

v0.0.9
---------------------------
Reconfigure SSL settings to use one of low,med,high, defaulting to low.
This release removed the following vars:
  - haproxy_enable_strict_tls
  - haproxy_enable_reallystrict_tls
This release added the following var:
  - haproxy_tls_level

v0.0.8
---------------------------
Added more stringent SSL settings

v0.0.7
---------------------------
Fixed ACL enforcement issue

v0.0.6
---------------------------
Fixed "check" command when cookie validation isn't enabled

v0.0.5
---------------------------
Added support for back-end mode

v0.0.3
---------------------------
Added support for generic frontend block rules defined as a list

v0.0.2
---------------------------
Substantial changes to add additional capabilities from other projects. May not be compatible with previous version.

v0.0.1
---------------------------
Initial Commit - working version
