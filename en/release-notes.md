<!-- pre-align:aligned sig=9a6130697b7f -->

<a id="release-notes"></a>
## Release Notes { #release-notes }

**Application Service > Cloud Scheduler > Release Notes**

<a id="april-28-2026"></a>
## April 28, 2026 { #april-28-2026 }
<a id="feature-updates"></a>
### Feature Updates { #feature-updates }
* When creating a schedule or schedule template using the target template, sensitive information is not displayed on the screen.
* When copying a schedule or schedule template using the target template, only non-sensitive information is copied.

<a id="november-25-2025"></a>
## November 25, 2025 { #november-25-2025 }
<a id="added-features"></a>
### Added Features { #added-features }
* Added the feature to verify results for running schedule.

<a id="september-23-2025"></a>
## September 23, 2025 { #september-23-2025 }
<a id="september-23-2025-feature-updates"></a>
### Feature Updates { #september-23-2025-feature-updates }
* Improved log messages to make it easier to identify the cause of errors when schedule execution fails.

<a id="june-24-2025"></a>
## June 24, 2025 { #june-24-2025 }
<a id="bug-fixes"></a>
### Bug Fixes { #bug-fixes }
* Fixed a bug where parameters (Request Body) had to be entered as JSON objects only.

<a id="may-27-2025"></a>
## May 27, 2025 { #may-27-2025 }
<a id="may-27-2025-bug-fixes"></a>
### Bug Fixes { #may-27-2025-bug-fixes }
* Fixed console messages about the time zone applied to the start and end dates.

<a id="april-29-2025"></a>
## April 29, 2025 { #april-29-2025 }
<a id="april-29-2025-bug-fixes"></a>
### Bug Fixes { #april-29-2025-bug-fixes }
* Fixed a bug where the schedule execution time was not displayed when a Cron expression was set to every Sunday during schedule creation or editing.

<a id="march-25-2025"></a>
## March 25, 2025 { #march-25-2025 }
<a id="march-25-2025-added-features"></a>
### Added Features { #march-25-2025-added-features }
* Added the target template feature.

<a id="march-25-2025-feature-updates"></a>
### Feature Updates { #march-25-2025-feature-updates }
* Modified to limit the size of parameters to 256 KB when creating and modifying schedules and templates.

<a id="january-21-2025"></a>
## January 21, 2025 { #january-21-2025 }
<a id="january-21-2025-feature-updates"></a>
### Feature Updates { #january-21-2025-feature-updates }
* Added restrictions when creating schedules.
  * Changed the maximum length of a URL to 255 characters when creating and modifying schedules.
  * Changed the maximum size of a parameter to 56 KB when creating and modifying schedules.
  * Changed the start date when creating and modifying schedules to only be set to 5 minutes after the current time.
* Made modifications to ignore spaces before and after search terms when searching for schedules and templates.
* Changed error messages.

<a id="december-24-2024"></a>
## December 24, 2024 { #december-24-2024 }
<a id="december-24-2024-added-features"></a>
### Added Features { #december-24-2024-added-features }
* Added the schedule template feature.

<a id="november-26-2024"></a>
## November 26, 2024 { #november-26-2024 }
<a id="november-26-2024-bug-fixes"></a>
### Bug Fixes { #november-26-2024-bug-fixes }
* Fixed a bug that causes schedule execution to fail intermittently.

<a id="oct-29-2024"></a>
## Oct 29, 2024 { #oct-29-2024 }
<a id="release-of-a-new-service"></a>
### Release of a New Service { #release-of-a-new-service }
* Cloud Scheduler is a service that allows you set various tasks to run on a schedule of your choosing.