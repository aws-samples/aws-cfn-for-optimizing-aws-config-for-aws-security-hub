## AWS CloudFormation for optimizing AWS Config for AWS Security Hub

This repo contains the CloudFormation template to set up AWS Config to record only what’s needed for Security Hub as detailed in the AWS Security Blog Post: Optimize AWS Config for AWS Security Hub. Check out the blog for more information on how to use this CloudFormation template.

### Requirements

This CloudFormation template only works if AWS Config is not currently enabled in the account/region that you want to run it in. For more information on managing the AWS Config recorder check out the [AWS Config User Guide](https://docs.aws.amazon.com/config/latest/developerguide/stop-start-recorder.html).

### Getting Started

Download the CloudFormation template (`AWS-Config-optimized-for-AWS-Security-Hub.yaml`) and deploy it from the console. You can also use AWS CloudFormation StackSets to deploy, update, or delete the template across multiple accounts and Regions with a single operation. 

### Template Parameters

- DeliveryChannelName
    - The name of the delivery channel.
- Frequency
    - The frequency with which AWS Config delivers configuration snapshots.
- TopicArn
    - The Amazon Resource Name (ARN) of the Amazon Simple Notification Service (Amazon SNS) topic that AWS Config delivers notifications to. Note: Leaving `<New Topic>` as the TopicArn will result in the generation of a new topic.
- NotificationEmail
    - Email address for AWS Config notifications (for new topics).

## Security

See [CONTRIBUTING](CONTRIBUTING.md#security-issue-notifications) for more information.

## License

This library is licensed under the MIT-0 License. See the LICENSE file.

