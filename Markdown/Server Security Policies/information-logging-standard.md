# Information Logging Standard

**Last Update Status:** *Updated August 2020*

## Overview

Logging from critical systems, applications and services can provide key
information and potential indicators of compromise. Although logging
information may not be viewed on a daily basis, it is critical to have
from a forensics standpoint.

## Purpose

The purpose of this document attempts to address this issue by
identifying specific requirements that information systems must meet in
order to generate appropriate audit logs and integrate with an
enterprise's log management function.

The intention is that this language can easily be adapted for use in
enterprise IT security policies and standards, and also in enterprise
procurement standards and RFP templates. In this way, organizations can
ensure that new IT systems, whether developed in-house or procured,
support necessary audit logging and log management functions.

## Scope

This policy applies to all production systems on MailRoute
Network.

# Standard

1. General Requirements

    All systems that handle confidential information, accept network
connections, or make access control (authentication and authorization)
decisions shall record and retain audit-logging information sufficient
to answer the following questions:

    -  What activity was performed?

    -  Who or what performed the activity, including where or on what
       system the activity was performed from (subject)?

    -  What the activity was performed on (object)?

    -  When was the activity performed?

    -  What tool(s) was the activity was performed with?

    -  What was the status (such as success vs. failure), outcome, or
       result of the activity? 

1. Activities to be Logged

    Therefore, logs shall be created whenever any of the following
activities are requested to be performed by the system:

    1.  Create, read, update, or delete confidential information, including
    confidential authentication information such as passwords;

    1.  Create, update, or delete information not covered in \#1;

    1.  Initiate a network connection;

    1.  Accept a network connection;

    1.  User authentication and authorization for activities covered in \#1
    or \#2 such as user login and logout;

    1.  Grant, modify, or revoke access rights, including adding a new user
    or group, changing user privilege levels, changing file permissions,
    changing database object permissions, changing firewall rules, and
    user password changes;

    1.  System, network, or services configuration changes, including
    installation of software patches and updates, or other installed
    software changes;

    1.  Application process startup, shutdown, or restart;

    1.  Application process abort, failure, or abnormal end, especially due
    to resource exhaustion or reaching a resource limit or threshold
    (such as for CPU, memory, network connections, network bandwidth,
    disk space, or other resources), the failure of network services
    such as DHCP or DNS, or hardware fault; and

    1. Detection of suspicious/malicious activity such as from an Intrusion
    Detection or Prevention System (IDS/IPS), anti-virus system, or
    anti-spyware system.

1. Elements of the Log

    Such logs shall identify or contain at least the following elements,
directly or indirectly. In this context, the term "indirectly" means
unambiguously inferred.

    1.  Type of action -- examples include authorize, create, read, update,
        delete, and accept network connection.
    
    1.  Subsystem performing the action -- examples include process or
        transaction name, process or transaction identifier.
    
    1.  Identifiers (as many as available) for the subject requesting the
        action -- examples include user name, computer name, IP address, and
        MAC address. Note that such identifiers should be standardized in
        order to facilitate log correlation.
    
    1.  Identifiers (as many as available) for the object the action was
        performed on -- examples include file names accessed, unique
        identifiers of records accessed in a database, query parameters used
        to determine records accessed in a database, computer name, IP
        address, and MAC address. Note that such identifiers should be
        standardized in order to facilitate log correlation.
    
    1.  Before and after values when action involves updating a data
        element, if feasible.
    
    1.  Date and time the action was performed, including relevant time-zone
        information if not in Coordinated Universal Time.
    
    1.  Whether the action was allowed or denied by access-control
        mechanisms.
    
    1.  Description and/or reason-codes of why the action was denied by the
        access-control mechanism, if applicable.

1. Formatting and Storage

    The system shall support the formatting and storage of audit logs in
such a way as to ensure the integrity of the logs and to support
enterprise-level analysis and reporting. Note that the construction of
an actual enterprise-level log management mechanism is outside the scope
of this document. Mechanisms known to support these goals include but
are not limited to the following:

    1.  Microsoft Windows Event Logs collected by a centralized log
        management system;
    
    1.  Logs in a well-documented format sent via *syslog*, *syslog-ng*, or
        *syslog-reliable* network protocols to a centralized log management
        system;
    
    1.  Logs stored in an ANSI-SQL database that itself generates audit logs
        in compliance with the requirements of this document; and
    
    1.  Other open logging mechanisms supporting the above requirements
        including those based on CheckPoint OpSec, ArcSight CEF, and IDMEF.

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

> None.

## Definitions and Terms

> None.

## Revision History

August 2020 - Initial MailRoute Documentation