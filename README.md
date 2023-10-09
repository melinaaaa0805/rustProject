<!DOCTYPE html>
<html>

<head>
    <title>Project Documentation</title>
</head>

<body>

    <h1>Project Documentation</h1>

    <h2>Introduction</h2>
    <p>
        This documentation provides instructions for downloading, building, and running the project developed in Rust.
        The project is an HTTP API that returns JSON-formatted request headers when a GET request is made to the "/ping" endpoint.
        Additionally, it handles other HTTP methods by responding with a 404 error and an empty response.
    </p>

    <h2>Prerequisites</h2>
    <p>
        Before you can run the project, make sure you have the following prerequisites installed on your system:
    </p>
    <ul>
        <li>Rust</li>
        <li>Cargo</li>
    </ul>

    <h2>Downloading the Project</h2>
    <p>
        You can download the project from its Git repository using the following command:
    </p>
    <pre><code>git clone &lt;repository-url&gt;</code></pre>
    <p>Replace &lt;repository-url&gt; with the URL of your Git repository.</p>

    <h2>Building the Project</h2>
    <p>
        Navigate to the project directory and use Cargo to build the project:
    </p>
    <pre><code>cd project-directory
cargo build</code></pre>
    <p>This command will compile the project and its dependencies.</p>

    <h2>Configuring the Port</h2>
    <p>
        By default, the project listens on port 8080. You can configure the listening port by setting the PING_LISTEN_PORT
        environment variable. For example, to run the project on port 3030:
    </p>
    <pre><code>export PING_LISTEN_PORT=3030</code></pre>

    <h2>Running the Project</h2>
    <p>
        You can start the project using the following command:
    </p>
    <pre><code>cargo run</code></pre>
    <p>The project will start, and you should see log messages indicating that the server is running.</p>

    <h2>Sending Requests</h2>
    <p>
        To test the API, you can use a tool like curl or a web browser to make GET requests to the following URL:
    </p>
    <pre><code>http://localhost:8080/ping</code></pre>
    <p>Replace 3030 with the port you configured if you changed it.</p>

    <h3>Example using curl</h3>
    <pre><code>curl http://localhost:3030/ping</code></pre>
    <p>You should receive a JSON response containing the request headers.</p>

    <h2>Handling Other HTTP Methods</h2>
    <p>
        The project responds with a 404 error and an empty response for any HTTP method other than GET when making a request
        to the root ("/") endpoint. For example:
    </p>
    <pre><code>curl -X POST http://localhost:8080/</code></pre>

    <h2>Conclusion</h2>
    <p>
        You have successfully downloaded, built, and run the Rust project. You can now interact with the API by sending GET
        requests to the "/ping" endpoint. For any other HTTP method or endpoint, the project will respond with a 404 error.
    </p>

    <p>
        Feel free to customize this documentation with project-specific details and additional information as needed.
    </p>

</body>

</html>
