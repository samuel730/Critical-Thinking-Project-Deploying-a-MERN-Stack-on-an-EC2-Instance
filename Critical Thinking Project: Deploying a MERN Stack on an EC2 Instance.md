# Critical Thinking Project: Deploying a MERN Stack on an EC2 Instance

## Project Overview

In this project, I deployed a full MERN (MongoDB, Express, React, Node.js) stack application on an AWS EC2 Ubuntu instance.

The goal of the project was to understand how to configure a cloud server, deploy a backend API, connect it to a database, and serve a frontend application publicly.

I built an Employee Management System that allows users to add, view, and delete employee records.

---

## What I Did

I carried out the full deployment process step by step on an AWS EC2 instance.

I started by launching an EC2 Ubuntu server and connecting to it using SSH from my local machine. After gaining access to the server, I installed Node.js and set up the environment required to run both the backend and frontend applications.

---

## Step 1: Launching the EC2 Instance

I launched an Ubuntu EC2 instance from the AWS Management Console and verified that the instance was running successfully.

### Screenshot

<img width="2560" height="1440" alt="Screenshot 2026-06-11 211414" src="https://github.com/user-attachments/assets/c43d7353-5faf-48fd-8c76-dfedbeed88ad" />

<img width="2560" height="1440" alt="Screenshot 2026-06-11 211330" src="https://github.com/user-attachments/assets/fa153f00-b480-41e4-917e-29a4cf155b3c" />

<img width="2560" height="1440" alt="Screenshot 2026-06-11 211306" src="https://github.com/user-attachments/assets/c1e72c2b-36e8-447c-bea6-fef756ad787f" />

<img width="1243" height="1207" alt="Screenshot 2026-06-11 211020" src="https://github.com/user-attachments/assets/fbf7334b-e8fa-4425-a693-212c4470a757" />

---

## Step 2: Connecting to the EC2 Instance

After launching the instance, I connected to it using SSH from my terminal.

### Command Used

```bash
ssh -i mykey.pem ubuntu@16.171.55.233
```

### Screenshot

<img width="2560" height="1440" alt="image" src="https://github.com/user-attachments/assets/aec63bb9-0351-4ace-b56b-4aac3482e214" />

---

## Step 3: Creating the MongoDB Atlas Cluster

I created a MongoDB Atlas cluster and configured database access for my application.

### Screenshot

<img width="2560" height="1168" alt="image" src="https://github.com/user-attachments/assets/19de981a-4577-4fff-8a7b-37f0fcca5fd5" />

---

## Step 4: Configuring the Environment Variables

I created a `.env` file containing the MongoDB connection string and application configuration.

### Screenshot

<img width="2560" height="1440" alt="image" src="https://github.com/user-attachments/assets/2767f866-8d9b-49e8-9191-1194f487f919" />

---

## Step 5: Installing Backend Dependencies

I installed all required backend dependencies, including Express, Mongoose, CORS, and dotenv.

### Command Used

```bash
npm install
```

### Screenshot

<img width="2314" height="350" alt="image" src="https://github.com/user-attachments/assets/c044e2e9-a124-42b7-89d9-e433eb9b793e" />

---

## Step 6: Starting the Backend Server

I started the backend application and verified that it connected successfully to MongoDB Atlas.

### Command Used

```bash
node index.js
```

### Screenshot

<img width="2404" height="220" alt="image" src="https://github.com/user-attachments/assets/383da689-87c4-4867-bddf-a7861d21766e" />

---

## Step 7: Testing the Backend API

I tested the API endpoint to ensure that the server was responding correctly.

### Screenshot

<img width="2560" height="1440" alt="image" src="https://github.com/user-attachments/assets/50da0c7f-e95a-429b-880e-f324ad744240" />

---

## Step 8: Installing Frontend Dependencies

I installed the frontend dependencies inside the React application.

### Screenshot

<img width="2554" height="436" alt="image" src="https://github.com/user-attachments/assets/d766935b-073b-402f-acfe-0c872dae53fe" />

---

## Step 9: Running the Frontend Application

I started the React application using Vite and exposed it to external users.

### Command Used

```bash
npm run dev -- --host 0.0.0.0
```

### Screenshot

<img width="2542" height="514" alt="image" src="https://github.com/user-attachments/assets/e4b541b3-4477-4f17-b04f-3c5e03af43cc" />

---

## Step 10: Accessing the Application in the Browser

I opened the application using the EC2 public IP address and verified that the frontend communicated successfully with the backend.

### Screenshot

<img width="2560" height="1440" alt="image" src="https://github.com/user-attachments/assets/7c08f715-8eb8-41a3-8d1e-28c1aed8037a" />

## Conclusion

This project provided me with practical experience in deploying a full MERN stack application on a cloud platform. Throughout the project, I successfully launched and configured an AWS EC2 instance, deployed a Node.js and Express backend, connected the application to MongoDB Atlas, and deployed a React frontend using Vite.

During the deployment process, I encountered several challenges, including API route mismatches, frontend accessibility issues, and security group configuration problems. By troubleshooting these issues and implementing the necessary fixes, I gained a better understanding of cloud infrastructure, application deployment, networking, and full-stack integration.

At the end of the project, I successfully deployed a fully functional Employee Management System that allows users to create, view, and delete employee records. The frontend, backend, and database were successfully integrated and made accessible through the EC2 public IP address.

Overall, this project strengthened my understanding of cloud computing, web application deployment, and real-world DevOps practices, while providing valuable hands-on experience with the MERN technology stack.

