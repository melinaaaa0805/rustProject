#Project Documentation
Introduction
This documentation provides instructions for downloading, building, and running the project developed in Rust. The project is an HTTP API that returns JSON-formatted request headers when a GET request is made to the "/ping" endpoint. Additionally, it handles other HTTP methods by responding with a 404 error and an empty response.

#Prerequisites
Before you can run the project, make sure you have the following prerequisites installed on your system:

-Rust
-Cargo
-Downloading the Project
You can download the project from its Git repository using the following command:

bash

git clone <repository-url>
Replace <repository-url> with the URL of your Git repository.

Building the Project
Navigate to the project directory and use Cargo to build the project:

bash

cd project-directory
cargo build
This command will compile the project and its dependencies.

Configuring the Port
By default, the project listens on port 8080. You can configure the listening port by setting the PING_LISTEN_PORT environment variable. For example, to run the project on port 3030:

bash

export PING_LISTEN_PORT=8080
Running the Project
You can start the project using the following command:

bash

cargo run
The project will start, and you should see log messages indicating that the server is running.

Sending Requests
To test the API, you can use a tool like curl or a web browser to make GET requests to the following URL:

bash

http://localhost:8080/ping
Replace 3030 with the port you configured if you changed it.

Example using curl
bash

curl http://localhost:8080/ping
You should receive a JSON response containing the request headers.

#Handling Other HTTP Methods
The project responds with a 404 error and an empty response for any HTTP method other than GET when making a request to the root ("/") endpoint. For example:

bash

curl -X POST http://localhost:8080/
Conclusion
You have successfully downloaded, built, and run the Rust project. You can now interact with the API by sending GET requests to the "/ping" endpoint. For any other HTTP method or endpoint, the project will respond with a 404 error.

Feel free to customize this documentation with project-specific details and additional information as needed.
