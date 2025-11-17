# 🌐 is-dev.me — Free Subdomain Service

Welcome to **is-dev.me**, a free subdomain service for developers, students, hobby projects, bots, APIs, portfolios, and general web hosting needs.  
All DNS records are managed automatically using **deSEC DNS API** and GitHub Actions.

---

## 🚀 Features
- ✔ Free subdomain
- ✔ Automated DNS via GitHub Actions
- ✔ Supports A, AAAA, CNAME, MX, TXT, NS, and more
- ✔ Simple registration through Pull Request
- ✔ Works with GitHub Pages, Vercel, Netlify, Cloudflare Pages, VPS, and more

---

## 📥 How to Register a Subdomain

### 1. Fork this repository

### 2. Create a JSON file inside the `records` folder  
Example:  
`records/tio.json`

### 3. Use the following structure:

```json
{
  "owner": {
    "username": "YourGitHubUsername",
    "email": "your@email.com",
    "repo": "https://github.com/YourGitHubUsername/your-repo"
  },
  "subdomain": "tio",
  "records": {
    "CNAME": "your-target-domain.com"
  }
}
````

**Notes:**

* `subdomain` → desired subdomain (e.g. `"tio"` → `tio.is-dev.me`)
* `records` → DNS records (A, AAAA, TXT, CNAME, etc.)
* CNAME must point to a valid hostname

### 4. Submit a Pull Request

Your DNS will be applied automatically.

### 5. Wait for DNS propagation (1–10 minutes)

---

## 📘 Example DNS Records

### GitHub Pages (CNAME)

```json
{
  "CNAME": "username.github.io"
}
```

### VPS Server (A record)

```json
{
  "A": "123.45.67.89"
}
```

### TXT record

```json
{
  "TXT": "verification=example"
}
```

---

## ⚙️ How Automation Works

GitHub Actions will:

1. Read all JSON files inside `/records`
2. Validate DNS schema
3. Send updates to deSEC API
4. Create or update DNS records

---

## 📄 Rules

* No illegal content, malware, phishing, or harmful activities
* Subdomains may be revoked for violations
* One subdomain per user (exceptions for large projects)

---

## 💬 Support

This project does not provide dedicated support.
You may open an **Issue** if needed.

---

## ❤️ Credits

Thanks for using **is-dev.me**.
Maintained with automation and care.

