# 🚀 Node.js Interview Questions

## 📌 Node.js Fundamentals

1. What is Node.js?
2. Why do we use Node.js?
3. How does Node.js work?
4. What are the features of Node.js?
5. What is the difference between Node.js and JavaScript?
6. What is the difference between Node.js and a browser?
7. What is the V8 Engine?
8. What is npm?
9. What is npx?
10. What is package.json?
11. What is package-lock.json?
12. What is the difference between dependencies and devDependencies?
13. What is semantic versioning (SemVer)?
14. What is CommonJS?
15. What are ES Modules (ESM)?
16. Difference between CommonJS and ES Modules?
17. What is REPL in Node.js?

---

## 📌 Event Loop & Async Programming

18. What is the Event Loop?
19. How does Node.js handle multiple requests?
20. What is asynchronous programming?
21. Difference between synchronous and asynchronous code?
22. What are callbacks?
23. What is callback hell?
24. How do Promises solve callback hell?
25. What are async/await?
26. Difference between Promise.all(), Promise.allSettled(), Promise.race(), and Promise.any()?
27. What are microtasks and macrotasks?
28. What is process.nextTick()?
29. What is setImmediate()?
30. Difference between setTimeout() and setImmediate()?
31. What happens when an exception occurs inside async code?

---

## 📌 Node.js Architecture

32. Explain Node.js architecture.
33. Why is Node.js single-threaded?
34. Is Node.js really single-threaded?
35. What is libuv?
36. What is the thread pool?
37. How can CPU-intensive tasks affect Node.js?
38. How can we handle CPU-intensive tasks?
39. What are Worker Threads?
40. Difference between Worker Threads and Child Processes?
41. What is clustering?
42. Difference between Cluster and Worker Threads?

---

## 📌 Modules

43. What are modules?
44. How do you create your own module?
45. What are built-in modules?
46. What is module caching?
47. How does require() work?
48. How does import/export work?

---

## 📌 File System (fs)

49. What is the fs module?
50. Difference between synchronous and asynchronous file operations?
51. How do you read a file?
52. How do you write a file?
53. How do you append data to a file?
54. How do you delete a file?
55. How do you rename a file?
56. What are Streams?

---

## 📌 Streams & Buffers

57. What are Streams?
58. Types of Streams?
59. What is a Buffer?
60. Difference between Streams and Buffers?
61. What is piping?
62. How do Streams improve performance?

---

## 📌 HTTP Module

63. What is the HTTP module?
64. How do you create an HTTP server?
65. Difference between HTTP and HTTPS?
66. What are request and response objects?
67. How do you send JSON responses?

---

## 📌 Express.js

68. What is Express.js?
69. Why use Express instead of the HTTP module?
70. How do you create routes?
71. What is middleware?
72. Types of middleware?
73. How do you handle errors in Express?
74. What is express.json()?
75. What is express.urlencoded()?
76. Difference between app.use() and app.get()?
77. What is Router in Express?
78. What is next()?

---

## 📌 REST APIs

79. What is REST?
80. What are REST principles?
81. Difference between PUT and PATCH?
82. Difference between POST and PUT?
83. Common HTTP status codes?
84. What are CRUD operations?
85. How do you validate request data?

---

## 📌 Authentication & Security

86. What is JWT?
87. How does JWT work?
88. What is session-based authentication?
89. Difference between JWT and Sessions?
90. What is Passport.js?
91. What is bcrypt?
92. Why hash passwords?
93. What is CORS?
94. What is CSRF?
95. What is XSS?
96. How do you secure a Node.js application?
97. What is Helmet.js?
98. What is Rate Limiting?

---

## 📌 Database

99. How do you connect Node.js with a database?
100. Difference between SQL and NoSQL?
101. What is connection pooling?
102. What is an ORM?
103. Difference between ORM and Query Builder?
104. What is Drizzle ORM?
105. What are migrations?
106. Why are migrations needed?
107. What are transactions?

---

## 📌 Error Handling

108. Difference between try/catch and .catch()?
109. What are custom errors?
110. How do you handle uncaught exceptions?
111. What is unhandled promise rejection?
112. Difference between operational errors and programmer errors?

---

## 📌 Performance

113. How do you improve Node.js performance?
114. What is caching?
115. What is Redis?
116. Why use compression?
117. How do Streams improve memory usage?
118. How do you monitor memory leaks?
119. What causes memory leaks?

---

## 📌 Process Module

120. What is process?
121. What is process.env?
122. What is process.exit()?
123. What is process.cwd()?
124. What is process.argv()?

---

## 📌 Child Processes

125. What are Child Processes?
126. Difference between exec() and spawn()?
127. Difference between fork() and spawn()?

---

## 📌 Events

128. What is EventEmitter?
129. How do you create custom events?
130. Difference between EventEmitter and callbacks?

---

## 📌 Testing

131. What testing frameworks have you used?
132. What is Jest?
133. What is unit testing?
134. What is integration testing?
135. How do you mock dependencies?

---

## 📌 Deployment

136. How do you deploy a Node.js application?
137. What is PM2?
138. Why use Nginx with Node.js?
139. What is Docker?
140. Environment variables in production?

---

## 📌 Advanced Topics

141. What is Event-Driven Architecture?
142. What are Message Queues?
143. What is RabbitMQ?
144. What is Kafka?
145. What are WebSockets?
146. Difference between WebSockets and HTTP?
147. What is Socket.IO?
148. What are Server-Sent Events (SSE)?
149. What is GraphQL?
150. Difference between GraphQL and REST?

---

## 📌 Scenario-Based Questions

151. Why is your Node.js application slow?
152. How would you handle one million requests?
153. How would you upload large files?
154. How would you build a real-time chat application?
155. How would you design a notification system?
156. How would you implement authentication?
157. How would you prevent duplicate API requests?
158. How would you improve API response time?
159. How would you debug memory leaks?
160. How would you scale a Node.js application?

---

# ⭐ Most Frequently Asked (Must Prepare)

- What is Node.js?
- How does Node.js work?
- Explain the Event Loop.
- What is libuv?
- What is V8 Engine?
- Difference between synchronous and asynchronous programming.
- Callbacks vs Promises vs Async/Await.
- process.nextTick() vs setImmediate().
- Streams and Buffers.
- EventEmitter.
- Express Middleware.
- Authentication using JWT.
- Sessions vs JWT.
- CORS.
- REST API principles.
- SQL vs NoSQL.
- Migrations.
- Worker Threads.
- Child Processes.
- Clustering.
- Node.js Architecture.
- How does Node.js achieve concurrency?
- CommonJS vs ES Modules.
- Module Caching.
- Error Handling.
- Performance Optimization.
- Memory Leaks.
- PM2.
- Docker.
- WebSockets.
