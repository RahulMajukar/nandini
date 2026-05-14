# Important Interview Questions for Nandini Chikkatumbal

---

## Project-Based Questions

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

## 1. What is Spring Boot and how is it different from Spring Framework?

Spring Boot makes it easier to build Java applications. With Spring Framework, you have to manually configure many things. With Spring Boot, most things are already set up for you automatically. 

Spring Boot comes with an embedded server and reduces boilerplate code, so you can focus on building features faster.

## 2. How did you design REST APIs in your projects?

I designed APIs by following REST principles - using proper HTTP methods (GET for reading, POST for creating, PUT for updating, DELETE for removing). 

Each API endpoint represents a resource (like `/documents`, `/users`), and I return proper status codes (200 for success, 404 for not found, 500 for errors).

I also made sure to add pagination for large datasets, validate user input, and document the APIs properly.

## 3. What is RBAC and how did you use it?

RBAC stands for Role-Based Access Control. It means different users have different permissions based on their role (like admin, manager, user).

I implemented it by:
- Creating a roles table in the database (admin, manager, user, etc.)
- Storing user roles in their login token
- Checking the role before allowing access to sensitive operations
- Using role checks in both frontend and backend

## 4. How did you handle PDF generation?

I used a PDF library to create PDF documents. The process is simple:
- Get data from the database
- Create a document structure
- Add the data, tables, and images to the document
- Generate the PDF file
- Send it to the user to download or email

## 5. How do you design a database schema?

I follow normalization principles to keep the database organized:
- Break data into separate tables by topic
- Use relationships between tables to connect data
- Add indexes on columns that are searched frequently
- Avoid storing the same data in multiple places

For the AGI project, I created separate tables for documents, approvals, users, and roles.

## 6. What is the difference between REST and GraphQL?

- **REST**: You have multiple endpoints for different data. Sometimes you get more data than you need (overfetching) or less data than you need (underfetching).
- **GraphQL**: You have one endpoint and ask for exactly what data you need. The client decides what fields to fetch.

I used REST for simple operations and GraphQL for complex data queries where flexibility was needed.

## 7. How did you build responsive dashboards in React?

I used React with CSS frameworks like Tailwind CSS and Bootstrap to make responsive UIs.

