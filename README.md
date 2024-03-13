![CloudwatchAgentInstalled](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/70db5a94-2c89-4b0a-a481-ec3c65d33521)# AWS CloudWatch Logging and Monitoring

This project demonstrates how to set up AWS CloudWatch logging and monitoring using an EC2 instance and various AWS services.

## Overview

The project involves setting up a Linux EC2 instance, installing the AWS CloudWatch agent, creating a logging group, setting up a pattern filter, defining custom metrics, and configuring an alarm to trigger based on specific conditions.

## Installation

1. **Create an EC2 Instance**: Launch a Linux EC2 instance on AWS.


2. **Install AWS CloudWatch Agent**: Install the AWS CloudWatch agent on the EC2 instance. You can find installation instructions [here](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/install-CloudWatch-Agent-commandline-fleet.html).

![CloudwatchAgentInstalled](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/75a4a3ea-04dc-4380-ba89-3693677f485e)


4. **Create Logging Group**: In the CloudWatch console, navigate to the "Log groups" section and create a new log group for the EC2 instance.

![Logfile](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/19aeb036-e67d-4d73-9218-5cee1a7b0ec7)


6. **Define Log Stream**: Within the created log group, define a log stream to receive logs from the EC2 instance.

7. **Set Up Pattern Filter**: Create a pattern filter for the log stream to filter for the word "error" or any other desired pattern.

8. **Define Custom Namespace and Metrics**: In the CloudWatch Metrics section, define a custom namespace and metrics based on the logs received from the EC2 instance.


9. **Create Alarm**: Set up an alarm based on the custom metrics. Define conditions such as receiving three matches to the "error" filter within 30 seconds.

   ![AlarmPage](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/14fec3e9-5700-4ffd-bd91-41cac61ad759)

![AlarmDetails](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/d5c3dc44-1e52-4cea-9add-bb9f425d0163)


10. **SNS Topic and Email**:

![NewSNSTopic](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/19aaafea-4ebf-4795-acfa-960571813820)


![SNSEmail](https://github.com/Its-Lord-Stark/CloudwatchMonitoringLogging/assets/126385754/88d8d60f-1424-448f-8122-4ca25c3bd221)




## Usage

Once the setup is complete, the CloudWatch agent will start sending logs to the defined log group. The defined pattern filter will filter for specific keywords like "error". The custom metrics will provide insights into the logged data. The alarm will trigger if the specified conditions are met, sending an email notification via SNS.

## Contributing

Contributions to improve and enhance this project are welcome. Please fork the repository, make your changes, and submit a pull request.
