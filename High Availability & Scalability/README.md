# High Availability and Scalability

 - Autoscaling Groups - 
 - Load Balancing - 

## Diagram Showcasing Autoscaling & Load Balancing 

![image](https://user-images.githubusercontent.com/97620055/186613008-4358d007-bc5e-449e-8c7f-6e17e653f6c8.png)



## Architecture for Multi-AZs, ALB and ASG

![image](https://user-images.githubusercontent.com/97620055/186875999-30611641-587f-48d8-9c73-ec1076a5e976.png)


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

## Load Balancer / Target Group

## Auto Scaling Group Creation
- Autoscaling group (ASG) are created with follows steps. Screenshots below display the 