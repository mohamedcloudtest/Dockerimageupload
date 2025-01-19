<h2><u><b>Docker Image Upload:</b></u></h2>

<h3><u><b>Project Overview:</b></u></h3>

This project automates building and uploading Docker images to Azure Container Registry (ACR) using Azure DevOps pipelines. It demonstrates a CI/CD workflow for a Dockerized application, leveraging Azure services. Specifically, Azure Storage Accounts store application data, Virtual Machines provide compute power for hosting, and Virtual Networks ensure secure communication between resources, enabling efficient and reliable deployment.

<h3><u><b>Tools:</b></u></h3>

- **Terraform**: IaC tool to automate resource provision.
- **Azure**: Used Azure as my cloud platform for deploying and managing resources.
- **Azure DevOps**: CI/CD pipelines.
- **Docker**: Logical container used to containerize the app.
- **AKS (Azure Kubernetes Service)**: Deployed to manage and orchestrate the containerized application.
- **Node.js**: Runtime environment for developing the application.

<h3><u><b>Dockerfile:</b></u></h3>

![Image 17-01-2025 at 20 14](https://github.com/user-attachments/assets/d43e3238-fce4-4064-afa0-6dc2d8206715)


<h3><u><b>Terraform Configuration:</b></u></h3>

![Image 17-01-2025 at 20 12](https://github.com/user-attachments/assets/f8ccb331-a3a5-4d0f-bc6c-af353037f558)





<h3><u><b>Build Pipeline:</b></u></h3>

![Image 17-01-2025 at 19 53](https://github.com/user-attachments/assets/fba3ca80-385f-41d6-99e2-90bf86be6bf9)



<h3><u><b>YAML Script:</b></u></h3>
<img width="1440" alt="image" src="https://github.com/user-attachments/assets/501f73c7-0ed7-40fe-8484-b74e7da4be00" />

<h3><u><b>Summary:</b></u></h3>

Initially, I set up a GitHub repository with my application and Dockerfile, creating and testing the Docker image locally. Once created, I used Terraform to provision Azure resources like Storage Accounts to store app data, Virtual Networks and NSGs to provide secure networking and traffic control, Virtual Machines to host and run the application, and ACR to store and upload the Docker images built from the application.

An Azure DevOps pipeline is created to automate the build and push process. Security best practices, such as using Azure Key Vault, Network Security Groups (NSGs), are also implemented.

<h3><u><b>Conclusion:</b></u></h3>

In conclusion, this project successfully automates the CI/CD pipeline for a Dockerized application using Azure DevOps and various Azure services. Moving forward, I would enhance the project by using **Azure RBAC** for precise access control and **Azure Monitor** for real-time performance tracking. I would also manage multiple Docker containers efficiently by separating the front and back end of the application and would deploy this to a Kubernetes cluster for improved scalability and resource management.
