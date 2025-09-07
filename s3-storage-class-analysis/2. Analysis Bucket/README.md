### Step 4: Enable Storage Class Analysis

To gather data on object access patterns for future cost-optimization strategies, S3 Storage Class Analysis was enabled on the main bucket. This feature monitors how frequently objects are accessed.

1.  In the "my-main-bucket-for-storage-class-representation" bucket, I navigated to the Management tab.
2.  Under the Analytics section, I selected Storage Class Analysis and chose to Create analysis configuration.
3.  The configuration was set up with the following parameters:
    * Configuration Name: "my-analytics-report-bucket"
    * Scope: The analysis was configured to scan the Entire bucket.
    * Destination for Reports: The secondary bucket, "s3://my-analytics-reports-bucket", was selected to store the generated reports.
    * Destination Prefix: A new prefix, storage-class-reports/, was specified to keep the reports organized within the destination bucket.
4.  Finally, the configuration was saved and enabled.

Note: While the analysis configuration appears in the console immediately, the actual data reports (in CSV format) are generated daily by AWS and are not available instantly.
