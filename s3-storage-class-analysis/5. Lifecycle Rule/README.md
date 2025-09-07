### Step 5: Create a Demo Lifecycle Rule (Expiration)

To demonstrate the powerful automation capabilities of S3 for cost management, a simple lifecycle rule was created. The goal was to configure a policy that automatically cleans up objects after a short, demonstrable period.

1.  From the "my-main-bucket-for-storage-class-representation" bucket, I navigated to the Management tab and selected Lifecycle rules.
2.  A new lifecycle rule was created with the following configuration:
    * Rule Name: analysis-rule
    * Scope: The rule was applied to the Entire bucket.
    * Action: Expire current versions of objects.
    * Condition: The expiration was set to trigger 2 days after object creation.
3.  The rule was then saved and activated.

#### Why an Expiration Rule for a Demo?

For this short-term demonstration, an expiration rule was specifically chosen over a transition rule (e.g., moving objects to Standard-IA or Glacier). Transition rules require objects to be at least 30 days old, a condition that would not be met in a brief demo. The 2-day expiration rule provides a clear and quick result, effectively showcasing S3's automation capabilities.

In a real-world production scenario, this same lifecycle policy would be expanded. A common best practice would be to first transition infrequently accessed objects to a more cost-effective storage class like S3 Standard-Infrequent Access (Standard-IA) after 30 days, and then set an expiration policy for a much later date.
