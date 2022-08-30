# Alert Management

## Diagram of Monitoring Alert and Management

![image](https://user-images.githubusercontent.com/97620055/186612180-2a419b4f-b6b1-428e-9ba9-2ea813bd8a42.png)


## What is Amazon CloudWatch ?

- Amazon CloudWatch is the component of Amazon Web Services that provides real-time monitoring of AWS resources and customer applications running on Amazon infrastructure.

The following image shows the different AWS resources monitored by Amazon CloudWatch.

![image](https://user-images.githubusercontent.com/97620055/186393883-a4d01127-ff42-41db-aea7-e6ba4b0a5425.png)


- Amazon CloudWatch allows administrators to easily monitor multiple instances and resources from one console by performing the below tasks :

- Enables robust monitoring of resources like :

 1. Virtual instances hosted in Amazon EC2
 2. Databases located in Amazon RDS
 3. Data stored in Amazon S3
 4. Elastic Load Balancer
 5. Auto-Scaling Groups
 6. Other resources

- Monitors, stores and provides access to system and application log files.
- Provides a catalog of standard reports that you can use to analyze trends and monitor system performance
- Provides various alert capabilities, including rules and triggers high resolutions alarms and sends notifications
- Collects and provides a real-time presentation of operational data in form of key metrics like CPU utilization, disk storage etc. 

## What is Alert Management - Use cases?

- Alert management is a key part of managing modern, complex systems that are composed of many different APIs and microservices. Alerts are qualified, informational records used to assess and monitor systems to assess current or upcoming problems.
## What Actions To Be Taken In Case of Alert ?

   - Discover all cloud apps and resources used in your organization
   - Identify and revoke access to risky open authorised apps
   - Identify compromised user accounts
   - Enforce DLP policies for sensitive data stored in your cloud apps
   - Enforce adaptive session controls to manage user actions in real-time

## What Is  Amazon Simple Notification Service (SNS) ?

- It is a cloud service for coordinating the delivery of push messages from software applications to subscribing endpoints and clients. All messages published to Amazon SNS are warehoused across several availability zones to prevent loss. 

## What Is Amazon Simple Queue Service (SQS) ?

- It is a managed message queuing service technical professionals and developers use to send, store and retrieve multiple messages of various sizes asynchronously.
- The service enables users to decouple individual microservices, distributed systems and serverless applications from one another and to scale them without requiring the user to establish and maintain their own message queues.

## Alert Management

## Creating An Alarm on AWS:
   - On the left panel in AWS, naviage to alarms and create Alarm with relevant configurations. Deciding on range of metrics and values. I decided to do CPU utilisation > 20% for example below. Usually good practice to set up dashboard to view all your metrics. 

![CPU utilisation done](https://user-images.githubusercontent.com/97620055/186430366-1bb3fe33-a61b-47ad-b965-9f4f351fd832.PNG)

## Configuring SNS:
   - Once alarm is set, configure under actions and edit to set up SNS notification. Provide your email address for alert user when triggered. 

![SNS subsconfirmed](https://user-images.githubusercontent.com/97620055/186430271-adb02dd0-6528-4f61-a283-9a733fa6ab0a.PNG)


### Warning Tested  - CPU Utilisation > 20

1. Once, the metric is determined and value selected for the alarm to trigger.
2. I perfomed while loop to get CPU usage over 20 percent. **Red-Line - Target** (See Image Below).

![cpu alarm](https://user-images.githubusercontent.com/97620055/186595030-339da47e-f875-41f6-a7ff-1a5f3c2121fd.PNG)

3. If configured correctly an email will be sent as warning. Please see below: 

![image](https://user-images.githubusercontent.com/97620055/186595686-89ec3558-a715-4ba7-873f-12f013fd9bf2.png)