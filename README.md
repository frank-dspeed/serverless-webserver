# serverless-webserver
Example of a Serverless Webserver using Couchbase

## Concepts
We will run a Simple http2 server without state that simply writes requests to couchbase (Creates a Job) with a ID
then waits for the Job to Complet and returns the response.

the server gets connected to couchbase via websocket api 
