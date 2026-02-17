# 🚩 Room: Offensive Security Intro (TryHackMe)

This room serves as an introduction to the mindset of an ethical hacker. It covers the fundamental difference between offensive and defensive security and demonstrates a basic web application attack.

## 📝 Key Concepts

### 1. Offensive Security
* **Definition:** Breaking into computer systems, exploiting software bugs, and finding loopholes to gain unauthorized access.
* **Goal:** To understand hacker tactics in order to build stronger defense mechanisms (**"To outsmart a hacker, you need to think like one"**).

### 2. Directory Brute-forcing
Many web applications have hidden pages not linked to the main menu. Hackers use brute-force techniques to guess these URLs and find sensitive functionalities.

---

## 🛠 Tool Highlight: `dirb`
**dirb** is a web content scanner that uses a "wordlist" to test for the existence of hidden directories and pages on a web server.

**Command Used:**
```bash
dirb [http://fakebank.thm](http://fakebank.thm)