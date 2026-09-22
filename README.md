# NETWORKWALKS-B083-WK3-PM1-PM2-PASSWORD-CRACKING
# 🔐 Password Cracking with JTR(John the Ripper) & Networkwalks Tools

## 📌 Project Overview

This project was completed as part of **Week 3** of my **Cybersecurity & Ethical Hacking Internship at Networkwalks**.

The project focused on understanding password cracking in a controlled cybersecurity lab environment. I practiced recovering the password of a protected PDF using:

* **John the Ripper (JTR)**
* **Johnny GUI for John the Ripper**
* **Networkwalks Hash Calculator**
* **Networkwalks Password Cracker**

The exercises demonstrate how a protected file can be analyzed by extracting its password hash and using password-cracking tools to recover the original password. The purpose of the lab was to understand password security and the importance of using strong passwords.

---

# 🎯 Objectives

* Understand the basics of password cracking.
* Learn how password-protected PDF files can be analyzed.
* Extract the hash associated with a protected PDF.
* Use **John the Ripper** to perform password recovery.
* Use **Johnny**, the graphical interface for JTR.
* Use Networkwalks online tools for hash extraction and password recovery.
* Understand the relationship between password complexity and cracking time.
* Practice password-cracking techniques in a controlled and authorized environment.

---

# 🛠️ Tools & Technologies

### Method 1 – John the Ripper

* John the Ripper (JTR)
* Johnny GUI
* Windows PC / Kali Linux
* Protected PDF file
* PDF hash extraction tool

### Method 2 – Networkwalks Tools

* Networkwalks Hash Calculator
* Networkwalks Password Cracker
* Web Browser
* Windows PC / Kali Linux
* Protected PDF file

---

# 🔎 Method 1: Password Cracking with John the Ripper

## Step 1 – Download John the Ripper

Download **John the Ripper** from the official Openwall website:

* https://www.openwall.com/john/

John the Ripper is available for Windows, Linux, and macOS. Kali Linux also provides JTR as a pre-installed security tool.

---

## Step 2 – Install Johnny GUI

Download and install **Johnny**, the graphical interface for John the Ripper:

* https://openwall.info/wiki/john/johnny

Johnny provides a graphical interface that makes it easier to work with John the Ripper without entering all commands manually.

After installation:

1. Open **Johnny**.
2. Open **Settings**.
3. Browse to the JTR installation directory.
4. Select the `john.exe` file.
5. The `john.exe` file is located inside the **run** folder of the John the Ripper installation.

