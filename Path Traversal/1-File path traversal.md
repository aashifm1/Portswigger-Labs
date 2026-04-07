
## File Path Traversal – Simple Case

**Objective:**  
Access the `/etc/passwd` file.

**Steps:**

- Opened an image in a new tab.
- Observed the URL parameter:  
  `?filename=path`

<img width="925" height="550" alt="image1" src="https://github.com/user-attachments/assets/1e1ba6cd-7a24-42f3-bde1-b7c1d0b768b4" />

- Intercepted the request in Burp Suite.
- Modified the `filename` parameter to:

```bash
../../../etc/passwd
```

- Sent the request.

**Result:**

<img width="1434" height="703" alt="image2" src="https://github.com/user-attachments/assets/203b7cca-0f63-447c-943b-e5c645ff1a4f" />

- Successfully retrieved the `/etc/passwd` file.

**Conclusion:**


- This vulnerability is known as a **Path Traversal (Directory Traversal)** vulnerability.
