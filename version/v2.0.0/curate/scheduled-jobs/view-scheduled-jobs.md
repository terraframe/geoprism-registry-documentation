# View Scheduled Jobs

The **Scheduled Jobs** page lists the imports that are running or waiting for you to act, and a history of completed jobs.

1. Navigate to the **Scheduled Jobs** page from the sidebar. After you start an import, you can also click **Go to jobs** in the confirmation window.

## Jobs in progress

The **In progress** table shows each running import with its file name, the date it started and its status. A step indicator shows how far the import has got: **File Import**, **Staging**, **Validation** and **Database Import**. A step with a problem is highlighted in red.

<figure><img src="../../../../.gitbook/assets/image (14) (2).png" alt=""><figcaption></figcaption></figure>

Each job has buttons for what you can do next:

* **Details** opens the job's details while it runs.
* **Resolve Problems** appears when the job needs your attention (status **Needs Resolution**). It opens the job's details on the problems list. See [troubleshooting-scheduled-jobs.md](troubleshooting-scheduled-jobs.md "mention").
* **Cancel import** appears when problems were found during validation, before any data was imported.
* **Ignore All Errors** appears when problems were found during the database import. Some data has already been imported by then.

## Completed jobs

Click **View completed jobs** to see the **Completed Jobs** table. It lists each finished job with its status, the number of imported records, and when the import started and ended. Click **Details** to open a job.

<figure><img src="../../../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

## Job details

The **Job Details** page shows:

* The file name, who uploaded it and when the import started.
* How many records have been imported out of the total, and how many remain.
* **Configuration**, which shows the settings the import was run with.
* The **View Imported Data** tab, where you can see the imported data, and the **Problems** tab, which lists any problems that need to be resolved.

{% hint style="info" %}
Spatial Knowledge Graph RDF exports also appear on this page. When an export is ready, click **Download RDF Export** to download it. The download is removed 15 days after it was generated.
{% endhint %}
