# MPA_Node_Express_Serverless_Example

# Brief Introduction

MAP stands for "Multi page application".
This respository introduces this new concept 'MPA' with AWS lambda function.

# Notion Documentation

[Document](https://www.notion.so/Running-Node-Express-Apps-via-Lambda-API-Gateway-737f87966c784c23a1314b14a53b2038)

# Running Node/Express Apps via Lambda + API Gateway

[https://github.com/awslabs/aws-serverless-express](https://github.com/awslabs/aws-serverless-express)

```bash
npm install aws-serverless-express
```

- Create lambda.js in the root folder of your project

```jsx
'use strict'
const awsServerlessExpress = require('aws-serverless-express')
const app = require('./app')
const server = awsServerlessExpress.createServer(app)

exports.handler = (event, context) => awsServerlessExpress.proxy(server, event, context)
```

### Steps to be taken

1. compress files (node express project)
2. Create a new function (Author from scratch)
3. Upload a .zip file 
4. Set `any` method with Lambda proxy
5. Create a new resource with Lambda proxy


# Pros and Cons of Serverless Node/Express MPA

### Issues

- Statless Application
- Working with files is almost impossible
- Managing session isn't possible
- It doesn't behave like normal node.js application

# Learn more about AWS Serverless + Express Apps

If you want to dive deeper into serverless MPAs powered by Express, these resources should be helpful:

- AWS Blog: Migrating your Express App to Lambda: [https://aws.amazon.com/blogs/compute/going-serverless-migrating-an-express-application-to-amazon-api-gateway-and-aws-lambda/](https://aws.amazon.com/blogs/compute/going-serverless-migrating-an-express-application-to-amazon-api-gateway-and-aws-lambda/)
- Express Wrapper (Github): [https://github.com/awslabs/aws-serverless-express](https://github.com/awslabs/aws-serverless-express)