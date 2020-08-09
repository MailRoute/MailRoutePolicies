# Server Security Policy

**Last Update Status:** *Updated August 2020*

## Overview

Unsecured and vulnerable servers continue to be a major entry point for
malicious threat actors. Consistent Server installation policies,
ownership and configuration management are all about doing the basics
well.

## Purpose

The purpose of this policy is to establish standards for the base
configuration of internal server equipment that is owned and/or operated
by MailRoute. Effective implementation of this policy will
minimize unauthorized access to MailRoute proprietary information
and technology.

## Scope

All employees, contractors, consultants, temporary and other workers at
Cisco and its subsidiaries must adhere to this policy. This policy
applies to server equipment that is owned, operated, or leased by Cisco
or registered under a Cisco-owned internal network domain.

This policy specifies requirements for equipment on the internal Cisco
network. For secure configuration of equipment external to Cisco on the
DMZ, see the Internet *DMZ Equipment Policy*.

## Policy

1.  General Requirements

    1.  All internal servers deployed at MailRoute must be
        owned by an operational group that is responsible for system
        administration. Approved server configuration guides must be
        established and maintained by each operational group, based
        on business needs and approved by InfoSec. Operational
        groups should monitor configuration compliance and implement
        an exception policy tailored to their environment. Each
        operational group must establish a process for changing the
        configuration guides, which includes review and approval by
        InfoSec. The following items must be met:

        -   Servers must be registered within the corporate enterprise
            management system. At a minimum, the following information is
            required to positively identify the point of contact:
        
            -   Server contact(s) and location, and a backup contact
        
            -   Hardware and Operating System/Version
        
            -   Main functions and applications, if applicable

        -   Information in the corporate enterprise management system must be
            kept up-to-date.

        -   Configuration changes for production servers must follow the
            appropriate change management procedures

        -   For security, compliance, and maintenance purposes, authorized
        personnel may monitor and audit equipment, systems, processes,
        and network traffic per the *Audit Policy*.

    1.  Configuration Requirements

        1.  Operating System configuration should be in accordance with
            approved InfoSec guidelines.

        1.  Services and applications that will not be used must be
            disabled where practical.

        1.  Access to services should be logged and/or protected through
            access-control methods such as a web application firewall,
            if possible.

        1.  The most recent security patches must be installed on the
            system as soon as practical, the only exception being when
            immediate application would interfere with business
            requirements.

        1.  Trust relationships between systems are a security risk, and
            their use should be avoided. Do not use a trust relationship
            when some other method of communication is sufficient.

        1.  Always use standard security principles of least required
            access to perform a function. Do not use root when a
            non-privileged account will do.

        1.  If a methodology for secure channel connection is available
            (i.e., technically feasible), privileged access must be
            performed over secure channels, (e.g., encrypted network
            connections using SSH or IPSec).

        1.  Servers should be physically located in an access-controlled
            environment.

        1.  Servers are specifically prohibited from operating from
            uncontrolled cubicle areas.

    1.  Monitoring

        1.  All security-related events on critical or sensitive systems
            must be logged and audit trails saved as follows:

            -   All security related logs will be kept online for a minimum of 1
                week.
            
            -   Daily incremental tape backups will be retained for at least 1
                month.
            
            -   Weekly full tape backups of logs will be retained for at least 1
                month.
            
            -   Monthly full backups will be retained for a minimum of 2 years.
            
        1. Security-related events will be reported to InfoSec, who will
        review logs and report incidents to IT management. Corrective
        measures will be prescribed as needed. Security-related events
        include, but are not limited to:

            -   Port-scan attacks
            
            -   Evidence of unauthorized access to privileged accounts
            
            -   Anomalous occurrences that are not related to specific applications
                on the host.

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

-   Audit Policy

-   DMZ Equipment Policy

## Definitions and Terms

The following definition and terms can be found in the SANS Glossary
located at:

https://www.sans.org/security-resources/glossary-of-terms/

-   De-militarized zone (DMZ)

## Revision History

August 2020 - Initial MailRoute Documentation