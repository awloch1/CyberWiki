 Burp Suite captures and enables manipulation of all the HTTP/HTTPS traffic between a browser and a web server.
 Features:
 - **Proxy** - It enables interception and modification of requests and responses while interacting with web applications.
 - **Repeater** - allows for capturing, modifying, and resending the same request multiple times.
 - **Intruder** - automates sending many modified requests to an endpoint, useful for **fuzzing, parameter testing, brute-force testing, and discovering how an application responds to different payloads**.
- **Collaborator**(Pro version)- detects when the target server makes an external DNS/HTTP request, which is useful for finding **blind vulnerabilities**.

##### Burp Suite Session Management
- **Session handling** – controls how Burp manages and maintains an authenticated session, for example by refreshing tokens, updating cookies, or re-authenticating when needed.
- **Cookie jar** – stores cookies collected by Burp, such as `session`, `PHPSESSID`, or `JSESSIONID`, so they can be reused in later requests.
- **Macros** – saved sequences of requests that Burp can run automatically, for example: `GET login page → POST credentials → obtain a new session cookie`

##### Vulnerabilities in other authentication mechanisms
- **Keeping users logged in**
- **Resetting user passwords**
- **Changing user passwords**
