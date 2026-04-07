
## File Path Traversal – Simple Case

**Objective:**  
Access the `/etc/passwd` file.

**Steps:**

- Opened an image in a new tab.
- Observed the URL parameter:  
  `?filename=path`

- Intercepted the request in Burp Suite.
- Modified the `filename` parameter to:

```bash
../../../etc/passwd
```

- Sent the request.

**Result:**

- Successfully retrieved the `/etc/passwd` file.

**Conclusion:**

- This vulnerability is known as a **Path Traversal (Directory Traversal)** vulnerability.