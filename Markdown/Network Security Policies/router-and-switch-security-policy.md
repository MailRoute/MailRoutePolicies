# Router and Switch Security Policy

**Last Update Status:** *Updated August 2020*

## Overview

See Purpose.

## Purpose

This document describes a required minimal security configuration for
all routers and switches connecting to a production network or used in a
production capacity at or on behalf of MailRoute.

## Scope

All employees, contractors, consultants, temporary and other workers at
MailRoute and its subsidiaries must adhere to this policy. All
routers and switches connected to MailRoute production networks
are affected.

## Policy

Every router must meet the following configuration standards:

1.  No local user accounts are configured on the router. Routers and
    switches must use TACACS+ for all user authentication.

1.  The enable password on the router or switch must be kept in a secure
    encrypted form. The router or switch must have the enable password
    set to the current production router/switch password from the
    device's support organization.

1.  The following services or features must be disabled:

    -  IP directed broadcasts

    -  Incoming packets at the router/switch sourced with invalid
        addresses such as RFC1918 addresses

    -  TCP small services

    -  UDP small services

    -  All source routing and switching

    -  All web services running on router

    -  MailRoute discovery protocol on Internet connected
        interfaces

    -  Telnet, FTP, and HTTP services

    -  Auto-configuration

1.  The following services should be disabled unless a business
    justification is provided:

    -  MailRoute discovery protocol and other discovery
        protocols

    -  Dynamic trunking

    -  Scripting environments, such as the TCL shell

1.  The following services must be configured:

    -  Password-encryption

    -  NTP configured to a corporate standard source

1.  All routing updates shall be done using secure routing updates.

1.  Use corporate standardized SNMP community strings. Default strings,
    such as public or private must be removed. SNMP must be configured
    to use the most secure version of the protocol allowed for by the
    combination of the device and management systems.

1.  Access control lists must be used to limit the source and type of
    traffic that can terminate on the device itself.

1.  Access control lists for transiting the device are to be added as
    business needs arise.

1. The router must be included in the corporate enterprise management
    system with a designated point of contact.

1. Each router must have the following statement, or something substantially similar
   presented for all forms of login whether remote or local:

    > *\"UNAUTHORIZED ACCESS TO THIS NETWORK DEVICE IS PROHIBITED. You must
    > have explicit permission to access or configure this device. All
    > activities performed on this device may be logged, and violations of
    > this policy may result in disciplinary action, and may be reported to
    > law enforcement. There is no right to privacy on this device. Use of
    > this system shall constitute consent to monitoring.\"*

1. Telnet may never be used across any network to manage a router,
    unless there is a secure tunnel protecting the entire communication
    path. SSH version 2 is the preferred management protocol.

1. Dynamic routing protocols must use authentication in routing updates
    sent to neighbors. Password hashing for the authentication string
    must be enabled when supported.

1. The corporate router configuration standard will define the category
    of sensitive routing and switching devices, and require additional
    services or configuration on sensitive devices including:

    -  IP access list accounting

    -  Device logging

    -  Incoming packets at the router sourced with invalid addresses,
       such as RFC1918 addresses, or those that could be used to spoof
       network traffic shall be dropped

    -  Router console and modem access must be restricted by additional
       security controls

## Policy Compliance

### Compliance Measurement

The Infosec team will verify compliance to this policy through various
methods, including but not limited to, periodic walk-thrus, video
monitoring, business tool reports, internal and external audits, and
feedback to the policy owner.

## Exceptions

Any exception to the policy must be approved by the Infosec team in
advance.

## Non-Compliance

An employee found to have violated this policy may be subject to
disciplinary action, up to and including termination of employment.

## Related Standards, Policies and Processes

None.

## Definitions and Terms

None.

## Revision History

August 2020 - Initial MailRoute Documentation