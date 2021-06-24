# golang
Description:
This is a simple rest service which has a POST method and a GET method. It can post any json payload and will return POST done as response. The Get method returns the same json payload with timestamp.

Deployment in Cloud Run:
While deploying this service in cloud run, we were getting the below error:
Deployment failed
ERROR: (gcloud.run.deploy) Cloud Run error: Container failed to start. Failed to start and then listen on the port defined by the PORT environment variable. Logs for this revision might contain more information.

For fixing this error, we had to update the port using the below command:
gcloud run services update test-rest-service --port 8090

But this is a temporary solution. We are working on a permanent fix for this issue.
