# Invicible Brands - Assesment

Question 1:
Solution is saved as a Raman_CloudFormation.yaml file in the github repository.
https://github.com/raman030888/inviciblebrands/blob/master/Raman_CloudFormation.yaml

Question 2 & 3:
Solution for question 2 & 3 is provided in the Solution.docx https://github.com/raman030888/inviciblebrands/blob/master/Solution.docx

__________________

## Question 2:

One of our main challenges is to accommodate huge spikes of traffic, for example - thousands of users online within a couple of minutes. How would you suggest to setup our AutoScalingGroup in order to serve as little 50x errors as possible when scaling aggressively?

## Solution:
•	We have to create a basic auto scaling group under EC2 auto scaling and enable auto scaling metrics and Network Load balancer.
•	We can use the “AWS Auto Scaling” service under Management & Governance in AWS console.
•	Under AWS Auto Scaling service, we have to choose the autoscaling group and Provide a name for our scaling plan.
•	We have to choose the option “Optimize for availability” which will set the threshold to 40% and we can custom the load metrics as well.
•	By doing the above configuration it will scale up the instance with High availability and ability to manage sudden spikes.


## Question 3:
Define and describe a method in detail to use a Redis Cluster via ElastiCache as central PHP Session storage for the AutoScalingGroup above

## Solution:
We have to create the AWS Elastic cache redis instant in Cluster mode enabled. So that Redis will operate as a cluster. This will help to retain the session even if any of the redis instance is down and additional configuration step will be the session save path in PHP “.ini” file should point to cluster configuration endpoint and not an redis endpoint.

