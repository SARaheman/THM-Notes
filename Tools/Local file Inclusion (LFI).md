**Q:**  
What does the following URL do?

bash

CopyEdit

`http://10.10.190.238/secret-script.php?file=../../../../../etc/passwd`

**A:**  
This is a **Local File Inclusion (LFI)** attack.  
It attempts to read the system file `/etc/passwd` by exploiting a vulnerable `file` parameter that includes files without proper sanitization. The `../../..` traverses directories up to root.

---

**🧠 Key Concepts:**

- **LFI** = Load local files via web parameters
    
- `../` = Go up one directory
    
- Target: `/etc/passwd` (lists user accounts in Linux)
    
- Works if PHP uses something like `include($_GET['file'])` insecurely
    

---

**💥 Danger:**

- Can expose sensitive config files
    
- May lead to **Remote Code Execution (RCE)** if logs or uploads are included