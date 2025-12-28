# Client–Server Model and Full-Stack Applications

Modern financial applications are built using the **client–server model**, where responsibilities are cleanly divided to ensure scalability, security, and reliability. This model forms the backbone of web-based FinTech platforms.

A **client** is the user-facing part of an application, such as a web browser or mobile app. It is responsible for collecting user input and displaying results. In a FinTech UI, the client might allow a user to enter a stock symbol or cryptocurrency name and initiate a search. The client does not store sensitive data or perform critical financial logic.

A **server** is a program running on a remote machine that handles application logic. It receives requests from clients, validates inputs, applies business rules, fetches data, and sends structured responses back. In FinTech systems, the server is where pricing logic, validation, and security checks are enforced.

When a user clicks **“Search”** in the UI, the client sends a request to the server containing the user’s input. The server processes this request, retrieves the required data from storage or other sources, and sends the result back to the client. The client then updates the interface to display the information.

A **full-stack application** consists of three main layers: the frontend, backend, and database. The frontend is the client-side interface that users interact with. The backend is the server-side logic that processes requests. The database stores persistent data such as market information or user records. These layers communicate through **APIs**, which define how data is requested and returned in a structured and secure way.

The flow of data in a typical application follows a simple path: the client sends a request to the server, the server interacts with the database if needed, and the processed response is sent back to the client. Keeping these layers separate is essential for building robust and scalable FinTech systems.

<img width="1500" height="1144" alt="image" src="https://github.com/user-attachments/assets/adf60e95-fc34-4787-a0a3-7785f69772fc" />

### Flow Summary:
1. Client sends a request (Search action)
2. Server processes the request
3. Server queries the database
4. Database returns data
5. Server sends processed data to client
6. Client displays results
