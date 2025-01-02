# Blog management system
This is a microservices based project, that essentially allows user to view and write blogs, kinda similar to Medium. All of the code is containerized and you just need to have `docker` and `docker compose` installed on your machine. Here's how to get started with the project:
- Clone the repository
```bash
git clone --recurse-submodules https://github.com/MohitR1999/portfolio-service.git
```
- Set the environment variables inside each microservice, as follows:
```
JWT_SECRET= <Your preferred JWT secret, keep it same for both services>
PORT=<set it to 5000 for auth service, and 5001 for blog service>
MONGO_INITDB_ROOT_USERNAME=<root username for mongoDB>
MONGO_INITDB_ROOT_PASSWORD=<root password for mongoDB>
MONGO_INITDB_DATABASE=portfolio
ME_CONFIG_MONGODB_ADMINUSERNAME=<admin username for mongoDB>
ME_CONFIG_MONGODB_ADMINPASSWORD=<admin password for mongoDB>
MONGODB_URL=mongodb://<username>:<password>@<mongoDB service name which is present in the docker compose file for each service>:27017/portfolio
ME_CONFIG_BASICAUTH=true
```
- Run the following command for bringing services up:
```bash
docker compose up -d # This will run the containers in detached mode
```
- If you want to hot reload the services after any of them has a change, then run the following command:
```bash
docker compose up --watch # This will run the containers with watch mode enabled
```
- For any suggestions or feature requests, you can raise an issue :)