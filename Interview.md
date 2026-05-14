# Important Interview Questions for Nandini Chikkatumbal

---

## Project-Based Questions
## ✅ Introduction

**Good morning,**

My name is **Nandini Narayan Chikkatumbal**. I am a **Java Full-Stack Developer** currently working at **Swajyot Technology, Bangalore**, with around **three year of hands-on professional experience**. I specialize in building applications using **Java Spring Boot, React, and PostgreSQL**.

Along with my professional experience, during my college days I also developed a **Face Mask Detection system** using **Python, OpenCV, Keras, and TensorFlow**, where a real-time camera feed is used to detect faces and classify whether a person is wearing a mask or not 

I have completed my **Bachelor of Engineering** from **KLS VDIT, Haliyal**, and my **Diploma** from **Government Polytechnic, Hubli**.

At present, I am working in swajyot technology pvt ltd am working on a project for **AGI Greenpac Ltd**, a company involved in the manufacturing of packaging solutions such as **glass containers**. In this project, we are developing a system that manages **multiple digital forms with multi-level approval workflows**. After all approvals, the system generates the final output as a **PDF document**, along with **quality inspection and validation checks** before submission.

Previously, I worked on the **Gauge FXS project**, which manages different types of gauges and their **calibration schedules**. The system includes a **calendar-based scheduling module** and automated **email, SMS and WhatsApp notifications using the Twilio service** to remind users about upcoming calibrations.

The application is implemented as a **role-based system** secured using **JWT authentication**, and is developed using **Java Spring Boot, React, and PostgreSQL**.

Coming to my family background, we are four members in our family—my mother and two younger brothers, who are currently pursuing their studies. I am presently based in **Bangalore** for professional purposes.

**Thank you.**
## 1. Explain GageFxs Project

I worked on a system called GageFxs that helps companies manage and track equipment calibration schedules. 

The system tracks when equipment needs calibration, maintains service provider information, and keeps a complete history of all calibrations. It also sends notifications when calibrations are due.

I built the frontend using React and connected it with backend REST APIs. I created dashboards to show calibration data, added search and filtering features, and made sure the interface works well on different screen sizes.

## 2. Explain Headless CMS Website Project

I built a content management website for the Swajyot company using Payload CMS, Next.js, and PostgreSQL.

The system lets administrators add and update website content (like pages, blogs, services, images) without changing any code. Admins can log in, manage content, and control who can access what using role-based permissions.

I handled everything myself - from setting up the database, building APIs, creating the frontend, to deploying it. The website is fast, SEO-friendly, and easy to use.

**Features I built:**
- Dynamic page and blog management
- Image and media management
- Admin dashboard
- User login and permissions
- API design with REST and GraphQL

## 3. Explain AGI Green Pack Project

I built a Document Management System using Spring Boot (backend) and React (frontend).

The system helps companies manage documents and approve them in a structured way. Before, everything was manual and caused delays. Now documents automatically move through approval stages based on who needs to review them.

**Key features:**
- Documents can be uploaded and managed
- Multi-level approval workflow (created by one person, reviewed by manager, approved by admin)
- Only authorized users can see and edit documents
- Document locking prevents two people from editing the same document at the same time
- Forms to capture business data with validations
- Automatic PDF generation for reports

I worked on both backend API development and frontend UI creation.

---

## Technical Questions


## 1. How did you design REST APIs in your projects?

I designed APIs by following REST principles - using proper HTTP methods (GET for reading, POST for creating, PUT for updating, DELETE for removing). 

Each API endpoint represents a resource (like `/documents`, `/users`), and I return proper status codes (200 for success, 404 for not found, 500 for errors).

I also made sure to add pagination for large datasets, validate user input, and document the APIs properly.

## 2. What is RBAC and how did you use it?

RBAC stands for Role-Based Access Control. It means different users have different permissions based on their role (like admin, manager, user).

I implemented it by:
- Creating a roles table in the database (admin, manager, user, etc.)
- Storing user roles in their login token
- Checking the role before allowing access to sensitive operations
- Using role checks in both frontend and backend

## 3. How did you handle PDF generation?

I used a PDF library to create PDF documents. The process is simple:
- Get data from the database
- Create a document structure
- Add the data, tables, and images to the document
- Generate the PDF file
- Send it to the user to download or email

## 4. How do you design a database schema?

I follow normalization principles to keep the database organized:
- Break data into separate tables by topic
- Use relationships between tables to connect data
- Add indexes on columns that are searched frequently
- Avoid storing the same data in multiple places

For the AGI project, I created separate tables for documents, approvals, users, and roles.

## 5. What is the difference between REST and GraphQL?

- **REST**: You have multiple endpoints for different data. Sometimes you get more data than you need (overfetching) or less data than you need (underfetching).
- **GraphQL**: You have one endpoint and ask for exactly what data you need. The client decides what fields to fetch.

I used REST for simple operations and GraphQL for complex data queries where flexibility was needed.

## 6. How did you build responsive dashboards in React?

I used React with CSS frameworks like Tailwind CSS to make responsive UIs.