My approach:
- Design for mobile first, then add larger screens
- Use CSS Grid and Flexbox for flexible layouts
- Test on different screen sizes
- Reuse components to keep code DRY (Don't Repeat Yourself)
- Use React Hooks for managing component state
- Use chart libraries to display data visually

## 8. What is SSR and SSG in Next.js?

- **SSR (Server-Side Rendering)**: The page is built on the server when the user requests it. Good for pages that change frequently and need SEO.
- **SSG (Static Site Generation)**: The page is built once at build time and served to all users. Fast and good for pages that don't change often.

In the CMS project, I used SSG for blog pages (which rarely change) and SSR for admin pages (which show real-time data).

## 9. How do you implement pagination for large datasets?

Pagination shows data in pages instead of loading everything at once.

I use query parameters like `?page=1&limit=10` to tell the backend which page to fetch. The backend calculates how many records to skip, fetches that page, and returns the total count. The frontend shows page numbers for navigation.

This keeps performance fast even with millions of records.

## 10. How did you optimize database performance?

I used several techniques:
- Added indexes on columns that are frequently searched (makes queries faster)
- Used pagination to fetch data in chunks instead of all at once
- Added caching for data that doesn't change often
- Avoided N+1 query problems (fetching data in a loop - instead fetch all at once)
- Monitored slow queries and optimized them

## 11. How did you handle multiple users editing at the same time?

When multiple users try to edit the same document, conflicts can happen. I prevented this by:
- Locking documents when someone is editing them (only one person can edit at a time)
- Using version control to track document changes
- Keeping audit logs of who changed what and when
- Managing transactions in the database to keep data consistent

## 12. Tell us about your experience building end-to-end projects

In the CMS project, I did everything myself from start to finish:
- Planned the system architecture
- Designed the database
- Built the backend API
- Created the frontend UI
- Set up security and login
- Deployed to production
- Optimized performance

This gave me complete understanding of how all parts work together.

## 13. What was your biggest challenge and how did you solve it?

In the AGI project, the biggest challenge was building an approval workflow that could handle different approval paths for different document types.

I solved it by:
- Creating a flexible workflow engine that reads approval rules from the database
- Using a state machine pattern (each document has a state and can move to the next state)
- Testing with different workflow scenarios
- Storing all rules in the database so they can be changed without code changes

## 14. How do you learn new technologies?

When I started using Payload CMS (a new tool), I:
- Read the official documentation
- Built small test projects to understand features
- Followed online tutorials
- Experimented with different features
- Asked senior developers when stuck
- Applied the knowledge to my real project

## 15. What did you learn from teaching?

I taught Java and Full Stack Development at Besant Technologies. This taught me:
- How to explain complex topics in simple ways
- That different people learn differently - some like examples, some like theory
- The importance of patience and clear communication
- How to mentor and guide junior developers
- It reinforced my own fundamentals

## 16. Why did you choose Java Full Stack development?

I chose this because:
- Java is widely used in companies and has great job opportunities
- Spring Boot makes development fast and productive
- I wanted to work on both backend and frontend (full stack)
- There's always something new to learn in this field
- Companies value full stack developers

---

## Problem-Solving & Design Questions

## 17. How would you design a scalable document management system?

To build a scalable system, I would consider:

**Database**: Use PostgreSQL for reliable data storage and complex queries

**Storage**: Use cloud storage (like AWS S3) for document files, not the database

**Speed**: Add caching layer (Redis) for frequently accessed documents

**Security**: Encrypt documents, control who can access what, keep audit logs

**Performance**: Add indexes, use pagination, process heavy tasks in the background

**Reliability**: Keep backups, have disaster recovery plan, monitor the system

**Scaling**: Use load balancing to handle many users at once

## 18. How would you fix a slow API?

My approach:
- Monitor the API to see which requests are slow
- Check if the database query is the problem - if yes, add an index or optimize the query
- Check if we're fetching too much data - if yes, use pagination
- Check if we're doing N+1 queries (loops with database calls) - if yes, optimize to fetch all data at once
- Add caching if the data doesn't change often
- If the API has too much traffic, use load balancing to distribute requests

## 19. What is your approach to code quality?

I follow these practices:
- Write clean code with clear variable names
- Keep functions small and focused (do one thing well)
- Don't repeat code - use functions and components
- Write tests for important logic
- Review code with team members before merging
- Use tools to automatically format code
- Add comments only for complex logic

## 20. What are the main differences between MySQL and PostgreSQL?

| Feature | MySQL | PostgreSQL |
|---------|-------|-----------|
| Data Reliability | Good | Excellent |
| JSON Support | Basic | Advanced |
| Complex Queries | Good | Excellent |
| Free | Yes | Yes |

I chose PostgreSQL for the CMS because it has better support for complex queries and JSON data.

## 21. Explain your Git workflow

We used a simple branching strategy:
- **main** branch: Production code (deployed code)
- **develop** branch: Testing code (where features come together)
- **feature branches**: For building new features (e.g., `feature/user-login`)
- **bugfix branches**: For fixing bugs (e.g., `bugfix/login-error`)

Before merging, we review the code and make sure it works. Commit messages clearly explain what changed.

## 22. How do you approach security in applications?

I implement these security measures:
- **Authentication**: Users log in with username and password (password is hashed)
- **Authorization**: Users can only access what their role allows (RBAC)
- **Data Protection**: Encrypt sensitive data both in the database and when sending over internet (HTTPS)
- **Input Validation**: Check all user input to prevent attacks (like SQL injection, XSS)
- **Audit Logs**: Keep records of who did what and when
- **Keep Updated**: Update libraries and dependencies regularly to patch security issues

---

## Career & Growth Questions

## 23. What are your career goals?

**Short term (1-2 years):**
- Get better at system design and architecture
- Learn cloud platforms (AWS, Google Cloud)
- Improve problem-solving skills

**Long term (3-5 years):**
- Become a senior developer
- Lead teams and mentor junior developers
- Contribute to open-source projects
- Build my own products

## 24. How do you stay updated with new technologies?

I stay current by:
- Reading tech blogs and newsletters
- Following trending projects on GitHub
- Taking online courses (Udemy, Coursera)
- Experimenting with new tools in small projects
- Joining tech communities and forums
- Discussing technology with other developers

## 25. What is your biggest weakness and how are you improving?

A good way to answer this:
- Choose a real weakness (not a strength disguised as weakness)
- Explain why it matters
- Show concrete steps you're taking to improve
- Example: "I wasn't strong in system design initially. I started reading case studies, solving design problems, and discussing architecture with experienced developers. Now I'm much more comfortable with design decisions."

---

## Additional Technical Skills

## 26. What state management solutions have you used?

I've used:
- **React Hooks**: useState and useContext for managing component state
- **Context API**: For sharing data across multiple components
- **Custom Hooks**: For reusing logic across components

These solutions work well for most projects without needing extra libraries.

## 27. How do you handle API errors?

Error handling approach:
- Use try-catch blocks to catch errors
- Return proper error codes from the backend (400 for bad input, 500 for server errors)
- Validate input on both frontend and backend
- Show user-friendly error messages (not technical details)
- Log errors for debugging and monitoring

## 28. What tools have you used for version control and deployment?

- **Git**: For version control (track code changes)
- **GitHub**: For code repository and collaboration
- **Linux Command Line**: For server management
- **Deployment**: Understanding of deployment processes (deploying code to production)
- **CI/CD**: Understanding of automated testing and deployment pipelines

