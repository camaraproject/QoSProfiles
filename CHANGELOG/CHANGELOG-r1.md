# Changelog QoSProfiles

<!-- TOC:START -->
## Table of Contents
- [r1.1](#r11)
<!-- TOC:END -->

**Please be aware that the project will have frequent updates to the main branch. There are no compatibility guarantees associated with code in any branch, including main, until it has been released. For example, changes may be reverted before a release is published. For the best results, use the latest published release.**

The below sections record the changes for each API version in each release as follows:

* for an alpha release, the delta with respect to the previous release
* for the first release-candidate, all changes since the last public release
* for subsequent release-candidate(s), only the delta to the previous release-candidate
* for a public release, the consolidated changes since the previous public release

# r1.1

## Release Notes

This release candidate contains the definition and documentation of
* qos-profiles 1.2.0-rc.4

The API definition(s) are based on
* Commonalities r4.4 (0.9.0)
* Identity and Consent Management r4.2 (0.5.0)

## qos-profiles 1.2.0-rc.4

**qos-profiles 1.2.0-rc.4 is a release-candidate version of this API.**

- API definition **with inline documentation**:
  - [View it on ReDoc](https://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/camaraproject/QoSProfiles/r1.1/code/API_definitions/qos-profiles.yaml&nocors)
  - [View it on Swagger Editor](https://camaraproject.github.io/swagger-ui/?url=https://raw.githubusercontent.com/camaraproject/QoSProfiles/r1.1/code/API_definitions/qos-profiles.yaml)
  - OpenAPI [YAML spec file](https://github.com/camaraproject/QoSProfiles/blob/r1.1/code/API_definitions/qos-profiles.yaml)

### Breaking changes

* No breaking changes for API consumers: the HTTP method, path, request and response payloads are unchanged. Note that the operationId `retrieveQoSProfiles` was renamed to `retrieveQosProfiles` (#16), so code generated from the spec (client/server stubs) and test tooling that references the operationId or scenario tags will need updating.

### Added

* New test scenario `@qos_profiles_retrieveQosProfiles_02b_filter_by_name_not_found`: calling `retrieveQosProfiles` with a `name` that matches no profile returns `200` with an empty array (#26)

### Changed

* The API moved from QualityOnDemand to the new QoSProfiles repository. `externalDocs.url` now points to `https://github.com/camaraproject/QoSProfiles` (#18)
* The API description no longer limits QoS Profiles to Quality-On-Demand. It now lists QualityOnDemand, QoSBooking, DedicatedNetworks and NetworkSliceBooking as the APIs that use it (#19)
* Aligned with Commonalities r4.4 (`x-camara-commonalities: 0.9.0`), including the updated `additional-error-responses` description template (#12, #26)
* Error responses now use the Commonalities r4.4 response catalogue (`BadRequest400`, `Unauthenticated401`, `PermissionDenied403`, `NotFound404`, `IdentifierNotFound404`, `TooManyRequests429`) instead of the API's own `Generic*` definitions. `Generic422` is renamed to `RetrieveQosProfilesUnprocessable422` and uses the common `*_DEVICE` 422 examples (#26)
* The `404` response of `retrieveQosProfiles` now declares only `IDENTIFIER_NOT_FOUND`. `NOT_FOUND` was removed because this operation has no resource path that can be missing (#26)
* The `Duration.value` maximum is reduced from `2147483647` to `99999` (#24, #29)
* Test definitions: schema pointers now use the `#/components/...` form throughout (#26)

### Fixed

* The operationId `retrieveQoSProfiles` is corrected to `retrieveQosProfiles`. The feature file and scenario tags were renamed to match (#16)
* The `countryName` description now cites ISO 3166-1 alpha-2 instead of ISO 3166-2 (#14)
* The "DCSP" typo in the `serviceClass` table is now "DSCP", and the reference to the archived HomeDevicesQoD API is removed (#15)
* The CAMARA API Design Guide link now points to Commonalities r4.4 instead of r3.3 (#17, #26)

### Removed

* The API's own error response components `Generic400`, `Generic401`, `Generic403`, `NotFound404`, `RetrieveQosProfilesNotFound404` and `Generic429`. Commonalities references replace them (#26)

**Full Changelog**: https://github.com/camaraproject/QoSProfiles/commits/r1.1

