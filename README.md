# McAfee-NSM-Phantom
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

This integration is focusing on the threat intelligence sharing with McAfee NSM and the orchestrations platform Phantom. 
This App provides the capability to publish Threat Information from Phantom to McAfee NSM. 
This App supports the following actions:

1. **test connectivity** - Validate the asset configuration for connectivity using supplied configuration
2. **block ip** - Block an IP
3. **unblock ip** - Unblock an IP

## Component Description

**Phantom** is a community powered security automation and orchestration platform. https://www.phantom.us/
**McAfee NSM** gives visibility and control over all McAfee IPS sensors deployed across the enterprise network. https://www.mcafee.com/us/products/network-security-platform.aspx 

## Prerequisites

Phantom Platform tested with version 3.0.251
McAfee NSM 9.1.x (will also work with older NSM versions)

## Configuration
Download the Latest release, open the Phantom Platform and and go to Apps. Under Apps click install app and upload the tgz file. 

<img width="1331" alt="screen shot 2017-12-08 at 10 53 01" src="https://user-images.githubusercontent.com/25227268/33760476-035f5b4e-dc06-11e7-971f-5822967b82c1.png">

Configure a new asset and provide an asset name. In the asset settings define the NSM IP address or hostname, username, password and sensor ID.

<img width="707" alt="screen shot 2017-12-08 at 10 55 01" src="https://user-images.githubusercontent.com/25227268/33760547-434d330c-dc06-11e7-932f-35911cf41813.png">

Click test connectivity. This action will try to connect to the McAfee NSM.

<img width="915" alt="screen shot 2017-12-08 at 10 56 20" src="https://user-images.githubusercontent.com/25227268/33760587-73cc41f8-dc06-11e7-82b3-44bf3bd09f5d.png">

The block and unblock IP action will quarentine the IP for a given time.

<img width="517" alt="screen shot 2017-12-08 at 11 03 41" src="https://user-images.githubusercontent.com/25227268/33760840-7d2e13ba-dc07-11e7-898d-7a8db2968efd.png">

<img width="1440" alt="screen shot 2017-12-08 at 11 04 49" src="https://user-images.githubusercontent.com/25227268/33760901-a7e3a32c-dc07-11e7-9242-97a9159c3489.png">

## Summary

With this integration it is possible to integrate McAfee NSM and the orchestration platform Phantom by performing key action for threat containment and response.
