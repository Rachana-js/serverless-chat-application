# serverless-chat-application
# Project Setup

Prerequisites
1)AWS account with free tier access.
2)Node.js or Python installed on your system for Lambda development.
3)Postman for testing WebSocket APIs.

Steps
1)Clone the repository:
git clone https://github.com/Rachana-js/serverless-chat-application.git
cd serverless-chat-application

2)Set up AWS resources:
-->Create a WebSocket API in API Gateway with routes for $connect, $disconnect, and sendmessage.
-->Deploy the provided Lambda functions.
-->Create a DynamoDB table for connection details.

3)Configure environment variables:

Update Lambda functions with WEBSOCKET_TABLE and other required settings.
Deploy the API: Use the AWS Management Console to deploy the API and test connectivity.


Testing the Application
-->Open Postman or a WebSocket client.
-->Connect to the WebSocket URL:
        wss://<api-id>.execute-api.<region>.amazonaws.com/<stage>

Test the following actions:
-->Connect: Establish a WebSocket connection.
-->Send a message:
    {
      "action": "sendmessage",
      "message": "Hello, AWS!"
    }
-->Disconnect: Close the WebSocket connection.
