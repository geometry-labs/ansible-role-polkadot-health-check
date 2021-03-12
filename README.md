polkadot-health-check
=========

This role installs and enables a [Gruntwork health check agent](https://github.com/gruntwork-io/health-checker) on a Polkadot node to monitor the health of the RPC endpoint.

Requirements
------------

This role currently expects the Polkadot RPC API to be listening on **port 9933** and will report health status on **port 5500**.

Role Variables
--------------

- skip_health_check: false
    - When this variable is set, the health check agent will always return _200 OK_
    
- phc_api_rpc_port: 9933
    - This variable sets the API RPC port of the Polkadot client to check
    
- phc_health_check_port: 5500
    - This variable sets the port the health check agent will listen on
    
- phc_chain: "kusama"
    - This variable sets allows the role to namespace properly for multiple Polkadot clients running on the same instance

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

Maintained by [Richard Mah](https://github.com/shinyfoil) at [Geometry Labs](https://github.com/geometry-labs)
