<p><a href="/">home</a> / <a href="/guides">guides</a></p>
<div class="rainbow-retro"></div>

<h1>API Gateways</h1>

Most API flow is often going to first hit the gateway APIs which acts as the "front door" for applications to access data, business logic, or functionality from your backend services. Traffic is routed to the other APIs in an ecosystem, this can be AWS kinesis events, websockets, or regular old HTTP REST requests.  

There are many managed tools which will be mentioned in this document which add perspective around what options one would have in 2022 if starting out to make an API Gateway. 

Depending on which design strategy instrastructure and hosting provider you have there may be certain paradigms you are locked into and need to use. Examples of such are serverless and lambdas using mostly [AWS API Gateway](https://aws.amazon.com/api-gateway/), Kubernetes with a slightly different implimdentation of the [gateway in GKE](https://cloud.google.com/kubernetes-engine/docs/concepts/gateway-api) than [AWS's EKS](https://aws.amazon.com/blogs/containers/integrate-amazon-api-gateway-with-amazon-eks/).  

## Serverless API Gateway with AWS

![Example AWS API Gateway Diagram](https://d1.awsstatic.com/serverless/New-API-GW-Diagram.c9fc9835d2a9aa00ef90d0ddc4c6402a2536de0d.png)

Above is how we would expect the hosted solution for a base serverless implimentation. After hitting the gateway in a small example below we can expect the invocation of a lambda function to process the business logic. 

In the below example we have a small api which is returning a "helloworld" when a HTTP GET request is made on Port 80/8080. 


```js
//js api example code

```

We deploy this first lambda 

## Deploy the lambda in AWS console

// TODO: step 1 images for creating roles / and lambda deploy 

// TODO: step 2 images for setup apigateway 



## Set up an edge-optimized API using AWS CLI commands

Using the [apigateway](https://docs.aws.amazon.com/cli/latest/reference/apigateway/index.html) command, we are able to setup and provision the apigateway with the set of instructions above using the commands below: 

 Call the create-rest-api command to set up the REST API in a specific region (us-east-1). 
 
```bash
aws apigateway create-rest-api --name 'Simple Helloworld (AWS CLI)' --region us-east-1
```

The following is the output of this command:

```json
{
    "name": "Simple Helloworld (AWS CLI)", 
    "id": "xxxxxxxav7", 
    "createdDate": 1660927892
}
```
Note the returned id of the newly created RestApi. You need it to set up other parts of the API.

Call the get-resources command to retrieve the root resource identifier of the REST API. 

```bash
aws apigateway get-resources --rest-api-id xxxxxxxav7 --region us-east-1
```

The following is the output of this command:

```json
{
    "items": [
        {
            "path": "/", 
            "id": "bebolt24fg"
        }
    ]
}
```

Note the root resource Id. You need it to start setting the API's resource tree and configuring methods and integrations.

Call the create-resource command to append a child resource (test) under the root resource (bebolt24fg):

```
aws apigateway create-resource --rest-api-id xxxxxxxav7 \
      --region us-east-1 \
      --parent-id bebolt24fg \
      --path-part test
```

The following is the output of this command:

```json
{
    "path": "/test", 
    "pathPart": "test", 
    "id": "xxxxb4", 
    "parentId": "bebolt24fg"
}
```
 
<p class="spacers"> <br /></p>
<div align="center" >
  <p>
    <a href="https://beau.sh/guides/">⬅️ Back to Guides</a>
  </p>
</div>
