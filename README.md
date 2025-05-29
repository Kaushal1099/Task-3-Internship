# Task-3-Internship
| **Severity** | **Port/Service** | **Issue**                                    | **Fix/Mitigation**                           |
| ------------ | ---------------- | -------------------------------------------- | -------------------------------------------- |
| **High**     | 22/tcp (SSH)     | Deprecated SSH-1 Protocol                    | Disable SSH-1, use only SSH-2                |
| **High**     | 80/tcp (HTTP)    | BASE input validation flaws (SQLi, XSS, LFI) | Update BASE to v1.4.4+                       |
| **Medium**   | 22/tcp           | Weak SSH encryption (e.g., 3DES, RC4)        | Disable weak ciphers in SSH config           |
| **Medium**   | 80/tcp           | TRACE method enabled                         | Disable TRACE and TRACK in web server config |
| **Medium**   | 80/tcp           | phpMyAdmin XSS in `error.php`                | Upgrade phpMyAdmin or replace it             |
| **Medium**   | 80/tcp           | Apache httpOnly cookie disclosure            | Upgrade Apache to 2.2.22+                    |
| **Low**      | 22/tcp           | Weak MACs in SSH (e.g., MD5)                 | Disable weak MACs in SSH config              |


Most Critical Vulnerabilities:

Deprecated SSH-1 (High)
Impact: Can allow attackers to bypass security and hijack SSH sessions.
Fix: Disable SSH-1. Use only SSH-2 in /etc/ssh/sshd_config.
BASE Multiple Input Validation Issues (High)
Impact: Leads to SQL injection, XSS, LFI.
Fix: Upgrade to BASE v1.4.4 or later.
