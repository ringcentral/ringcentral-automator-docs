# Trigger: Scheduled

The **Scheduled trigger** is used for workflows that need to be executed automatically at a specific point in time or on a repeating basis. Unlike the On-Demand trigger, Scheduled workflows are entirely **autonomous**—they run without human intervention and cannot prompt a user for input at the time of execution.

They are analogous to **cronjobs**, serving as a reliable way to automate "set it and forget it" logic.

**When to use Scheduled workflows:**

* **Periodic Communication:** Sending recurring updates, stand-up reminders, or "Team Reminder" messages within chat channels.
* **Future-dated Actions:** Scheduling a message or task to be sent once at a specific future time (similar to a "latergram").
* **Maintenance Tasks:** Running routine data cleanups or system syncs at low-traffic hours.

![On demand workflow execution](../../../img/scheduled-workflow.png)

## Configuration

Because Scheduled workflows must be autonomous, all logic and data must be predefined within the workflow steps. The execution timing is configured using the following parameters:

* **Start Date/Time:** The exact moment the workflow should begin its first (or only) execution.
* **End Date:** (Optional) The date after which the workflow will no longer execute.
* **Recurrence:** An optional setting to repeat the workflow at specific intervals:
    * **Frequency:** Every Day, Week, Month, or Year.
    * **Termination:** Recurrence can be set to end on a specific date or after a certain number of occurrences.

## Inputs

Scheduled workflows **do not support user inputs** at runtime. All data required for the workflow to function must be:

1.  Hardcoded into the workflow steps.
2.  Retrieved dynamically from external systems (e.g., via an API call) during execution.
3.  Defined as static variables during the initial creation of the workflow.

## Outputs

When a scheduled workflow completes, the execution is logged within the Workflow Builder history. While there is no "active" user to view the output immediately, the results are captured as **JSON** for administrative review:

* **Execution Metadata:** Includes the `execution_id`, `status` (Success/Failure), and the precise `trigger_time`.
* **Log Data:** A record of whether the scheduled message or task was successfully delivered to the target destination.

## Execution

The execution lifecycle for a Scheduled workflow is handled by the system's internal scheduler:

1.  **Registration:** The creator sets the schedule parameters and activates the workflow.
2.  **Queueing:** The system monitors the clock; when the designated time is reached, the workflow is placed in the execution queue.
3.  **Autonomous Run:** The workflow engine executes the steps using the predefined logic. No user interaction is requested.
4.  **Logging:** The system records the outcome in the WFB history for audit
