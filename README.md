<a href="https://github.com/camaraproject/QoSProfiles/commits/" title="Last Commit"><img src="https://img.shields.io/github/last-commit/camaraproject/QoSProfiles?style=plastic"></a>
<a href="https://github.com/camaraproject/QoSProfiles/issues" title="Open Issues"><img src="https://img.shields.io/github/issues/camaraproject/QoSProfiles?style=plastic"></a>
<a href="https://github.com/camaraproject/QoSProfiles/pulls" title="Open Pull Requests"><img src="https://img.shields.io/github/issues-pr/camaraproject/QoSProfiles?style=plastic"></a>
<a href="https://github.com/camaraproject/QoSProfiles/graphs/contributors" title="Contributors"><img src="https://img.shields.io/github/contributors/camaraproject/QoSProfiles?style=plastic"></a>
<a href="https://github.com/camaraproject/QoSProfiles" title="Repo Size"><img src="https://img.shields.io/github/repo-size/camaraproject/QoSProfiles?style=plastic"></a>
<a href="https://github.com/camaraproject/QoSProfiles/blob/main/LICENSE" title="License"><img src="https://img.shields.io/badge/License-Apache%202.0-green.svg?style=plastic"></a>
<a href="https://github.com/camaraproject/QoSProfiles/releases/latest" title="Latest Release"><img src="https://img.shields.io/github/release/camaraproject/QoSProfiles?style=plastic"></a>
<a href="https://github.com/camaraproject/Governance/blob/main/ProjectStructureAndRoles.md" title="Incubating API Repository"><img src="https://img.shields.io/badge/Incubating%20API%20Repository-green?style=plastic"></a>

# QoSProfiles

Incubating API Repository to evolve and maintain the definitions and documentation of QoSProfiles Service API(s) within the Sub Project [ConnectivityQualityManagement](https://lf-camaraproject.atlassian.net/wiki/x/hAClB)

* API Repository [wiki page](https://lf-camaraproject.atlassian.net/wiki/x/hAClB)

> [!NOTE]
> This repository is being split out of [QualityOnDemand](https://github.com/camaraproject/QualityOnDemand), where the `qos-profiles` API was originally defined and released. For releases up to and including QualityOnDemand's Fall25 release (r3.2), see the [QualityOnDemand releases](https://github.com/camaraproject/QualityOnDemand/releases) and the history of [qos-profiles.yaml](https://github.com/camaraproject/QualityOnDemand/commits/main/code/API_definitions/qos-profiles.yaml) there. The initial content seed into this repository is tracked in a separate pull request.

## Scope

* Service API “qos-profiles” (see APIBacklog.md)
* The API provides the API consumer with the ability to:
  * discover all QoS profiles offered by the API provider
  * discover the available QoS profiles for a specific device
  * retrieve the characteristics of a specific QoS profile by name
* QoS profiles are used in conjunction with APIs in QualityOnDemand, QoSBooking, DedicatedNetworks, and NetworkSliceBooking, letting the API consumer request stable latency (reduced jitter) or throughput for specified application data flows or network slices
* Describe, develop, document, and test the API
* Started: April 2024 (within [QualityOnDemand](https://github.com/camaraproject/QualityOnDemand) repository)

<!-- CAMARA:RELEASE-INFO:START -->
<!-- The following section is automatically maintained by the CAMARA project-administration tooling: https://github.com/camaraproject/project-administration -->

## Release Information

The repository has no (pre)releases yet, work in progress is within the main branch.

<!-- CAMARA:RELEASE-INFO:END -->

> [!NOTE]
> Released versions of `qos-profiles` up to and including `1.2.0-rc.3` can be found in [QualityOnDemand](https://github.com/camaraproject/QualityOnDemand); see the [QualityOnDemand releases](https://github.com/camaraproject/QualityOnDemand/releases) there.

## Contributing

* Meetings are held virtually
  * Schedule: bi-weekly, Friday, 13:00 UTC (14:00 CET, 15:00 CEST). For date/time of the next meeting, see previous meeting minutes
  * [Registration / Join](https://zoom-lfx.platform.linuxfoundation.org/meeting/94112812156?password=f238d6af-c959-48d7-a862-abdb3c648e40)
  * Minutes: Access [meeting minutes](https://lf-camaraproject.atlassian.net/wiki/x/XCPe)
* Mailing List
  * Subscribe / unsubscribe to the mailing list of this Sub Project <https://lists.camaraproject.org/g/sp-cqm>.
  * A message to the community of this Sub Project can be sent using <sp-cqm@lists.camaraproject.org>.
