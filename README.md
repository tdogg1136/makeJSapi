# JavaScript Code Executor

This project enables you to execute JavaScript code on a remote server using a secure token-based authentication mechanism. The server utilizes Express.js to handle incoming POST requests containing JavaScript code, evaluates the code, and returns the result.

## How to Execute Code

Follow these steps to deploy and test the JavaScript Code Executor:

### Deployment

1. **Clone the Repository**: Take this GitHub repository URL and head to [Render](https://render.com/).
2. **Setup Blueprint**: Within Render, navigate to Blueprints and add the public repository URL.
3. **Configure Token**: Set a secure token and ensure it's at least 24 characters long.
4. **Deploy**: Spin up the server and wait until the deployment is complete.

### Testing with Postman

1. **Login to Postman**: Head to [Postman](https://postman.com/) and log in or create an account.
2. **Create a New Request**: Create a new POST request and add your deployed server URL.
3. **Set Endpoint**: Append the path `/execute` to your server URL. The request URL should look like this: `https://javascript-api-xxx.onrender.com/execute`.
4. **Configure Authorization**:
   - Go to the Authorization tab.
   - Select "API Key".
   - Set the key as `Authorization` and the value as your secure token.
   - Choose "Header" as the key's location.
5. **Prepare Payload**:
   - Navigate to the Body tab.
   - Select "raw" and set the content type to "text/plain".
6. **Add JavaScript Code**: Insert the following code into the payload:
   ```javascript
   // Hello World function
   const helloWorld = () => {
       const greeting = "Hello, World!";
       return greeting;
   };

   // Call the helloWorld function and store the result
   const result = helloWorld();

   // Output the result
   result; // Should return "Hello, World!"
   ```
7. **Send Request:** Send the request and you will receive the "Hello, World!" response.