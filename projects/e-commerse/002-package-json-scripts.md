# 📚 package.json Scripts (`start` and `db:push`)

## 📖 Simple English Explanation

These lines are **scripts** defined inside the `package.json` file. Scripts allow you to run commands using `npm run` instead of typing long commands in the terminal. They make common tasks like starting the application or updating the database much easier.

---

## 🤔 Why is it Needed?

- It saves time by giving short names to long commands.
- It keeps project commands consistent for all developers.
- It makes development easier and less error-prone.
- Without scripts, you would have to remember and type the full command every time.

---

## 🌊 Flow

```text
Run npm run <script-name>
          ↓
npm reads package.json
          ↓
Finds the matching command
          ↓
Executes the command
```

---

## ✍️ Syntax

```json
{
  "scripts": {
    "script-name": "command"
  }
}
```

---

## 💻 Example

### package.json

```json
{
  "scripts": {
    "start": "node dist/index.js",
    "db:push": "drizzle-kit push"
  }
}
```

### Run the scripts

```bash
npm run start
```

```bash
npm run db:push
```

---

## 🎤 Interview Answer (30 Seconds)

`package.json` scripts are shortcuts for terminal commands. Instead of typing long commands manually, we define them once in the `scripts` section and run them using `npm run <script-name>`. This makes development faster, more consistent, and easier for the whole team.

---

## 🧠 Memory Trick

Think of **scripts as phone contacts**.

Instead of remembering someone's full phone number, you save it as:

```text
Mom → 9876543210
```

Similarly,

```text
start  → node dist/index.js
db:push → drizzle-kit push
```

You remember only the **name**, and npm knows the full command.

---

## ⭐ Keywords

- package.json
- Scripts
- npm run
- Command Shortcut
- Node.js
- Terminal
