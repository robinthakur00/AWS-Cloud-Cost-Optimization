# AWS Cloud Cost Optimization 


## Identifying Stale EBS Snapshots

In this particular example, we are going to generate a Lambda function that is able to recognize EBS snapshots that are no longer linked to any active EC2 instance and remove them in order to reduce storage expenses.

## Description:

The Lambda function is designed to fetch all EBS snapshots that are owned by the account itself and to gather a roster of active EC2 instances, including those that are running and those that are stopped. The function then examines each snapshot to determine whether the associated volume, if it exists, is not associated with any active instance. If a snapshot is found to be outdated, it is removed, resulting in a more efficient use of storage resources and reduced costs.
