Ansible Role for HAProxy
========================

Ansible Role for HAProxy.

Requirements
------------

This role requires Ansible 2.10 or higher.

This role supports:
- Amazon Linux 2023 (haproxy 3.0)
- AlmaLinux 9 (haproxy 2.8)
- AlmaLinux 10 (haproxy 3.0)

Role Variables
--------------

See `defaults/main.yml` for available variables.

Breaking Changes
----------------

### v1.0.0

- Dropped CentOS 6 and 7 support
- Replaced `yum` module with `ansible.builtin.dnf`
- The `reqadd` frontend option has been removed (deprecated in haproxy 2.1+). Use `http_request_rules` instead:

  Before:
  ```yaml
  haproxy_frontends:
    - name: web
      reqadd:
        - "X-Forwarded-Proto:\\ https"
  ```

  After:
  ```yaml
  haproxy_frontends:
    - name: web
      http_request_rules:
        - "add-header X-Forwarded-Proto https"
  ```

- TLS configuration now includes TLSv1.3 ciphersuites (`ssl-default-bind-ciphersuites`)
- TLS options use `ssl-min-ver` syntax instead of `no-tlsv1x` flags
- Replaced external haproxy_exporter with native Prometheus exporter (`haproxy_prometheus_enabled`, `haproxy_prometheus_port`)
