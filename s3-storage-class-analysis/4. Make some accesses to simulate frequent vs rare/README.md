### Step 4: Simulate Object Access Patterns

To generate meaningful data for the Storage Class Analysis feature, I simulated different access patterns on the objects in the bucket. This process creates a distinction between frequently and infrequently accessed files, which the analysis tool can then report on.

* Frequent Access Simulation:
    * A select few files were accessed repeatedly to simulate "hot" data.
    * This was done by downloading the objects directly from the S3 console (Object actions → Download) approximately 10-20 times over a 1-2 day period. Each download registers as a GET request, which is tracked by the analysis tool.

* Infrequent Access Simulation:
    * The remaining objects in the bucket were intentionally left untouched to simulate "cold" or rarely used data.

This entire process was performed with low, controlled traffic to generate just enough data for the analysis without creating a significant load.
