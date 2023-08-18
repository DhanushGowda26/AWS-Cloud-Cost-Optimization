# AWS-Cloud-Cost-Optimization
Optimize AWS costs with a Lambda function that identifies and deletes stale EBS snapshots, reducing storage expenses. Automated process checks snapshot associations with active EC2 instances, ensuring efficient resource usage. Easy-to-use solution with clear documentation

# Identifying Stale EBS Snapshots
In this example, we'll create a Lambda function that identifies EBS snapshots that are no longer associated with any active EC2 instance and deletes them to save on storage costs.

Description:
The Lambda function fetches all EBS snapshots owned by the same account ('self') and also retrieves a list of active EC2 instances (running and stopped). For each snapshot, it checks if the associated volume (if exists) is not associated with any active instance. If it finds a stale snapshot, it deletes it, effectively optimizing storage costs.
