---
layout: default
#parent: Child of Test
#grand_parent: Test
nav_order: 5
---

# Security

ACCORD can meet HIPAA, FERPA, and other less-restrictive data sensitivity requirements. 
More restrictive levels, such as CUI, FISMA, PCI cannot be satisfied. A list of compliance
will be released as the platform nears production launch.

## Authentication

ACCORD makes use of InCommon authentication, a federated SAML-based standard used by most institutions of 
higher education in the U.S. This means that ACCORD does not have its own user identity store but instead 
relies upon authentication via your home institution's single sign-on tool.


## Authorization

ACCORD manages user access and permissioning non-hierarchically. All members of a project have equal access
to the data storage for that project, without any privileged superuser or root. Access Management is controlled
by normal POSIX groups defined by COmanage, a collaborative IAM tool from the National Science Foundation.


## Closed Environemnts

ACCORD environments have no outbound connectivity to the Internet other than whitelisted library and tool 
repositories (PyPi, CPAN, CRAN). Connections to tools such as GitHub and external APIs are disallowed.

We are considering implementing a local source control tool in the future.


## Encryption

All connectivity to ACCORD environments is encrypted using SSL over HTTPS. 
Plain-text (unencrypted) access is prohibited. 

Data transfers in/out via the Globus DTN meet FIPS 140-2 compliance.


## Isolation

ACCORD environments cannot, by design, have any access to other environments -- including storage, 
network connectivity, or data. Environments run within isolated Kubernetes pods and their (overlay)
network connectivity is isolated and encrypted. The cluster control plane is also encrypted for management
and requests.


## Private Environment URLs

**[TO-DO]** When you request an ACCORD environment, a unique HTTPS endpoint is created for you and 
*can only be used by you*. That URL will look something like:

    https://jupyter-notebook-1a2b3c4d5e-mst3k.uvarc.io/

These environments cannot be shared.

Using certificate authentication from your browser (something you will set up the first time you use 
ACCORD and will renew annually), the platform verifies that you, and only you, access that environment. 
If you want to collaborate with a co-investigator, they can simply create an identical environment 
within the same project!

## Client Posture-Checks

<img align=right" alt="MetaAccess by OPSWAT" src="/assets/img/opswat.png" style="float:right;" />

Access to ACCORD is restricted to computers (laptops, desktop workstations, etc.) that are sufficiently
updated and meet minimum security requirements. To verify the posture of user workstations, ACCORD uses
the MetaAccess client, a small piece of software that users install on their local computers. MetaAccess reports
its status to the OPSWAT API, which ACCORD can check with each user login.

More information about MetaAccess will be posted as it becomes available.
