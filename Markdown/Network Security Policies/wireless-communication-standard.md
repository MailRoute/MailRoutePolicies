# Wireless Communication Standard

**Last Update Status:** *Updated August 2020*

# Overview

See Purpose.

## Purpose

This standard specifies the technical requirements that wireless
infrastructure devices must satisfy to connect to a MailRoute
network. Only those wireless infrastructure devices that meet the
requirements specified in this standard or are granted an exception by
the InfoSec Team are approved for connectivity to a MailRoute
network.

#### Network devices including, but not limited to, hubs, routers, switches, firewalls, remote access devices, modems, or wireless access points, must be installed, supported, and maintained by an Information Security (Infosec) approved support organization. Lab network devices must comply with the Lab Security Policy.

## Scope

All employees, contractors, consultants, temporary and other workers at
MailRoute and its subsidiaries, including all personnel that
maintain a wireless infrastructure device on behalf of MailRoute,
must comply with this standard. This standard applies to wireless
devices that make a connection the network and all wireless
infrastructure devices that provide wireless connectivity to the
network.

Infosec must approve exceptions to this standard in advance.

## Standard

1.  General Requirements

    All wireless infrastructure devices that connect to a MailRoute
network or provide access to MailRoute Confidential, MailRoute
Highly Confidential, or MailRoute Restricted information
must:

    -  Use Extensible Authentication Protocol-Fast Authentication via Secure Tunneling (EAP-FAST), Protected Extensible Authentication Protocol (PEAP), or Extensible Authentication Protocol-Translation Layer Security (EAP-TLS) as the authentication protocol.

    -  Use Temporal Key Integrity Protocol (TKIP) or Advanced Encryption System (AES) protocols with a minimum key length of 128 bits.

    -  All Bluetooth devices must use Secure Simple Pairing with encryption enabled.

1.  Lab and Isolated Wireless Device Requirements

    -   Lab device Service Set Identifier (SSID) must be different from MailRoute production device SSID.

    -   Broadcast of lab device SSID must be disabled.

1. Home Wireless Device Requirements

    All home wireless infrastructure devices that provide direct access to a
MailRoute network, such as those behind Enterprise Teleworker
(ECT) or hardware VPN, must adhere to the following:

    -   Enable WiFi Protected Access Pre-shared Key (WPA-PSK), EAP-FAST, PEAP, or EAP-TLS
    
    -   When enabling WPA-PSK, configure a complex shared secret key (at least 20 characters) on the wireless client and the wireless access point
    
    -   Disable broadcast of SSID
    
    -   Change the default SSID name
    
    -   Change the default login and password

## Policy Compliance

### Compliance Measurement

The Infosec team will verify compliance to this policy through various
methods, including but not limited to, periodic walk-thrus, video
monitoring, business tool reports, internal and external audits, and
feedback to the policy owner.

# Exceptions

Any exception to the policy must be approved by the Infosec Team in
advance.

# Non-Compliance

An employee found to have violated this policy may be subject to
disciplinary action, up to and including termination of employment.

# Related Standards, Policies and Processes

-   Lab Security Policy

# Definitions and Terms

The following definition and terms can be found in the SANS Glossary
located at:

https://www.sans.org/security-resources/glossary-of-terms/

-   AES

-   EAP-FAST

-   EAP-TLS

-   PEAP

-   SSID

-   TKIP

-   WPA-PSK

# Revision History

August 2020 - Initial MailRoute Documentation