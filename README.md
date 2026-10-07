# CST8915 Lab 3: Deploying the Algonquin Pet Store on Azure

**Student Name**: Jane Akinyi Odhiambo
**Student ID**: 041268593
**Course**: CST8915 Full-stack Cloud-native Development
**Semester**: Fall 2026

---

## Demo Video

[Lab 3 Demo Video](https://www.youtube.com/watch?v=0aBSqtx6t8Y)

---

## Service Repositories

- [Order Service](https://github.com/odhi0003/order-service)
- [Product Service](https://github.com/odhi0003/product-service)
- [Store Front](https://github.com/odhi0003/store-front)

---

## Reflection Questions

### 1. What challenges did you encounter when configuring environment variables in the GitHub Actions workflow?

I did not encounter any major challenges when configuring the environment variables in the GitHub Actions workflow. I configured VUE_APP_ORDER_SERVICE_URL and VUE_APP_PRODUCT_SERVICE_URL as variables in the GitHub production environment and referenced them in the workflow using ${{ vars.VUE_APP_ORDER_SERVICE_URL }} and ${{ vars.VUE_APP_PRODUCT_SERVICE_URL }}. The workflow successfully built and deployed the frontend with the correct backend configuration. This also keeps the configuration separate from the application code, following the 12-Factor App configuration third principle.

---

### 2. How does deploying microservices on Azure Web App Service differ from running them locally?

When running microservices locally, I have to start them manually using commands in the terminal and configure their environment variables locally. With Azure Web App Service, Azure manages the hosting environment and provides publicly accessible domains for the backend services. I also had to configure the application settings and environment variables so that the services could communicate correctly in the Azure environment.

---

### 3. Why is it important to use environment variables for configurations in a cloud environment?

Using environment variables is important because it follows the third factor of the 12-Factor App methodology, which states that configuration should be stored in the environment. This allows configuration values such as service URLs to be changed without modifying the application code. It also helps protect sensitive information, such as passwords and connection strings, from being hard-coded and exposed in the source code.