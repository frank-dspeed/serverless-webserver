# serverless-webserver
Example of a Serverless Webserver using Couchbase

## Concepts
We will run a Simple http2 server without state that simply writes requests to couchbase (Creates a Job) with a ID
then waits for the Job to Complet and returns the response.

the server gets connected to couchbase via websocket api 


## Local Development
docker run -d --name db -p 8091-8094:8091-8094 -p 11210:11210 couchbase
node server.js
node worker.js 
node couchbase-driver.js

when a new job is created via the driver the server will send a message to a registered worker as soon as a worker gets the job he will lock the job and process it and then respond to the server
