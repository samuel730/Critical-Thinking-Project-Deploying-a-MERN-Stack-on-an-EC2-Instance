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

## Backend Deployment

I created and configured the backend using Node.js and Express inside the server directory.

I installed the required dependencies, including Express, Mongoose, CORS, and dotenv.

After that, I:

- Built a REST API to handle employee data
- Created routes for GET, POST, and DELETE operations
- Connected the backend to MongoDB Atlas using a connection string stored in a .env file
- Verified that the server was running successfully on port 5050

The backend was successfully connected to the database and responded correctly to API requests.

---

## Database Setup (MongoDB Atlas)

I created a MongoDB Atlas cluster and configured it as the cloud database for the project.

I connected the cluster to my backend application using Mongoose.

The database stores employee records with the following structure:

- name
- position
- level

The connection was tested and confirmed working during backend startup.

---

## Frontend Deployment

I built the frontend using React with Vite.

I configured the frontend to communicate with the backend using the EC2 public IP address instead of localhost.

I also exposed the frontend server to the internet by running it with:

--host 0.0.0.0

This allowed the application to be accessed externally through the EC2 public IP.

---

## Integration of Full Stack Application

After both the frontend and backend were running, I connected them using HTTP requests.

The frontend communicates with the backend using the following API endpoint:

http://16.171.55.233:5050/employees

This enabled full CRUD functionality between the user interface, backend server, and database.

---

## Challenges I Faced

During the deployment process, I encountered several issues:

- The frontend was not initially accessible due to a missing host configuration
- AWS security group rules were blocking external access to required ports
- API routes were inconsistent at first (/record vs /employees)
- The frontend was initially pointing to localhost instead of the EC2 IP address

---

## How I Solved Them

I resolved these issues by:

- Updating Vite to run with --host 0.0.0.0
- Configuring AWS security groups to allow ports 5050 and 5173
- Standardizing backend routes to /employees
- Replacing localhost URLs with the EC2 public IP

---

## Final Result

At the end of the project, I successfully deployed a working full-stack MERN application on AWS EC2.

The system is fully functional and accessible online.

---

## Live Application Links

Frontend:
http://16.171.55.233:5173

Backend API:
http://16.171.55.233:5050/employees

---

## Conclusion

This project helped me understand real-world cloud deployment, backend development, frontend integration, and database connectivity.

I was able to successfully deploy and connect all components of a full MERN stack application on a live AWS EC2 instance.

---

## Author

Name: Samuel Adesanya  
Project: MERN Stack EC2 Deployment  
Date: June 2026
## Screensots

<img width="1243" height="1207" alt="Screenshot 2026-06-11 211020" src="https://github.com/user-attachments/assets/5be4ba6b-802a-4f47-a8c6-45e3d0af916b" />

<img width="2560" height="1440" alt="Screenshot 2026-06-11 211306" src="https://github.com/user-attachments/assets/38f3056c-6dd1-4ffa-a008-0e1ec8aef3bf" />

<img width="2560" height="1440" alt="Screenshot 2026-06-11 211330" src="https://github.com/user-attachments/assets/43fbef54-7b1d-4982-942a-a329a72cd343" />

<img width="2560" height="1440" alt="Screenshot 2026-06-13 133419" src="https://github.com/user-attachments/assets/e3d39901-338f-4d64-971f-b2c3f56aef46" />

<img width="2560" height="1440" alt="Screenshot 2026-06-12 155811" src="https://github.com/user-attachments/assets/74726012-41bc-413e-a2e6-467ebd83eb6e" />

<img width="2560" height="1440" alt="Screenshot 2026-06-11 220309" src="https://github.com/user-attachments/assets/4529eda9-0fe8-4247-a1f4-7a76f4804105" />

<img width="2560" height="1440" alt="Screenshot 2026-06-11 220257" src="https://github.com/user-attachments/assets/79bdfb05-a149-4d14-aecd-b21b2df47528" />

<img width="2560" height="1440" alt="Screenshot 2026-06-11 220235" src="https://github.com/user-attachments/assets/5f3688ea-c1d3-401e-a7ed-25e0030a3a21" />

<img width="1217" height="118" alt="Screenshot 2026-06-11 211738" src="https://github.com/user-attachments/assets/8873d12e-3f39-45e8-8fa9-dab62d22ff15" />

<img width="867" height="92" alt="Screenshot 2026-06-11 211621" src="https://github.com/user-attachments/assets/8408d733-8472-440e-933c-10f27d5b6ed1" />

<img width="2560" height="1440" alt="Screenshot 2026-06-11 211414" src="https://github.com/user-attachments/assets/09d5871d-4b1e-4d42-b0fc-d6529552a5d9" />

<img width="2560" height="404" alt="Screenshot 2026-06-16 194622" src="https://github.com/user-attachments/assets/0e9ccbd6-f965-44fa-9b02-fb6b57811cfc" />

<img width="2560" height="1440" alt="Screenshot 2026-06-16 194527" src="https://github.com/user-attachments/assets/d9a05dda-b86e-4716-92c2-275b7ea7cb55" />


<img width="2560" height="1440" alt="image" src="https://github.com/user-attachments/assets/79fdfd54-3d78-4d5e-9e26-76db5673e0d7" />

<img width="2560" height="1440" alt="image" src="https://github.com/user-attachments/assets/80992c1b-f976-4e56-bab4-cea8f0802bad" />
