# McAfee-NSM-Phantom
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

This integration is focusing on the threat intelligence sharing with McAfee NSM and the orchestrations platform Phantom. 
The Phantom NSM App provides the capability to publish and ingest threat information. 

This App supports the following actions:

1. **test connectivity** - validate the asset configuration for connectivity using supplied configuration
2. **block ip** - quarantine an IP address for a given time
3. **unblock ip** - unquarantine an IP address
4. **get alert** - Get Alert Details from McAfee NSM
5. **on poll** - ingest McAfee NSM Alerts automatically

## Component Description

**Phantom** is a community powered security automation and orchestration platform. https://www.phantom.us/

**McAfee NSM** gives visibility and control over all McAfee IPS sensors deployed across the enterprise network. https://www.mcafee.com/us/products/network-security-platform.aspx 

## Prerequisites

Phantom Platform tested with version 3.0.284

McAfee NSM 9.1.x (will also work with older NSM versions)

## Configuration
Download the Latest release, open the Phantom Platform and and go to Apps. Under Apps click install app and upload the tgz file. 

<img width="1406" alt="screenshot 2018-11-06 at 18 25 41" src="https://user-images.githubusercontent.com/25227268/48081967-96e8b080-e1f1-11e8-868e-b60d052571f9.png">

Configure a new asset and provide an asset name. In the asset settings define the NSM IP address or hostname, username and password. To ingest alerts provide details what kind of alerts should be ingested, the time and optional a filter for ingestion.

<img width="714" alt="screenshot 2018-11-06 at 18 26 12" src="https://user-images.githubusercontent.com/25227268/48081987-a7992680-e1f1-11e8-9de9-97a78e2bcc7b.png">

If no SensorID is defined click the test connectivity button. The app will recognized that there is no SensorID defined and will get all available SensorIDs.

<img width="810" alt="screenshot 2018-11-06 at 18 26 46" src="https://user-images.githubusercontent.com/25227268/48082006-b41d7f00-e1f1-11e8-8598-21ce066328e2.png">

Enter the required SensorID in the configuration save and test the connectivity again.

<img width="810" alt="screenshot 2018-11-06 at 18 27 06" src="https://user-images.githubusercontent.com/25227268/48082032-c39cc800-e1f1-11e8-92df-820a7351f5ec.png">

The block and unblock IP action will quarentine the IP for a given time.

<img width="517" alt="screen shot 2017-12-08 at 11 03 41" src="https://user-images.githubusercontent.com/25227268/33760840-7d2e13ba-dc07-11e7-898d-7a8db2968efd.png">

<img width="1440" alt="screen shot 2017-12-08 at 11 04 49" src="https://user-images.githubusercontent.com/25227268/33760901-a7e3a32c-dc07-11e7-9242-97a9159c3489.png">

For alert ingestions go to Ingest settings and poll now. The app will reach out to NSM and ingest alerts basend on the configured settings.

<img width="815" alt="screen shot 2018-02-13 at 14 26 01" src="https://user-images.githubusercontent.com/25227268/36152115-117c7948-10ca-11e8-90a8-32c95d2779a1.png">

## Summary

With this integration it is possible to integrate McAfee NSM and the orchestration platform Phantom by performing key action for threat hunting and response.
