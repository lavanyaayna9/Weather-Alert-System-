Intelligent Weather Alert System for Airlines
This project automates weather alerts using a Bash script on an AWS EC2 instance. The script fetches weather data, checks conditions, and triggers SNS alerts for freezing temperatures, ensuring timely notifications for necessary actions. This helps airlines make informed decisions to enhance passenger safety.

Steps:

1. Create an IAM Role for EC2-
Go to IAM Console and create a new role.
Assign EC2, SNS, and CloudWatch FullAccess permissions to the role.
Name the role and complete the role creation.

2. Launch an EC2 Instance & Attach IAM Role-
Open AWS Console > EC2 > Launch Instance.
Name the instance, select Amazon Linux as OS, configure instance type.
Allow SSH and HTTP access in security group settings.
Attach the IAM Role created earlier in Advanced Settings.
Click on Launch Instance.

3. Install Dependencies on EC2-
Connect to the EC2 instance via SSH.
Update packages and install essential tools.
Install pip and boto3 for AWS integration.

4. Create an SNS Topic-
Go to AWS SNS Console and create a new topic.
Define a topic name and description, then click on Create Topic.

5. Subscribe to the SNS Topic-
Create an email subscription for receiving alerts.
Confirm the subscription via email verification.
Verify subscription status.

6. Deploy Weather Alert Script-
Store the API key as an environment variable.
Upload and modify the Bash script for automating weather alerts.
Test the script and validate the output.

7. Automate the Script Using Cron Jobs-
Configure crontab to run the script at regular intervals.
Check the status of crontab and monitor execution logs.

8. Receive Weather Alerts via SNS-
Verify SNS updates and subscription status.
Test SNS notifications for freezing temperatures.

This project successfully automates weather alerts for airlines using AWS services like IAM, EC2, and SNS. By fetching real-time weather data and triggering notifications for freezing temperatures, it ensures timely alerts to enhance passenger safety. This setup can be expanded to monitor various weather conditions, multiple locations, or even integrate mobile push notifications for comprehensive alert management.
