---
layout: default
nav_order: 6
---

# User Guide

### Request Access

User onboarding is a multi-step process:

1. A PI requests access using an online form. Required documentation includes a description of the project data, level of sensitivity, the anticipated scope of computing for the project, and any supplemental information such as IRB approval, etc.

[Request Access](http://example.com/){: .btn .btn-green }

2. The project application will be reviewed and approved/declined.
3. If approved and a PI is from an institution that is new to ACCORD, an MOU/contract between their home institution and UVA will need to be established.
4. The approved project, under institutional contract, can now be fulfilled.
5. The PI will confirm their email and complete final registration steps.
6. When registration is complete the user will be notified by email. Their project will now be created.


### Create a Project

A new project creates the following:

1. System group with the PI as both a member and owner.
2. 1TB project storage share within ACCORD cluster storage.
3. Home directory for the PI within that project storage.

PIs may suspend a project at any time using the console. Project data is stored for ~6 months and then
automatically removed. Suspended projects can be reinstated by request before this time.

[Manage a project](http://example.com/){: .btn .btn-green }


### Add Team Members

Once additional researchers have requested access to ACCORD and have been approved (following the onboarding
steps above), the owner of a project can add those individuals to their project. The PI can add additional 
users at any time, and may also remove users as needed.

Because user authentication is handled through single sign-on from each user's home institution, PIs should
be aware of the `eppn` for their colleagues. An `eppn` looks similar to most institutional email
addresses, in the form of `userid` + `domain`, such as `mst3k@mit.edu` or `abc5y@virginia.edu`.


### Transfer Data

Details on Globus data transfer coming soon


### Create an Environment

From the ACCORD console, select the project you want to work with. Next select an environment from the list of environments. Your container should be running within a few seconds and will appear under "Running Environments" on the same page.

To learn more about your choices of environment, see [Environments](https://accord-documentation.uvarc.io/environments)

### View the status of an environment

Check the "Running Environments" section of the ACCORD console. This will tell you the type of environment,
when you created it, how long it has been running, and how to connect to or terminate it.


### Connect to an Environment

Once you have created an environment, the console will display all of your running environments. Click on 
the "CONNECT" button for the appropriate environment and a new browser tab will open.


### Terminate an environment

Using the "Running Environments" section of the ACCORD console, find the environment you wish to terminate.
On the far right will be a red "Terminate" button. Clicking this will stop and destroy your environment.
Note that your files and storage are never terminated or destroyed in this process. Any special session information
or data read into memory will be lost, however.

Terminated environments cannot be recovered. However, they can be replicated (see below).

### Replicate an environment

To replicate or repeat an environment you used before, scroll down on the ACCORD console to see a list of
environments you have run before. Click the orange "Run" button next to an environment you want to reuse.


## Software Requirements


- A modern web browser such as Chrome, Firefox, Safari, or Edge.
- Install and register OPSWAT, a posture-checking client.



<button onclick="location.href='https://www.opswat.com/'" type="button">Learn more about OPSWAT</button>

- Create and install an authentication certificate.

<button onclick="location.href='https://virginia.service-now.com/its/?id=itsweb_kb_article&sys_id=58aafbcfdbf6c744f032f1f51d961927'" type="button">Create a certificate</button>

