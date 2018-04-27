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
