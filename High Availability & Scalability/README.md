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


## Auto Scaling Group & Load Balancer Creation
- Autoscaling group (ASG) are created with follows steps. Screenshots below display the process followed on AWS.

1. As shown for continuity use the template that was constructed earlier to save time.

![asg1](https://user-images.githubusercontent.com/97620055/187378354-f1c4695c-d086-4e16-a485-4292d3668669.PNG)

2. Selecting of instance type and configuring subnet zones. 
 
![ASG2](https://user-images.githubusercontent.com/97620055/187378564-f72fc205-8e26-4ea8-b6fa-e556c1e638c9.PNG)

3. Creating Application Load Balancer here:

![asg3](https://user-images.githubusercontent.com/97620055/187378955-e2a0d0dd-bd7b-45b7-8b1f-7a74f19227e1.PNG)

4. Configuring ASG policy with relevant details:

![asg4](https://user-images.githubusercontent.com/97620055/187379051-e494d202-5ba0-43b4-aa2a-6282549b030a.PNG)

5. Options to add alert notifications if required.

![asg5](https://user-images.githubusercontent.com/97620055/187379365-1f1746f4-3ff6-4481-87d6-1014d9d2803e.PNG)

6. Add tags as good practice to specify relevant ASG when running.

![asg6](https://user-images.githubusercontent.com/97620055/187379524-a0c70e17-bb11-40f5-9fc8-16b5594252d2.PNG)

7. Confirmation of ASGs have been created.

![asg 7](https://user-images.githubusercontent.com/97620055/187379733-852ae595-5257-498b-955b-211a1754e130.PNG)

8. Testing using DNS name if app is running. It work's !

![ASG DNS Working](https://user-images.githubusercontent.com/97620055/187379886-ee3ebb72-876d-49f9-8f41-2291bcecdecd.PNG)

## Configuring Database ASGs

- The same process is followed as above, however the ALB must be internal as request to database will be made internally so no exposure happens. This is vital for data security.

## New Script Require

