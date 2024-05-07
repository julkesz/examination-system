# Examination system
Java Spring Boot application for creating, writing and grading online exams.

## Description
The task of the module is to enable the assessment of students' work and conduct examinations electronically. The functionality related to projects and assignments allows for the submission and evaluation of projects and other student work. The system stores and provides current information on students' progress, including grades from passed subjects and all assignments, tests and projects. An important feature are electronic exams. The system allows for exam organization, including determining participants and exam questions/tasks. From the prepared tasks, the system assigns questions/tasks to individual students based on rules defined by the teacher (e.g., according to the number of points, topics, type of tasks – for example: each student receives 5 questions worth 2 points, 4 questions worth 5 points, and 2 tasks worth 10 points, with each question from a different topic).

Grading is automated as mush as possible: for closed tasks, the scoring is determined by the system, while for open tasks, there is an option for the instructor to input a grade and write a comment. Information about results and study progress is appropriately protected and accessible to interested parties – students and instructors.

- The designed system is a Single Page Application (SPA) web application based on a **three-tier architecture** (client-server). The server handles the main logic of the system: handling client requests, generating reports, delivering, and storing data. The server-side layer is created using the **Spring framework**.
- The communication model between the client-side and server-side is based on the **REST** (Representational State Transfer) style. Communication occurs using the HTTP(S) protocol and typical methods for this protocol: GET, POST, PUT, DELETE. Messages are transmitted in JSON format.
- Data access implementation is carried out using an Object-Relational Mapping (ORM) library - **Spring Data JPA**. The data layer consists of a relational **PostgreSQL** database.
- **Spring Security** is used to authenticate users. Once authenticated, the web application attaches an **JSON Web Token (JWT)** containing the user’s identity and attributes to every request sent to the /api/ endpoint. Requests that require authentication are intercepted by the security filter, which can verify the token and make its properties available to the request.

## Getting started
### Dependencies
Backend:
- Java 17 SDK
- Gradle

Frontend:
- Next.js

### Running the application locally
1. Go to ./backend and start the application using Gradle:
```
./gradlew bootRun
```
2. In the other terminal, go to ./frontend and start it using npm, yarn or pnpm:
```
npm run dev
# or
yarn dev
# or
pnpm dev
```
3. Open http://localhost:4000 with your browser to see the result.
4. To log in as a teacher, type: email: teacher@gmail.com and password: password
5. To log in as a student, type: email: student@gmail.com and password: password
