# AWS CloudWatch Logging and Monitoring

This project demonstrates how to set up AWS CloudWatch logging and monitoring using an EC2 instance and various AWS services.

## Overview

The project involves setting up a Linux EC2 instance, installing the AWS CloudWatch agent, creating a logging group, setting up a pattern filter, defining custom metrics, and configuring an alarm to trigger based on specific conditions.

## Installation

1. **Create an EC2 Instance**: Launch a Linux EC2 instance on AWS.


2. **Install AWS CloudWatch Agent**: Install the AWS CloudWatch agent on the EC2 instance. You can find installation instructions [here](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/install-CloudWatch-Agent-commandline-fleet.html).

   ![CloudwatchAgentInstalled](https://github.com/Its-Lord-Stark/CloudwatchLoggingMonitoring/assets/126385754/b0da5886-3457-4787-9767-4361784f62fe)


4. **Create Logging Group**: In the CloudWatch console, navigate to the "Log groups" section and create a new log group for the EC2 instance.

   ![Logfile](https://github.com/Its-Lord-Stark/CloudwatchLoggingMonitoring/assets/126385754/b514c2bd-8ede-48f0-956f-3e5f03f0fce6)


6. **Define Log Stream**: Within the created log group, define a log stream to receive logs from the EC2 instance.

7. **Set Up Pattern Filter**: Create a pattern filter for the log stream to filter for the word "error" or any other desired pattern.

8. **Define Custom Namespace and Metrics**: In the CloudWatch Metrics section, define a custom namespace and metrics based on the logs received from the EC2 instance.

![CretingAlarm](https://github.com/Its-Lord-Stark/CloudwatchLoggingMonitoring/assets/126385754/c9e6c5a6-d29e-44b1-a30f-8dc222e34faf)




9. **Create Alarm**: Set up an alarm based on the custom metrics. Define conditions such as receiving three matches to the "error" filter within 30 seconds.
![AlarmPage](https://github.com/Its-Lord-Stark/CloudwatchLoggingMonitoring/assets/126385754/5e4682ee-b456-42b6-8c38-51a66b3d0357)

   
![AlarmDetails](https://github.com/Its-Lord-Stark/CloudwatchLoggingMonitoring/assets/126385754/ac7c85ec-e123-4d95-b58b-0f9866e4b85a)



10. **SNS Topic and Email**:

    
![NewSNSTopic](https://github.com/Its-Lord-Stark/CloudwatchLoggingMonitoring/assets/126385754/f128d2e4-1d1c-46c4-8d34-8530be5c5806)

![SNSEmail](https://github.com/Its-Lord-Stark/CloudwatchLoggingMonitoring/assets/126385754/25a6528a-3e6a-441f-9f28-9960df0d5025)





## Usage

Once the setup is complete, the CloudWatch agent will start sending logs to the defined log group. The defined pattern filter will filter for specific keywords like "error". The custom metrics will provide insights into the logged data. The alarm will trigger if the specified conditions are met, sending an email notification via SNS.

## Contributing

Contributions to improve and enhance this project are welcome. Please fork the repository, make your changes, and submit a pull request.
