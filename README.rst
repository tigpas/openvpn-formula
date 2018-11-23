=======
openvpn
=======

Formula to install and configure openvpn server and client.

.. note::

    See the full `Salt Formulas installation and usage instructions
    <http://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html>`_.

Available states
================

.. contents::
    :local:

``openvpn``
--------

Installs OpenVPN.

``openvpn.config``
--------

Configures OpenVPN client and server. Multiple clients and servers are possible.

``openvpn.gui``
--------

Configures OpenVPN GUI (Windows only). Sets global registry settings as described `here <https://github.com/OpenVPN/openvpn-gui/#registry-values-affecting-the-openvpn-gui-operation>`_.

``openvpn.adapters``
--------

Manages TAP-Windows device adapters (Windows only). Ensures that any devices specified with ``dev_node`` in pillar exist.

``openvpn.ifconfig_pool_persist``
---------------------------------

Installs and configures an ifconfig_pool_persist file. Used to assign host IPs.

``openvpn.network_manager_networks``
------------------------------------

Don't setup a OpenVPN client service, but add ready-to-use NetworkManager configurations.

Example
=======

See *openvpn/pillar.example*.

Notes
=====

This formula does can optionally deploy certificates and keys, but does not generate them. This must be done manually or with another formula.
