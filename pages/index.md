---
title: Get started with ZRA VSDC
description: How to get started with the VSDC API
---

# VSDC API Documentation

{% callout %}
This documentation outlines how developers and third-party vendors can interact with and utilize the VSDC (Virtual Sales Data Controller) API. Built on REST architecture, the VSDC API adheres to REST principles, employing authentication mechanisms, HTTP verbs, and standard response codes. Each API endpoint is documented with its corresponding HTTP method, path, and attribute description.
{% /callout %}

## Audience
The intended audience for this API reference includes users of private Enterprise Resource Planning Systems (ERPs) for managing operations such as accounting, invoicing, and inventory management, and developers and third-party vendors specialized in creating and selling software for creating and managing invoices and inventory operations.

## Environments

The VSDC API provides functionality in two distinct environments: Test and Production. The Test VSDC API is available within a dedicated test environment, referred to as the Sandbox. This environment is designed to facilitate integration testing and development activities without impacting live production data.

The Test VSDC API should access sample data associated with your Taxpayer Identification Number (TPIN) and registered branches. By leveraging this test environment, you can safely validate and test your integration ensuring that your development efforts do not modify or affect actual invoice transactions, customer information, or stock data in the production environment.

Conversely, once the development and testing phases are complete, and the third-party system has been thoroughly validated and deemed ready for live operations, the Production VSDC API is deployed in the production environment. This live environment facilitates seamless integration between the third-party system and the Smart Invoice platform for operational purposes.
    

## Registration 
To access the Test VSDC API , you need to sign up on the [Sandbox Taxpayer Portal](https://sandboxportal.zra.org.zm/basic/login/indexLogin). However, to access the Production VSDC API that handles live transactions, you must first complete development and testing using the Sandbox environment. Once your integration has undergone technical and administrative verification by ZRA to ensure compliance with the set requirements, you can then sign up on the [Smart Invoice Taxpayer Portal](https://siportal.zra.org.zm/basic/login/indexLogin) to start live operations.  

## Authentication
The VSDC API utilizes API keys as a security mechanism to authenticate all requests originating from third-party systems. These unique API keys are generated during the [device initialization](http://localhost:3000) process and stored securely within the VSDC. Each subsequent API request made through the VSDC automatically includes these keys, eliminating the need for developers to manually obtain or append them to any request.


## Data Types
The VSDC API uses data types that are compatible with JSON formatting. When interacting with each endpoint, make sure to strictly follow the prescribed data formats and structures for requests and responses as highlighted in their respective sections.


## Request and Response Bodies
The VSDC API communicates using the JSON data format. When sending requests, you need to structure the data as JSON objects. Similarly, all responses from the API will be encoded in JSON format.


## Relationship and Dependencies
Certain VSDC API endpoints rely on other operations to be completed first, in order to successfully execute the intended transaction or process. For such interdependent endpoints, the documentation will explicitly highlight the prerequisite operations under the respective endpoint section. Developers must ensure that all required preparatory steps are carried out before calling an endpoint that depends on the completion of those prior operations.


## Response Codes
The VSDC API utilizes standard HTTP response codes to communicate API request success or failure. In addition, custom response codes have been added to the JSON response body to indicate the specifics of the API request. Refer to Section 5 the API response codes section for further details.


## Setup your local environment
### Prerequisites
{% callout %}
#### Install Java Development Kit (JDK)
- Ensure that you have the Java Development Kit (JDK) installed on your system. You can download and install the JDK from the official Oracle website or use OpenJDK, which is an open-source implementation of the JDK.

- Set up the JAVA_HOME environment variable to point to the directory where you installed the JDK. Additionally, add the bin directory of the JDK to your system's PATH variable. 

#### Install a Servlet Container or Application Server
You need a servlet container or application server to deploy and run the VSDC WAR file. Recommended options include Apache Tomcat, HTTPD Server, and Eclipse Jetty. Download and install the servlet container or application server of your choice.
{% /callout %}

### Deploy the WAR File
{% callout %}
Copy the WAR file to the appropriate directory within your servlet container or application server. This location may vary depending on the servlet container you are using. Typically, there's a "webapps" directory where you can place your WAR file.
{% /callout %}

### Run the VSDC
{% callout %}
#### Start the Servlet Container or Application Server
Start the servlet container or application server where you deployed the WAR file. This can usually be done by running a startup script or using a command-line interface.

#### Access the Deployed Application
Once the servlet container or application server has started successfully, you can access the deployed application by opening a web browser and navigating to the appropriate URL. The URL will typically include the hostname or IP address of the server, followed by the context path of the application.

### Monitor Logs (Optional)
Monitor the logs of the servlet container or application server for any errors or warnings. These logs can provide valuable information if there are issues with deploying or running the application.
{% /callout %}

## Next steps
- [VSDC Services](http://localhost:3000)
- [Calling your first endpoint](http://localhost:3000)