# Scheduled Jobs

Imports in Geoprism Registry run in the background as scheduled jobs. The **Scheduled Jobs** page lets you follow an import while it runs, fix any problems it finds, and review past imports.

Each import goes through four steps:

1. **File Import:** the file is uploaded.
2. **Staging:** the data is prepared for import.
3. **Validation:** the data is checked, for example for parent locations and terms that can't be found. Nothing is imported yet.
4. **Database Import:** the data is written to the registry.

A job's status is one of **Queued**, **Running**, **Needs Resolution**, **Success**, **Failed** or **Canceled**. A job that needs resolution waits until you fix or ignore its problems.

* [view-scheduled-jobs.md](view-scheduled-jobs.md "mention") explains the jobs list and job details.
* [troubleshooting-scheduled-jobs.md](troubleshooting-scheduled-jobs.md "mention") explains how to resolve problems.
