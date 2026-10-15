<!-- pre-align:aligned sig=45254daa27ca -->

<a id="manage-schedule"></a>
## Manage Schedule { #manage-schedule }
**Application Service > Cloud Scheduler > Console User Guide > Manage Schedule**

This document explains the feature to manage the schedules you create.

<a id="modify-schedule"></a>
## Modify Schedule { #modify-schedule }
You can select a schedule to change its information, including execution information, target information, and more. Select the schedule you want to change, then click **Modify Schedule**. See [Create Schedule](create-schedule) to change the schedule information.

!!! danger "Caution"
    It can take up to 20 seconds for changes to the schedule to be reflected, so changes to the contents of the schedule, including activation/deactivation, may fail during that time.

<a id="delete-schedule"></a>
## Delete Schedule { #delete-schedule }
You can select a schedule to delete. You can also delete multiple at the same time. Select the schedule you want to delete, then click **Delete Schedule**.

<a id="copy-schedule"></a>
## Copy Schedule { #copy-schedule }
Select the schedule you want to copy, then click **Copy Schedule**.
The schedule name and description are not copied, which is useful if you want to reuse a pre-created schedule.

!!! danger "Caution"
    When copying a schedule created using the target template, sensitive information in the target template is not copied for security reasons.
    Enter the sensitive information again when copying the schedule.

<a id="activatedeactivate-schedule"></a>
## Activate/Deactivate Schedule { #activatedeactivate-schedule }
Select a schedule, and then click **Activate** or **Deactivate**.

!!! tip "Important"
    * A deactivated schedule will not execute any schedules.
    * If you reactivate a deactivated schedule, it will not run any schedules missed during the deactivation period.
    * Activation and deactivation can each be performed on multiple items simultaneously.
    * However, it is not possible to select both activated and deactivated schedules at the same time.

<a id="view-schedule-information"></a>
## View Schedule Information { #view-schedule-information }
You can select a schedule to view its information in the bottom area of the screen.

* **Basic Info**: Show basic information about the schedule, including the name, description, status, and execution type.
* **Target Info**: Show the information about a target to run a schedule . Target information varies depending on the target type.
    * **Direct Input**: Show the URL, HTTP method, HTTP headers, and parameters to run.
    * **Target Template**: Show the information you entered for the target template to run.

!!! tip "Note"
    Sensitive information in the target template is not provided in its original form for security reasons.

* **Execution History**: Show when the schedule is executed, whether it succeeded or failed, whether it was retried, and the execution log.
    * Execution history is available for viewing for up to 30 days.
* **Additional Settings**: Check the retry policy information.