My approach:
- Design for mobile first, then add larger screens
- Use CSS Grid and Flexbox for flexible layouts
- Test on different screen sizes
- Reuse components to keep code DRY (Don't Repeat Yourself)
- Use React Hooks for managing component state
- Use chart libraries to display data visually

## 7. What is SSR and SSG in Next.js?

- **SSR (Server-Side Rendering)**: The page is built on the server when the user requests it. Good for pages that change frequently and need SEO.
- **SSG (Static Site Generation)**: The page is built once at build time and served to all users. Fast and good for pages that don't change often.

In the CMS project, I used SSG for blog pages (which rarely change) and SSR for admin pages (which show real-time data).

## 8. How do you implement pagination for large datasets?

Pagination shows data in pages instead of loading everything at once.

I use query parameters like `?page=1&limit=10` to tell the backend which page to fetch. The backend calculates how many records to skip, fetches that page, and returns the total count. The frontend shows page numbers for navigation.

This keeps performance fast even with millions of records.

## 9. How did you optimize database performance?

I used several techniques:
- Added indexes on columns that are frequently searched (makes queries faster)
- Used pagination to fetch data in chunks instead of all at once
- Added caching for data that doesn't change often
- Monitored slow queries and optimized them

## 10. What is your approach to code quality?

I follow these practices:
- Write clean, well-documented code
- Keep functions small and focused (do one thing well)
- Use consistent naming conventions
- Use tools to automatically format code (like Prettier)
- Add comments only for complex logic
- Review code with team members before merging

I also use tools like ESLint and Prettier to maintain code quality. sonar as well

## 11. Tell us about your experience building end-to-end projects

In the CMS project, I did everything myself from start to finish:
- Planned the system architecture
- Designed the database
- Built the backend API
- Created the frontend UI
- Set up security and login
- Deployed to production
- Optimized performance

This gave me complete understanding of how all parts work together.

## 12. What was your biggest challenge and how did you solve it?

In the AGI project, the biggest challenge was building an approval workflow that could handle different approval paths for different document types.

I solved it by:
- Creating a flexible workflow engine that reads approval rules from the database
- Using a state machine pattern (each document has a state and can move to the next state)
- Testing with different workflow scenarios
- Storing all rules in the database so they can be changed without code changes

## 13. How do you learn new technologies?

When I started using Payload CMS (a new tool), I:
- Read the official documentation
- Built small test projects to understand features
- Followed online tutorials
- Experimented with different features
- Asked senior developers when stuck
- Applied the knowledge to my real project

## 14. What did you learn from teaching?

I taught Java and Full Stack Development at Besant Technologies. This taught me:
- How to explain complex topics in simple ways
- That different people learn differently - some like examples, some like theory
- The importance of patience and clear communication
- How to mentor and guide junior developers
- It reinforced my own fundamentals

## 15. Why did you choose Java Full Stack development?

I chose this because:
- Java is widely used in companies and has great job opportunities
- Spring Boot makes development fast and productive
- I wanted to work on both backend and frontend (full stack)
- There's always something new to learn in this field
- Companies value full stack developers

---

## Problem-Solving & Design Questions


## 1. How would you fix a slow API?

My approach:
- Monitor the API to see which requests are slow
- Check if the database query is the problem - if yes, add an index or optimize the query
- Check if we're fetching too much data - if yes, use pagination
- Add caching if the data doesn't change often



## 2. What are the main differences between MySQL and PostgreSQL?

| Feature | MySQL | PostgreSQL |
|---------|-------|-----------|
| Data Reliability | Good | Excellent |
| JSON Support | Basic | Advanced |
| Complex Queries | Good | Excellent |
| Free | Yes | Yes |

I chose PostgreSQL for the CMS because it has better support for complex queries and JSON data.


## 3. How do you approach security in applications?

I implement these security measures:
- **Authentication**: Users log in with username and password (password is hashed)
- **Authorization**: Users can only access what their role allows (RBAC)
- **Data Protection**: Encrypt sensitive data both in the database and when sending over internet (HTTPS)
- **Input Validation**: Check all user input to prevent attacks (like SQL injection, XSS)
- **Audit Logs**: Keep records of who did what and when
- **Keep Updated**: Update libraries and dependencies regularly to patch security issues

---

## Career & Growth Questions

## 1. What are your career goals?

**Short term (1-2 years):**
- Get better at system design and architecture
- Learn cloud platforms (AWS, Google Cloud)
- Improve problem-solving skills

**Long term (3-5 years):**
- Become a senior developer
- Lead teams and mentor junior developers
- Contribute to open-source projects
- Build my own products

## 2. How do you stay updated with new technologies?

I stay current by:
- Reading tech blogs and newsletters
- Following trending projects on GitHub
- Taking online courses (Udemy, Coursera)
- Experimenting with new tools in small projects
- Joining tech communities and forums
- Discussing technology with other developers

## 3. What is your biggest weakness and how are you improving?

A good way to answer this:
"I wasn't strong in system design initially. I started reading case studies, solving design problems, and discussing architecture with experienced developers. Now I'm much more comfortable with design decisions."

