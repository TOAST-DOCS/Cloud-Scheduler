# Create Schedule
**Application Service > Cloud Scheduler > Console User Guide > Create Schedule**


A schedule consists of basic information, target info, and additional settings.

* Basic information: Select the type, cycle, and start/end dates for the schedule to execute.
* Target info: Enter the API information and HTTP methods, headers, and parameters called by the schedule.
* Additional settings: Set whether to enable/disable the schedule and the retry policy (number of times, interval).

This document explains the steps to create a schedule in detail.

## Create Schedule

To create a schedule, you must first enable the Cloud Scheduler service. See [Guide to Enabling Project Services ](https://docs.nhncloud.com/en/nhncloud/en/console-guide/#guide-to-enabling-project-services) to enable the Cloud Scheduler service.

1. In the NHN Cloud console, click **Application Service > Cloud Scheduler**.

1. Click **+ Create Schedule**.

1. To use templates, select **Enable**.

1. If there's a template you want to use, select the template.

1. Enter basic information settings, then click **Next**.
    * **Name**: Enter a name for the schedule you're creating. You can enter up to 32 characters. 
    * **Description**: Enter a description for the schedule you're creating. You can enter up to 255 characters.
    * **Execution Type**: Select the type of schedule execution. The type can be **one-time** or **recurring**, and the settings will vary depending on the type you select.
        * **One-time**: Run the task only once at the time you specify. Enter the **execution date and time**.
        * **Recurring**: Run the task repeatedly at a set time or at a set interval. You can choose between **Cron** or **Rate** types to set when the task runs.
            * **Cron expression**: Enter 5 fields separated by spaces. The fields are, in order, "minute, hours, day of month, month, day of week". Each field can be entered as shown in the following table, and you can also use symbols to separate entries in each field or to indicate repetition.
            
              | Field | Value | Allowed symbols |
              | --- | --- | --- |
              | Minutes | 0 to 59 | `*`, `,`, `-` |
              | Hours | 1 to 24 | `*`, `,`, `-` |
              | Day of month | 1 to 31 | `*`, `,`, `-` |
              | Month | 1 to 12 or JAN to DEC | `*`, `,`, `-` |
              | Day of week | 0 to 6 or SUN to SAT | `*`, `,`, `-` | 
              
            * **Rate**: Run the schedule at a certain time interval (in minutes/hours/day). You can register for up to 30 days (43,200 minutes, 720 hours).
            
        * **Started on**: The date the schedule starts. The start date is required, The start date can be set from 5 minutes after the current time.
        * **Ended on**: The date on which the schedule ends. If not set, the schedule will continue to run with the recurrence interval you entered.

1. Select a target type. The target type can be either **direct input** or **target template**, and what you enter depends on the type you select.
   * **Direct input**: Enter the target information directly.
        * **URL**: Enter the URL to call. You can enter up to 255 characters.
        * **HTTP Method**: Click the drop-down list to select an HTTP method.
        * **HTTP headers**: Click ** + Add** to enter HTTP headers. You can add up to 20 HTTP headers, and the total size of all headers you add can be up to 8 KB combined.
        * **Parameters**: Enter the body of the request. The Parameters field appears when you select the HTTP method as **POST**, **PUT**, or **PATCH**. The maximum parameter size you can enter is 256 KB.
    * **Target template**: Enter target information based on the target template provided by Cloud Scheduler.

1. After you complete the additional settings, click **Next**.
    * **Activate Schedule**: Select whether to activate the schedule.
    * **Retry policy**: You can set to retry a schedule run when it fails. When you select **set**, the **Retry interval** and **Maximum number of retries** fields are displayed.
        * If the API call fails, retry the schedule according to the retry policy you set.
        * API success vary depending on timeout and result validation conditions.
        * **Retry Interval**: Enter the interval to retry failed schedules. You can set a minimum of 1 minute and a maximum of 60 minutes.
        * **Maximum Number of Retries**: Enter the maximum number of retries. You can set a maximum of 5 retries.
   * **Timeout**: enter the timeout time of the API call. If the API execution time exceeds the set time, the call will fail.
    * **Result Validation**: You can set validation criteria for API call responses. Selecting **User Setting** displays the **Result Validation Conditions** and **Condition Combination Method** fields.
        * **Result Validation Conditions**: set result validation conditions by entering the validation type, target, value, and operator. You can add up to 10 conditions.
            * **Validation Type**: select one of the following:
                * **HTTP Status Code**: validate the HTTP status code of response.
                * **Response Body**: validate the response body.
                * **Response Body(Optional)**: validate the response body. If the validation field entered in the target does not exist in the response body, it is treated as 'True'.
                * **Header**: validate a response header.
            * **Target**: enter the fields to be validated according to the validation type. Up to 50 characeters are allowed.
                * **HTTP Status Code**: disabled as no target to enter exists.
                * **Response Body**: enter JSONPath to specify the field to be validated. For more information, refer to the example below.
                * **Response Body(Optional)**: enter JSONPath to specify the field to be validated. For more information, refer to the example below.
                * **Header**: enter the header name to be validated.
            * **Value**: enter the value of the target to be validated. up to 20 characters are allowed. When validating **HTTP Status Code**, between 100 and 599 characters are allowed.
            * **Operator**: select an operator to use when validating results.
        * **Condition Combination Method**: select how to combine multiple validation conditions.
            * **All Conditions Matched**: if all conditions are 'True', the result is treated as success.
            * **Some Conditions Matched**: if any condition is 'True', the result is treated as success.

> **Example of Response Body (include Optional) JSONPath Target Input**
> ```
> {
>  "firstName": "NHN",
>  "lastName" : "Cloud",
>  "phoneNumbers": [
>    {
>      "type"  : "iPhone",
>      "number": "0123-4567-8888"
>    },
>    {
>      "type"  : "galaxy",
>      "number": "0123-4567-8910"
>    }
>   ]
> }
> ```
> * When validating the **firstName** field in the above response body, JSONPath: `$.firstName`
> * When validating the **type** field of the second object in the **phoneNumbers** field of the above response body, JSONPath: `$.phoneNumbers[1].type`
> * [JSONPath Official Guide](https://goessner.net/articles/JsonPath/)
    


1. In the **Final Review and Save** step, confirm the information you set up earlier and click **Create Schedule**.

!!! tip "Important"
    * You can use the template feature to quickly enter preset information. See [Manage Template](manage-schedule-template).
    * Cron expressions are built with five fields, which are in the order "Minute Hour Day Month Day of Week".
    * For smooth schedule execution, set the start date at least 5 minutes ahead of the current time.
    * It can take up to 30 seconds for the schedule you create to be reflected, so changes to the schedule contents, including activation/deactivation, may fail during that time.


!!! danger "Caution"
    * Cron expressions work based on UTC+09:00. For example, if you enter '0 9 \* \* \*', the task will run every day at 9:00 AM UTC.
    * If you select the recurring type as **Rate**, the schedule execution can change depending on the value of  **Started on** and **Rate**. See [How Rate schedules work](create-schedule/#rate) and [Schedule Execution Examples](create-schedule/#_3) to set them up correctly. 

## How Rate Schedules Work

Rate schedules run schedules based on the time intervals you set.
This section explains how Rate schedules work.

* Intial Start Date: The date the rate schedule first starts is the **started on** time you set.
* Schedule Execution Time: Rate schedules run at the **Rate** interval you set based on the **started on** time. This applies equally to activation after deactivation.
* When Rate changes: When the rate changes, the schedule runs at the changed rate interval. However, it will run at the changed rate interval based on the **started on** time, regardless of the last execution time.

## Schedule Execution Examples

When a schedule runs depends on the start and end dates you set, and what type of schedule you entered.
To help you understand, we'll show you an example of how a Cron and Rate schedule type would run with the same start and end dates.

!!! TIP "Important"
    The date data in Schedule Execution Examples is based on UTC+09:00.


* **Started on**: 2024-01-05 00:00:00
* **Ended on**: 2024-01-08 01:00:00
* For Cron schedules
    * **Cron expression**: 0 12 * * * (run every day at 12 noon)
    * First Schedule Execution Time
        * 2024-01-05 12:00:00
    * Last Schedule Execution Time
        * 2024-01-07 12:00:00
* For Rate schedules
    * General cases
        * **Rate**: Executes every 12 hours
        * First schedule execution time
            * 2024-01-05 00:00:00
        * Last schedule execution time
            * 2024-01-08 00:00:00
    * Disable and enable schedule
        * **Rate**: Executes every 3 hours
        * First execution
            * 2024-01-05 00:00:00
        * Second execution
            * 2024-01-05 03:00:00
        * Disable schedule
            * 2024-01-05 04:00:00
        * Able schedule
            * 2024-01-05 10:00:00
        * Third execution
            * 2024-01-05 12:00:00
        * Fourth execution
            * 2024-01-05 15:00:00
    * Change **Rate**
        * **Rate**: Executes every 3 hours
        * First execution
            * 2024-01-05 00:00:00
        * Second execution
            * 2024-01-05 03:00:00
        * **Rate**: Change to exeuction every 4 hours
            * 2024-01-05 05:00:00
        * Third execution
            * 2024-01-05 08:00:00
        * Fouth execution
            * 2024-01-05 12:00:00