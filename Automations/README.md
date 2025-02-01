## Running Kubernetes in Docker (kind)

If you are running Kubernetes in Docker using `kind`, follow these steps to retrieve the Docker container IP and update the environment files:

Environment files exists in the directory

```/backend/.env.docker && /frontend/.env.docker```

### Step 1: Get the Docker Container IP
Run the following command to get the IP address of your `kind` container:

```bash
docker inspect -f '{{range.NetworkSettings.Networks}}{{.IPAddress}}{{end}}' <docker-container-id/name>
```
if you are using kind, remove following jenkin stage
"stage('Exporting environment variables')"



