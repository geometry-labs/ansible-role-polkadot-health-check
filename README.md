polkadot-health-check
=========

This role installs and enables a [Gruntwork health check agent](https://github.com/gruntwork-io/health-checker) on a Polkadot node to monitor the health of the RPC endpoint.

Requirements
------------

This role currently expects the Polkadot RPC API to be listening on **port 9933** and will report health status on **port 5500**.

Role Variables
--------------

This role does not currently contain any settable variables. 

Dependencies
------------

This role does not currently contain any dependencies.

Example Playbook
----------------

    - hosts: polkadot-nodes
      roles:
         - { role: insight_infra.polkadot_health_check }

License
-------

Apache 2.0

Author Information
------------------

Maintained by [Richard Mah](https://github.com/shinyfoil) for [Insight Infrastructure](https://github.com/insight-infrastructure)
