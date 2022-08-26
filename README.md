# Cloud Monitoring and Alert Management


## What Is Cloud Monitoring ?
- Cloud monitoring is a broad category that includes monitoring of web and cloud applications, infrastructure, networks, platform, application, and micro-services.

## Four Golden Signals That Should Be Monitored.

   1. Latency - Time taken by the host server to approve the request of a real user. 
   2. Traffic -  The load users put on an application. All the users using an application are combined to measure the total load. Real-time monitoring is essential. 
   3. Errors - Should be identified in real-time and, AI for application monitoring is the only solution. HTTP errors - rectified. 
   4. Saturation - is defined as percentage of an application or software system being used. High saturation results in performance degradation. 

## Benefits of cloud monitoring

- Monitoring is crucial to make sure that all the services which you are using on the cloud are running smoothly and efficiently. Such a strategy should focus on identifying when service-level objectives (SLOs) are not being met, likely negatively affecting the user experience. So, then what are the benefits of leveraging cloud monitoring tools? With cloud monitoring:

   - Scaling for increased activity is seamless and works in organizations of any size
   - Dedicated tools (and hardware) are maintained by the host
   - Tools are used across several types of devices, including desktop computers, tablets, and phones, so your organization can monitor apps from any location
   - Installation is simple because infrastructure and configurations are already in place
   - Your system doesn’t suffer interruptions when local problems emerge, because resources aren’t part of your organization’s servers and workstations
   - Subscription-based solutions can keep your costs low

## Types of Monitoring:

1. **Database monitoring**
   - Because most cloud applications rely on databases, this technique reviews processes, queries, availability, and consumption of cloud database resources. This technique can also track queries and data integrity, monitoring connections to show real-time usage data. For security purposes, access requests can be tracked as well. For example, an uptime detector can alert if there’s database instability and can help improve resolution response time from the precise moment that a database goes down.

2. **Website monitoring**
   - A website is a set of files that is stored locally, which, in turn, sends those files to other computers over a network. This monitoring technique tracks processes, traffic, availability, and resource utilization of cloud-hosted sites.

3. **Virtual network monitoring**
   - This monitoring type creates software versions of network technology such as firewalls, routers, and load balancers. Because they’re designed with software, these integrated tools can give you a wealth of data about their operation. If one virtual router is endlessly overcome with traffic, for example, the network adjusts to compensate. Therefore, instead of swapping hardware, virtualization infrastructure quickly adjusts to optimize the flow of data.

4. **Cloud storage monitoring**
   - This technique tracks multiple analytics simultaneously, monitoring storage resources and processes that are provisioned to virtual machines, services, databases, and applications. This technique is often used to host infrastructure-as-a-service (IaaS) and software-as-a-service (SaaS) solutions. For these applications, you can configure monitoring to track performance metrics, processes, users, databases, and available storage. It provides data to help you focus on useful features or to fix bugs that disrupt functionality.

5. **Virtual machine monitoring**
   - This technique is a simulation of a computer within a computer; that is, virtualization infrastructure and virtual machines. It’s usually scaled out in IaaS as a virtual server that hosts several virtual desktops. A monitoring application can track the users, traffic, and status of each machine. You get the benefits of traditional IT infrastructure monitoring with the added benefit of cloud monitoring solutions.

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

## Diagram Showcasing Autoscaling & Load Balancing 

![image](https://user-images.githubusercontent.com/97620055/186613008-4358d007-bc5e-449e-8c7f-6e17e653f6c8.png)


## NPM Service Creation

- Used Script As Below: 

![image](https://user-images.githubusercontent.com/97620055/186872885-293a5449-4864-45e5-ab54-dc4d6f111576.png)

## AMI - APP Running

- Configuring userdata as follows:

![User Data - NPM](https://user-images.githubusercontent.com/97620055/186874903-c8d51527-13da-4bca-a083-1be2d96ed845.PNG)

- Saved the latest AMI. Launch the instance and test for app is running. 

![App Running - npm](https://user-images.githubusercontent.com/97620055/186875294-dc5b4a12-4439-4646-a94a-4356a4a28fa3.PNG)


## Template Building

- Created Launch template from the running EC2 instance.

![template build](https://user-images.githubusercontent.com/97620055/186874350-98111c8b-f5f9-4631-aa17-c1d7c5e76c47.PNG)

## Creating Target Grouo

## Create Auto Scaling Group

## Debugging Issues

- User data - different shell than ec2 so when ec2 is stopped. 
- Npm Service - delete and redit script to command. 
