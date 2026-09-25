# Troubleshooting Scheduled Jobs

When Geoprism Registry finds problems in an import, the job's status changes to **Needs Resolution** and the job waits for you. Problems are found at one of two stages, and what you can do depends on the stage.

## Finding the problems

1. On the [Scheduled Jobs](view-scheduled-jobs.md) page, find the job in the **In progress** table. The step with the problem is highlighted in red.

   <figure><img src="../../../../.gitbook/assets/image (14) (2).png" alt=""><figcaption></figcaption></figure>
2. Click **Resolve Problems**. The **Job Details** page opens on the **Problems** tab.

   <figure><img src="https://lh4.googleusercontent.com/IhFFTih4s3WozWbMm45gssTdXBCZPzfiWERSX2eUAkDqOqKZDYNKgq696QBFKTEVRGzDB7lAfqKY9dGZFnu5GojoWgdr3J1j3sjiER3NJupj-i4Txa3k1jxw9wr0BJTO0HcIAo5tdDJnlgvCQpZlsNuumVjiXl68soFJFShsIy9cnoS4YT0BI-j-Xw" alt=""><figcaption></figcaption></figure>
3. Click **Resolve** next to a problem to open the **Problem Resolution** window, which explains the problem and how to fix it.

## Problems found during validation

Validation runs before any data is imported. The Problems tab lists each problem with its **Problem Type**, **Label** and **Affected Rows**.

| Problem                                  | How to resolve it                                                                                                                                                                              |
| ---------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A parent Geo-Object can't be found       | **Create Synonym** to map the label in your file to an existing Geo-Object, or **Ignore** all rows with that parent label. Synonyms apply system-wide, including to all future imports.      |
| A term can't be found                    | **Create Synonym** to map the label in your file to an existing term, or **Ignore** all rows with that term label. Synonyms apply system-wide, including to all future imports.               |
| An unexpected error while processing a row | Correct the data in your source file, then click **Re-Upload and Resume Import** and upload the corrected file.                                                                             |

When you've dealt with the problems:

* If all problems are resolved, click **Reimport**.
* Otherwise, click **Resume Import** and confirm to continue the import.
* To stop instead, click **Cancel import**. None of the data is imported.

## Problems found during the database import

Some data has already been imported when these problems are found. The Problems tab lists each problem with its **Problem Type**, **Message** and **Row Number**. Problem types include:

* **Data Not Found**
* **Duplicate Data**
* **Invalid Geometry**
* **Parent Lookup** and **Multiple Parent Match**
* **Postal Code Lookup**
* **Permissions**

Click **Resolve** to see the problem. Where the row created a Geo-Object, you can click **Edit GeoObject** to fix it directly. For other problems, you may need to correct your source file and import it again.

To finish the import without fixing the remaining problems:

1. Click **Ignore All Errors**.

   <figure><img src="../../../../.gitbook/assets/image (26) (1).png" alt=""><figcaption></figcaption></figure>
2. Confirm by clicking **Complete Import**. All unresolved problems are ignored, and the rows that had problems aren't imported.

   <figure><img src="https://lh4.googleusercontent.com/dUb_qP2jbs_1Jhz2M7sL4o7SMNPXek9zMtd0Xp46sva4UFIpCsTrKtYZbineD3KV-a0sVu834moh72446WVaQ0JkGzugodEEHi86Mkar-GLpdgZ6t_GmLIclh1uBlGl6d-FGYyKI6-zGHAP8hpQ7KGXEjqGCiI1pDM-Zw4ULZizvbFCxF54ftmAmcQ" alt=""><figcaption></figcaption></figure>
