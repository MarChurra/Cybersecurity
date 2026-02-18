## How Websites work
- When a client browser makes a request to a web server, for a webpage, it will respond with data that your browser uses to show you the page.
- There are two major components that make up a website:
    - Front End (Client-Side) - the way a browser renders a website
    - Back end (Server-Side) - A server that processes your requests and returns a response.
- A website by itself is mainly built by HTML, CSS, Javascript.
- Sensitive Data Exposure occurs when a website does not proerply protect or remove senstitive clear-text information to the end-user, usually found in a site´s frontend source code.
- Sensitive information can be potentially leveraged to further an attacker´s access within different parts of a web application.

## HTML Injection
- A vulnerability that occurs when unfiltered user input is displayed on the page. If a website fails to sanitise user input and that input is used on the page, an attacked can inject HTML code into a vulnerable website.
- Input sanitisation is very important in keeping a website secure, as information a user inputs into a website is often used in other frontend and backend functionality
