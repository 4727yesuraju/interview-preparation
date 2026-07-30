# 📚 Cookies vs Local Storage vs Session Storage

## 📖 Simple English Explanation

All three are used to **store data in the browser**, but they differ in **storage size, lifetime, and how they are used**.

- **Cookies** → Small data stored by the browser. Sent to the server with every HTTP request.
- **Local Storage** → Stores data permanently (until manually removed).
- **Session Storage** → Stores data only for the current browser tab.

> **Simple Definition:**
>
> - **Cookies** → Small data sent to the server with every request.
> - **Local Storage** → Persistent browser storage.
> - **Session Storage** → Temporary storage for one browser tab.

---

## 🤔 Why is it Needed?

### Cookies

- Store login sessions.
- Authentication.
- User preferences.

### Local Storage

- Store data permanently.
- Save theme preferences.
- Cache application data.

### Session Storage

- Store temporary data.
- Multi-step forms.
- Shopping cart during one session.

---

## 🌊 Flow

```text
User Visits Website
        │
        ▼
Need to Store Data?
        │
        ├───────────────┬─────────────────┐
        ▼               ▼                 ▼
Cookies        Local Storage      Session Storage
        │               │                 │
Sent to Server   Stored in Browser  Stored Per Tab
        │               │                 │
Expires          Until Deleted      Until Tab Closes
```

---

## ✍️ Syntax

### Cookies

```javascript
document.cookie = "username=John";
```

---

### Local Storage

```javascript
localStorage.setItem("name", "John");

const name = localStorage.getItem("name");

localStorage.removeItem("name");
```

---

### Session Storage

```javascript
sessionStorage.setItem("name", "John");

const name = sessionStorage.getItem("name");

sessionStorage.removeItem("name");
```

---

## 💻 Example

### Cookies

```javascript
document.cookie = "theme=dark";
```

The browser stores:

```text
theme=dark
```

This cookie is sent with future HTTP requests to the same website (if applicable).

---

### Local Storage

```javascript
localStorage.setItem("theme", "dark");

console.log(localStorage.getItem("theme"));
```

**Output**

```text
dark
```

Even after refreshing or reopening the browser, the value remains until it is removed.

---

### Session Storage

```javascript
sessionStorage.setItem("username", "John");

console.log(sessionStorage.getItem("username"));
```

**Output**

```text
John
```

If you close the tab, the data is removed.

---

## 📋 Comparison

| Feature                  | Cookies                                     | Local Storage                 | Session Storage              |
| ------------------------ | ------------------------------------------- | ----------------------------- | ---------------------------- |
| Storage Size             | ~4 KB                                       | ~5–10 MB (browser dependent)  | ~5–10 MB (browser dependent) |
| Sent to Server           | ✅ Yes                                      | ❌ No                         | ❌ No                        |
| Expiry                   | Configurable                                | Until removed                 | Until tab closes             |
| Shared Across Tabs       | ✅ Yes (same site, subject to cookie rules) | ✅ Yes (same origin)          | ❌ No                        |
| Accessible by JavaScript | ✅ Yes (unless `HttpOnly`)                  | ✅ Yes                        | ✅ Yes                       |
| Best Use                 | Authentication, session IDs                 | User preferences, cached data | Temporary tab-specific data  |

---

## 🌍 Real-World Uses

| Use Case                                       | Best Choice     |
| ---------------------------------------------- | --------------- |
| Login session                                  | Cookies         |
| JWT token (if using secure `HttpOnly` cookies) | Cookies         |
| Dark/Light theme                               | Local Storage   |
| Language preference                            | Local Storage   |
| Temporary form data                            | Session Storage |
| Shopping cart during one tab                   | Session Storage |

---

## 🎤 Interview Answer (30 Seconds)

Cookies, Local Storage, and Session Storage are browser storage mechanisms. Cookies are small and are sent to the server with every HTTP request, making them useful for authentication and sessions. Local Storage stores data permanently until it is removed and is ideal for user preferences. Session Storage stores data only for the current browser tab and is cleared when the tab is closed.

---

## 🧠 Memory Trick

```text
🍪 Cookies
│
├── Small (4 KB)
├── Sent to Server
└── Login Sessions

----------------------

💾 Local Storage
│
├── Large
├── Browser Only
└── Permanent

----------------------

🗂️ Session Storage
│
├── Browser Only
├── Per Tab
└── Deleted When Tab Closes
```

Easy Rule:

> **Cookies = Server**

> **Local Storage = Permanent**

> **Session Storage = Temporary**

---

## ⭐ Keywords

- Cookies
- Local Storage
- Session Storage
- Browser Storage
- Authentication
- Session
- Persistent Data
- Temporary Data
- `localStorage`
- `sessionStorage`
- `document.cookie`
