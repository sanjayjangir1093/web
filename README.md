Deploy a web server on an AWS EC2 instance, configure SSH connectivity between instances,
and automate the hosting process using a shell script 

          1st.task  AWS Setup and Instance Management:
- Launch two t2.micro EC2 instances using different operating systems (Amazon Linux and
Ubuntu).
1  instance is amazone linux os and instance name server 1
  ![Screenshot 2024-10-24 112814](https://github.com/user-attachments/assets/676aac5e-6a94-476f-b753-18324d6d84af)
after name choose AMI
![Screenshot 2024-10-24 112835](https://github.com/user-attachments/assets/71091716-9812-4745-b2b2-f827c3b44ee7)
choose instance type t2.micro and create key(SECRET-KEY)
![Screenshot 2024-10-24 112904](https://github.com/user-attachments/assets/166b00bd-8731-481a-bc7d-bf673dd9d8d6)
and after create network setting(defult network) and configure storage 8gb and launch instance 
![Screenshot 2024-10-24 113235](https://github.com/user-attachments/assets/af8d0385-f50b-44bc-a22f-da44949d16a4)

2 instance choose os is ubuntu and instance name is server 2
after same work 

![Screenshot 2024-10-24 113127](https://github.com/user-attachments/assets/0020efe2-39b0-4de7-af22-06db1dc69452)
![Screenshot 2024-10-24 113202](https://github.com/user-attachments/assets/f977001d-266f-4ef6-9fd3-a53454a30513)
![Screenshot 2024-10-24 113235](https://github.com/user-attachments/assets/10bb0545-a871-4cef-b956-62094d09cdaf)
![Screenshot 2024-10-24 113255](https://github.com/user-attachments/assets/8406ddcd-0718-443f-bde8-d20db9087738)
![Screenshot 2024-10-24 121824](https://github.com/user-attachments/assets/01b7150d-ef0c-4834-a559-61987363f73d)





                          2nd TASK IS Instance Management:
- Start, stop, restart, and terminate EC2 instances.


- START INSTANCE ![Screenshot 2024-10-24 181121](https://github.com/user-attachments/assets/be155216-9922-4e15-b02b-4b2ab5ddd6e2)

- ![Screenshot 2024-10-24 180546](https://github.com/user-attachments/assets/e573c421-c8ce-4144-91f8-f6089f3e3b8d)


- STOP INSTANCE ![Screenshot 2024-10-24 120923](https://github.com/user-attachments/assets/83bdf55d-9bc1-4e81-9c37-246aa0301ed2)

- ![Screenshot 2024-10-24 181019](https://github.com/user-attachments/assets/6ec867e4-988b-40c3-8f68-edcea499436d)




- RESTART INSTANCE ![Screenshot 2024-10-24 181511](https://github.com/user-attachments/assets/cdf492d3-5c68-440f-94a7-1f8c9de88a10)

- ![Screenshot 2024-10-24 120847](https://github.com/user-attachments/assets/2a86368e-a302-4b79-80b0-7f50f1039da1)
- 



- TERMINATE INSTANCE ![Screenshot 2024-10-24 120949](https://github.com/user-attachments/assets/f95d61ce-800e-4716-878b-53542ad7a6ee)
 ![Screenshot 2024-10-24 181626](https://github.com/user-attachments/assets/c895a0d0-20a3-4140-9160-a839bdf5a26d)






             3rd task is SSH Configuration & Connectivity
  Set up SSH key pairs to allow secure connection
  launch instance section and create new key (SERVER-KEY)
 ![Screenshot 2024-10-24 182244](https://github.com/user-attachments/assets/3fe39b01-4170-459a-a9e6-0f483906e1c8)
  Connect to both instances from your local machine using SSH.
- 1st session for amazon linux in my cmd  ![Screenshot 2024-10-24 122446](https://github.com/user-attachments/assets/0d870a7c-2edf-4d2a-851e-562c87fb1bf4)
![Screenshot 2024-10-24 122533](https://github.com/user-attachments/assets/7506ae58-a873-40ba-8369-2b3b47cf4081)
- 2nd for ubnutu ![Screenshot 2024-10-24 185337](https://github.com/user-attachments/assets/be040ca1-9790-4ae7-849e-945820709470)

- ![Screenshot 2024-10-24 122715](https://github.com/user-attachments/assets/f94aaa00-5151-4346-9a26-7d70562df924)
- Configure security group (HTTP,HTTPS and ICMP)
- ![Screenshot 2024-10-24 122858](https://github.com/user-attachments/assets/4594f508-9cd8-4772-b1bb-e7c964805357)
  PING CHECK CONNECTIVITY BOTH INATANCE LINUX TO UBUNTU USE PRIVATE IP
  ![Screenshot 2024-10-24 123059](https://github.com/user-attachments/assets/7d1f4ef0-8a93-41c4-82c1-44a4df761149)
  PING CHECK CONNECTIVITY BOTH INATANCE UBUNTU TO LINUX PRUVATE IP
  ![Screenshot 2024-10-24 123212](https://github.com/user-attachments/assets/4a032472-431d-4a3c-bcf5-6c5cff8ffdb2)


             4th task is install web server
  - install nginx and apache2 server
  - before install update instance use command sudo apt update after use command apt install nginx -y && sudo apt install apache2 -y
  - ![Screenshot 2024-10-24 125122](https://github.com/user-attachments/assets/da295fdb-85fd-42cc-abcd-5d6e60bd7d1a)
  - ![Screenshot 2024-10-24 125530](https://github.com/user-attachments/assets/9e1061dd-d01a-459e-a956-0069ed49ffaf)
  - check version
  - ![Screenshot 2024-10-24 125642](https://github.com/user-attachments/assets/dfff428e-2ea0-41f4-9341-45ff343135a2)
  - start service (sudo systemctl start and check status)
  - ![Screenshot 2024-10-24 130052](https://github.com/user-attachments/assets/44cedea4-4874-42e1-86c3-238d1e24ec76)
  -  Create a simple HTML web page with text "Hello World"
  -  ![Screenshot 2024-10-24 160044](https://github.com/user-attachments/assets/f283ebf3-f2e5-4782-90a9-36bd822a7ee9)
  -  ![Screenshot 2024-10-24 160148](https://github.com/user-attachments/assets/33261c52-8c41-40d1-b641-90681e64b8b9)
  -  ![Screenshot 2024-10-24 160204](https://github.com/user-attachments/assets/39505705-1593-4cec-a9bd-4a1ed55010cc)
  -  ![Screenshot 2024-10-24 160313](https://github.com/user-attachments/assets/e4127038-7871-4b80-aa44-9d6fcab7ce38)
 



-







