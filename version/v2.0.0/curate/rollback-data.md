# Rollback Data

Rollback returns the registry to the state it was in before a data import. Use it to undo an import that loaded the wrong file or bad data.

Each time a data import runs, Geoprism Registry saves a **rollback checkpoint** for it. The **Data Rollback** page lists these checkpoints by file name, newest first.

{% hint style="danger" %}
A rollback can't be undone. Rolling back an import also rolls back **every import and change made after it**, not just that one file.
{% endhint %}

## When you can roll back

* **Before publishing.** Publishing a [Spatial Knowledge Graph](../explore/spatial-knowledge-graphs-skg/README.md) deletes all rollback checkpoints, because data that has been published can no longer be rolled back. Only imports made since the last publish can be rolled back.
* **When no imports are running.** You can't start a rollback while a data import is running or scheduled. Check the [Scheduled Jobs](scheduled-jobs/view-scheduled-jobs.md) page first.
* **One rollback at a time.** You can't start a rollback while another one is in progress.

## Rolling back an import

1. Navigate to the **Data Rollback** page from the sidebar.
2. Find the import you want to undo. Click its file name to open the import job and check that it's the right one.
3. Click **Rollback** next to the file.
4. A confirmation asks whether you want to roll back all data imported, and all changes made, since before that file was imported. Click **Rollback** to confirm.

A progress bar shows the rollback as it runs. The imports are undone one at a time, starting with the newest. When the rollback finishes, the checkpoints it undid are removed from the list.