![image alt](https://github.com/rohithkr24/NETWORKWALKS-B083-WK3-PM1-PM2-PASSWORD-CRACKING/blob/8d828bc51fdabee8ffca1c2fd353429d93c61846/2_Johnny.png)

---

## Step 3 – Obtain the PDF Hash

For the authorized lab PDF:

1. Obtain the protected PDF provided for the exercise.
2. Open a PDF hash extraction tool.
3. Upload the protected PDF.
4. Extract the password hash.

The lab material uses the following PDF hash extraction tool:

**PDF Hash Extractor:**
https://www.onlinehashcrack.com/tools-pdf-hash-extractor.php

The extracted hash should begin with:

```text
$pdf$
```

If the extracted value contains additional characters such as `b'` at the beginning, the lab instructions specify removing those characters before saving the hash.

---

## Step 4 – Save the Hash

1. Open **Notepad**.
2. Paste the complete PDF hash.
3. Save the file as:

```text
hash1.txt
```

The resulting text file contains the hash that will be supplied to John the Ripper through Johnny.

---

## Step 5 – Load the Hash into Johnny

1. Open **Johnny**.
2. Select **Open password file**.
3. Browse to:

```text
hash1.txt
```

4. Open the file.
5. Select **Start new attack**.

John the Ripper will then attempt password recovery. The time required depends on factors such as the computer's processing speed and the complexity of the password.

![image alt](https://github.com/rohithkr24/NETWORKWALKS-B083-WK3-PM1-PM2-PASSWORD-CRACKING/blob/8d828bc51fdabee8ffca1c2fd353429d93c61846/1_PM1_results.png)

---

## Step 6 – Recover the Password

After the password-recovery process completes, the recovered password can be used to open the authorized protected PDF.

For the lab exercise, the recovered password is then entered into the PDF reader to verify successful recovery.

---

# 🌐 Method 2: Password Cracking with Networkwalks Tools

The second part of the project uses two browser-based Networkwalks tools:

1. **Hash Calculator**
2. **Password Cracker**

Unlike the JTR setup, these tools run directly in a web browser and do not require local installation.

---

## Step 1 – Obtain the Protected PDF

Download the authorized lab PDF from the Networkwalks project page:

https://networkwalks.com/project-task-lab-password-cracking-with-networkwalks-tools/

---

## Step 2 – Open Hash Calculator

Open the Networkwalks Hash Calculator:

https://networkwalks.com/hash-calculator/

Upload the protected PDF file.

The tool processes the file and produces a PDF password hash beginning with:

```text
$pdf$
```

---

## Step 3 – Copy the Hash

Copy the **complete hash value** generated by the Hash Calculator.

Make sure the complete value is copied, including the `$pdf$` prefix.

---

## Step 4 – Open Password Cracker

Open the Networkwalks Password Cracker:

https://networkwalks.com/password-cracker/

Paste the extracted hash into the Password Cracker.

---

## Step 5 – Start Password Recovery

Start the password-cracking process.

The tool attempts different password candidates until it finds a matching password.

The time required depends on the complexity of the password.

---

## Step 6 – Verify the Recovered Password

Once the process finishes, the recovered password is displayed.

Open the authorized protected PDF and enter the recovered password. If the password is correct, the PDF opens successfully.

---

# 🧠 Key Concepts Learned

### Encryption vs Hashing

The lab distinguishes between encryption and hashing:

* **Encryption** is described as a two-way process in which encrypted information can be decrypted using the appropriate key.
* **Hashing** is described as a one-way process that converts plaintext into a message digest.

### Password Cracking

Password cracking is the process of attempting to recover a password from stored password data or a protected file. The lab demonstrates the general workflow of extracting a hash and attempting to find a password that matches it.

### Password Complexity

The exercises demonstrate that password complexity can affect the amount of time required for password recovery. Simple or commonly used passwords can be significantly easier to recover than stronger passwords.

---

# 📊 Project Workflow

```text
              Protected PDF
                    │
                    ▼
             Extract PDF Hash
                    │
             ┌──────┴──────┐
             │             │
             ▼             ▼
       John the Ripper   Networkwalks
             │             │
             ▼             ▼
          Johnny       Hash Calculator
             │             │
             ▼             ▼
      Password Attack  Password Cracker
             │             │
             └──────┬──────┘
                    ▼
             Recovered Password
                    │
                    ▼
              Open Protected PDF
```

---

# 🔐 Ethical & Security Disclaimer

This project was performed as part of a cybersecurity learning exercise in a controlled environment.

Password-cracking techniques should only be used on files, accounts, systems, or data for which you have explicit authorization to perform security testing.

Do **not** use these techniques to access passwords, accounts, files, or systems belonging to other people without permission.

The objective of this project is to understand password security, ethical hacking methodologies, and the importance of strong password protection.

---

# 📚 Learning Outcomes

Through this project, I gained practical exposure to:

* John the Ripper
* Johnny GUI
* Password hash extraction
* PDF password recovery
* Networkwalks security tools
* Password-cracking workflows
* Hashing and encryption concepts
* Password complexity and security
* Ethical and authorized security testing

---

# 📁 Project Information

**Program:** Cybersecurity & Ethical Hacking Internship |
**Organization:** Networkwalks |
**Week:** 03 |
**Project:** Password Cracking with JTR & Networkwalks Tools |
**Repository:** GitHub |
**Field:** Cybersecurity / Ethical Hacking |

---

# 👨‍💻 Author

**Rohith K R**

**Cybersecurity Intern — B083**

**LinkedIn:** [linkedin.com/in/rohith-k-r-55236a30b](https://linkedin.com/in/rohith-k-r-55236a30b)

---

## ⭐ Conclusion

Week 3 provided hands-on experience with password-cracking workflows using both **John the Ripper/Johnny** and **Networkwalks browser-based tools**. The project helped demonstrate how password hashes can be extracted from protected files and analyzed during an authorized security assessment.

The practical exercise also reinforced the importance of using strong and complex passwords to reduce the risk of successful password recovery.

