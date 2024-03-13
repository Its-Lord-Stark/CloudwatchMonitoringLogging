# AWS CloudWatch Logging and Monitoring

This project demonstrates how to set up AWS CloudWatch logging and monitoring using an EC2 instance and various AWS services.

## Overview

The project involves setting up a Linux EC2 instance, installing the AWS CloudWatch agent, creating a logging group, setting up a pattern filter, defining custom metrics, and configuring an alarm to trigger based on specific conditions.

## Installation

1. **Create an EC2 Instance**: Launch a Linux EC2 instance on AWS.


2. **Install AWS CloudWatch Agent**: Install the AWS CloudWatch agent on the EC2 instance. You can find installation instructions [here](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/install-CloudWatch-Agent-commandline-fleet.html).

![CloudwatchAgentInstalled](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/40339f7b-4346-4221-9e8c-e41498abb495)


3. **Create Logging Group**: In the CloudWatch console, navigate to the "Log groups" section and create a new log group for the EC2 instance.
![Logfile](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/556cc4c2-a947-4d2a-9bf9-4d04b40047a5)


4. **Define Log Stream**: Within the created log group, define a log stream to receive logs from the EC2 instance.

5. **Set Up Pattern Filter**: Create a pattern filter for the log stream to filter for the word "error" or any other desired pattern.

6. **Define Custom Namespace and Metrics**: In the CloudWatch Metrics section, define a custom namespace and metrics based on the logs received from the EC2 instance.


![CretingAlarm](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/8a8689e3-d3db-4472-abc6-418ba6fa9264)



7. **Create Alarm**: Set up an alarm based on the custom metrics. Define conditions such as receiving three matches to the "error" filter within 30 seconds.
   
![AlarmPage](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/ce514645-53e9-4abd-9f2c-735bccbc6fe6)

   
![AlarmDetails](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/361d7623-11bd-4e3f-9301-9515d1e55356)


9. **SNS Topic and Email**:

![NewSNSTopic](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/e81ce1fa-600a-41bf-a18c-60001acef991)




## Usage

Once the setup is complete, the CloudWatch agent will start sending logs to the defined log group. The defined pattern filter will filter for specific keywords like "error". The custom metrics will provide insights into the logged data. The alarm will trigger if the specified conditions are met, sending an email notification via SNS.

![SNSEmail](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/4359a357-dd57-4ac3-9009-c97ac6942c16)

## Contributing

Contributions to improve and enhance this project are welcome. Please fork the repository, make your changes, and submit a pull request.
