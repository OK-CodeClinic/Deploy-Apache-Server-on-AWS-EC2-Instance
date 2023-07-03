# Deploy Apache2 Server on AWS EC2 Instance 

## Description: 
This project shows how i launched my first EC2 instance in my free-tier AWS account to deploy apache2 service on the localhost.


## Steps
#### Region: 
I logged in to my AWS Management Console, I Choosed a region. In my case, i used
  ```US East (N. Virginia) us-east-1```, 
  I Navigate to AWS Services; choose EC2 to create an EC2 INSTANCE  then i followed these Steps below:

#### Step 1: Instance Name and Tags
I added Instance name and tags.
My EC2 name: ```web_01```n and other tags that include;

```Date created```
```Project```
``` Owner```
![Screenshot (35)](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/63f8db40-a821-4bee-a122-3d77b534e51f)


#### Step 2: Choosing an AMI
In the AWS makerplace AMI, thousands of AMI are provided by AWS and other verified.
- In my case i choosed 
  ```Ubuntu 18.04 LTS - Bionic```

#### Step 3: Configuring the Instance
Here, i configured my instance to ```t2 micro``` because its free tier eligible

#### 4: Created a Login Key Pair
In my case; I created a key Pair to login using SSH
  ```web_01-Devops-key```
  
#### Step 5: Configure Security Group and Subnet
- I added a secrity group that allows me to login through SSH port 80.
  ```web_01_SG```
- I select the default VPC
- I select a public subnet in ```Zone: US-east-1c```

### Step 6: Provisioning
In my vagrant expereince i learned about provisioning VMs before launch. Here in this case i did some provisioning to launch apache2 server.

#### Step 7: Review, then Launch
All steps needs to be reviewed before lunch.

#### Step 8: Connecting using SSH
- On my Gitbash, i change direcorty to the directory where my Keypair downloaded was located.

I then connect using the SSH instance ID provided


## Outcomes

#### Step 9: Check apache2 status
- Switch to root user
- Check apache2 status to see if its runnuing

#### Step 10: Connect to my localhost on browser
NB: Here, the secutity group deoesn't permit connection here. So, there is a reason to modify the security group in order to allow access on the local host.



- Now, apache2 is running on the localhost


#### Step 11: Terminate
There is a need to terminate the instance since there all pyurpose has been fufiled.

## Author

- [Kehinde Omokungbe](https://www.github.com/OK-CodeClinic)

