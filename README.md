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

  ![AMI](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/64947b8c-094f-4f93-a5e0-ae0cc8af91fd)


#### Step 3: Configuring the Instance
Here, i configured my instance to ```t2 micro``` because its free tier eligible

#### 4: Created a Login Key Pair
In my case; I created a key Pair to login using SSH
  ```web_01-Devops-key```

  ![KeyPair](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/fcdcc76a-9a24-4180-acfb-a66b840c7739)

  
#### Step 5: Configure Security Group and Subnet
- I added a secrity group that allows me to login through SSH port 80.
  ```web_01_SG```
- I select the default VPC
- I select a public subnet in ```Zone: US-east-1c```

- 
![SG](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/4941fbef-9dc4-4fd5-b1a6-5497b4e157be)

![VPC_Subnet](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/a515b404-19a8-44e1-8806-e6656c723ecc)


### Step 6: Provisioning
In my vagrant expereince i learned about provisioning VMs before launch. Here in this case i did some provisioning to launch apache2 server.

![Provisioning](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/18ace43d-d315-4aa0-b64b-a6a275713455)


#### Step 7: Review, then Launch
All steps needs to be reviewed before lunch.

![Launching](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/074048e0-fdd3-4033-a682-1fc0209795fc)

![Instances](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/db0e5d77-064e-4aef-b710-17bf71a19c56)



#### Step 8: Connecting using SSH
- On my Gitbash, i change direcorty to the directory where my Keypair downloaded was located.

- ![SSh_Client](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/0548bb53-cb66-4c25-aa35-270a05f93cd7)


I then connect using the SSH instance ID provided


![SSH_git](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/e9327e68-7ff9-49d1-97cf-8f674fcc748c)


## Outcomes

#### Step 9: Check apache2 status
- Switch to root user
- Check apache2 status to see if its runnuing

- ![CheckApache](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/921340b4-9866-45a8-969e-c498b8435a04)


#### Step 10: Connect to my localhost on browser
NB: Here, the secutity group deoesn't permit connection here. So, there is a reason to modify the security group in order to allow access on the local host.

![Modify+sg](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/ccd2b2c0-9e2b-4915-89d6-7dd010f3db08)

![Edit_SG_AllRules](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/8c0d8125-2932-4f5e-a1eb-4b27551d2285)

![Edit_SG_Successful](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/a288cb3c-1b82-43b0-9fce-a40e1f954cf5)


- Now, apache2 is running on the localhost

![apache_browser](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/f55f3915-8fe0-465b-adb7-435a4c6fb2f3)

#### Step 11: Terminate
There is a need to terminate the instance since there all pyurpose has been fufiled.

![Terminate (1)](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/fd180d6e-6dc3-42a9-934a-cc2cd0935bf1)

![Terminate (2)](https://github.com/OK-CodeClinic/Deploy-Apache-Server-on-AWS-EC2-Instance/assets/100064229/b5f7dcc9-b2ed-4b3b-84d6-6a9e177f6972)


## Author

- [Kehinde Omokungbe](https://www.github.com/OK-CodeClinic)

