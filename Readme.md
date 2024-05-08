## 1.What is AWS?

<h1>AWS is Amazon’s cloud service.</h1>

- It let’s you 
- Rent servers
- Manage domains
- Upload objects (mp4 files, jpgs, mp3s …)
- Autoscale servers
- Create k8s clusters

</h3>
The offering is Renting servers
<h3>

## 2.EC2 servers

<h2>VMs on AWS are called EC2 Servers<br>
EC2 stands for Elastic compute Version 2.</h2>

1. Elastic - Can increase/decrease the size of the machine
2. Compute - It is a machine
You can spin up a new EC2 instance from the aws dashboard

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2Ff0ee3fa6-e989-4982-a580-e8039c48ae62%2FScreenshot_2024-02-11_at_6.33.46_AM.png?table=block&id=3dc2315f-4c68-4d34-995e-c56ba0d08feb&cache=v2" alt="EC2">

## 3.Creating a new EC2 server

1. Click on Launch a new instance

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2Fce12b6eb-5d32-4cfa-bf79-049356382237%2FScreenshot_2024-02-11_at_6.35.37_AM.png?table=block&id=62284127-f634-49e1-8372-ae190cbe5e53&cache=v2" alt="">

2. Give a name 

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F99db06f8-46b8-4724-97b0-edf8eceddc2a%2FScreenshot_2024-02-11_at_6.40.08_AM.png?table=block&id=dc8d9b86-099f-43d9-b591-b73fba177838&cache=v2" alt="">

3. Select an OS

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F3d164ebc-9528-40fe-a313-669a9346657e%2FScreenshot_2024-02-11_at_6.40.15_AM.png?table=block&id=1b5a057c-15c7-4306-9c7c-b777110ce930&cache=v2" alt="">

4. Select size

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F4fad1e6c-5929-4619-87c9-6dd50bc4dc79%2FScreenshot_2024-02-11_at_6.41.19_AM.png?table=block&id=688a2e65-4d63-4976-a9e8-9b0a64038ae5&cache=v2" alt="">

5. Create a new Key pair

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2Fb988d06e-447a-476f-9599-b1b98a561f11%2FScreenshot_2024-02-11_at_6.42.11_AM.png?table=block&id=1f313b84-ebcc-4ac1-a118-7abcd4f33e13&cache=v2" alt="">


6. Select size

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F4f28c0ac-7f35-4200-a0e6-21df5ac982b3%2FScreenshot_2024-02-11_at_6.38.05_AM.png?table=block&id=f32975d3-a6ee-4a3b-a666-33eb338ff4fe&cache=v2" alt="">

7. Allow traffic on http/https

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2Faa98e7a1-aedf-4a1a-8e53-edb938b1b476%2FScreenshot_2024-02-11_at_6.37.57_AM.png?table=block&id=7f497c85-0715-467d-adcf-1bfc99fe7791&cache=v2" alt="">

## 4.SSH into server
(In your terminal)
1. Give ssh key  permission
chmod 700 web-dev.pem

2. ssh into machine
ssh -i web-dev.pem ubuntu@ec2-65-0-180-32.ap-south-1.compute.amazonaws.com

-- https://www.tecmint.com/resolve-temporary-failure-in-name-resolution/

3. Clone your repo
git clone https://github.com/web-dev

4. Install node.js
https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04

5. Install all dependencies
cd web-dev
npm install

6. Start backend
node index.js

## 5.Try hitting the server
You have an ip/DNS that you can hit to access your ec2 server

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2Fc937d600-8c4e-4c69-8f94-b08d7f47b6af%2FScreenshot_2024-02-11_at_6.54.09_AM.png?table=block&id=39e74650-04ba-490c-9c29-f99dad477d0e&cache=v2" alt="">

<h1>Try visiting the backend</h1>
your_domain:3000

<b>Notice</b> you can’t visit the website during this time

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F90f755af-9a75-4875-a126-1410feef6917%2FScreenshot_2024-02-11_at_6.57.17_AM.png?table=block&id=334e0f49-6d1e-4eeb-bb9d-405efa43671e&cache=v2" alt="">

<h3>Security group</h3>

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F1b991aa0-bc28-4642-83b9-5101a4ba4f4d%2FScreenshot_2024-02-11_at_6.59.14_AM.png?table=block&id=45e8ee3d-7edd-4160-85c5-dccc8abb6df8&cache=v2" alt="">

You can either open port 8080, or process on port 80

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2Febe18a38-147c-4866-9a30-71bace5a829c%2FScreenshot_2024-02-11_at_7.01.21_AM.png?table=block&id=48e9db64-d800-4c6e-87e9-1b890aa215e3&cache=v2" alt="">

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F5cb4a372-d4db-4698-94c6-37ccaccf9fab%2FScreenshot_2024-02-11_at_7.02.59_AM.png?table=block&id=0c572982-e36c-4658-934d-6753620b7f93&cache=v2" alt="">

http://your_domain:8080

## 6.nginx
(In your terminal)
https://www.nginx.com/resources/glossary/nginx/

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F0263a8e2-e824-45b1-901c-34b635308f87%2FScreenshot_2024-02-11_at_7.05.48_AM.png?table=block&id=ff5b15cd-c123-4238-a3bb-aada54dd8407&cache=v2" alt="">

- What is a reverse proxy?

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F2f9a47c6-e0ae-4819-a24e-f9110af8afd6%2FScreenshot_2024-02-11_at_7.12.50_AM.png?table=block&id=e8fc9376-df68-4487-8363-6a3aa4a8ebd8&cache=v2" alt="">

- Installing nginx
sudo apt update
sudo apt install nginx

This should start a nginx server on port 80

Try visiting the website

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2Fbc6b7e9a-9119-43d1-bebf-b870fecf66bf%2FScreenshot_2024-02-11_at_8.24.36_AM.png?table=block&id=06f6c8ad-ebd4-485b-ad72-9be5f4b6d6da&cache=v2" alt="">

<h2>Create reverse proxy</h2>
sudo rm sudo vi /etc/nginx/nginx.conf
sudo vi /etc/nginx/nginx.conf

events {
    # Event directives...
}

http {
	server {
    listen 80;
    server_name be1.100xdevs.com;

    location / {
        proxy_pass http://localhost:8080;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
	}
}

sudo nginx -s reload

- Start the Backend server
node index.js

- Visit the website
https://be1.100xdevs.com/

<img src="https://www.notion.so/image/https%3A%2F%2Fprod-files-secure.s3.us-west-2.amazonaws.com%2F085e8ad8-528e-47d7-8922-a23dc4016453%2F6f3c6675-2178-43e1-bbfe-a90e391db2f4%2FScreenshot_2024-02-11_at_8.50.59_AM.png?table=block&id=8a6d5e90-7897-498b-bdd3-bc2ab958c683&cache=v2" alt="">

## 7.Certificate management
- Use https://certbot.eff.org/