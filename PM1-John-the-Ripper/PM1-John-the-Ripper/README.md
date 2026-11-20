
# 🔐 PM1 — Password Recovery Using John the Ripper & Johnny

## 📌 Project Overview

As part of Week 3 of my NetworkWalks Cybersecurity Internship, I completed a practical password-recovery exercise using **John the Ripper** and its graphical user interface, **Johnny**.

The objective was to understand how password-cracking tools work, recover passwords from authorized training PDF files, and verify the results.

All activities were performed in a controlled learning environment.

## 🎯 Objectives

- Install and configure John the Ripper on Windows.
- Set up the Johnny graphical user interface.
- Understand how password hashes are used in password recovery.
- Load PDF password hashes into Johnny.
- Perform password-recovery attacks against training files.
- Verify successful recovery by opening the protected PDFs.

## 🛠️ Tools and Environment

| Tool | Purpose |
|------|---------|
| John the Ripper 1.9.0-jumbo-1 | Password recovery |
| Johnny GUI | Graphical interface for John the Ripper |
| Windows 64-bit | Operating system |
| PDF hash extractor | Obtaining PDF password hashes |
| Command Prompt | Verifying the John the Ripper installation |

## ⚙️ Implementation

### Step 1 — Installing John the Ripper

I downloaded the Windows 64-bit version of John the Ripper and extracted the archive.

The executable was located inside the `run` directory.

Initially, Windows Command Prompt did not recognize the `john` command because the executable was not in the current directory or system PATH.

I resolved this by navigating to the correct folder and running:

```cmd
john.exe --list=build-info
```

This confirmed that John the Ripper was installed and working.

### Step 2 — Configuring Johnny

I installed Johnny, the graphical interface for John the Ripper.

I then configured Johnny to use the `john.exe` executable from the extracted John the Ripper directory.

This allowed me to perform password-recovery operations through a graphical interface.

### Step 3 — Preparing the PDF Hashes

The exercise involved three password-protected training PDF files.

I used a PDF hash extraction tool to obtain the password-verification hashes and saved them as text files:

- `hash1.txt`
- `hash2.txt`
- `hash3.txt`

These files were used as inputs for the password-recovery process.

### Step 4 — Performing Password Recovery

For each training PDF:

1. Opened Johnny.
2. Selected the option to open a password file.
3. Loaded the corresponding PDF hash.
4. Started a password-recovery attack.
5. Monitored the progress and reviewed the results.

Johnny successfully recovered the password for the documented training file.

The interface displayed:

**100% (1/1: 1 cracked, 0 left)**

This confirmed that the loaded hash had been cracked successfully.

### Step 5 — Verifying the Results

After recovering the passwords, I opened the protected PDF files to verify that the recovered credentials worked.

The three training PDFs were successfully unlocked.

## 📸 Screenshots and Evidence

### Johnny — Successful Password Recovery

The Johnny interface displaying the successful recovery result.

![Johnny password recovery result](../screenshots/Johnny.png)

### PDF 1 — Successfully Unlocked

![PDF 1 unlocked](../screenshots/pdf1-unlocked.png)

### PDF 2 — Successfully Unlocked

![PDF 2 unlocked](../screenshots/pdf2-unlocked.png)

### PDF 3 — Successfully Unlocked

![PDF 3 unlocked](../screenshots/pdf3-unlocked.png)

## 🧩 Challenges and Solutions

**Challenge 1: John the Ripper command not recognized**

The `john` command was initially not recognized in Windows Command Prompt.

**Solution:** Navigated to the directory containing `john.exe` and executed the program from there.

**Challenge 2: Working with PDF password hashes**

The password-protected PDFs could not be used directly as ordinary plaintext password lists.

**Solution:** Extracted their password-verification hashes and loaded the resulting text files into Johnny.

## 🧠 Key Learning Outcomes

Through this exercise, I learned how to:

- Configure a password-auditing tool on Windows.
- Use a graphical interface for password recovery.
- Work with PDF password hashes.
- Interpret password-cracking results.
- Verify recovered passwords against protected documents.
- Troubleshoot command-line installation issues.

The exercise also demonstrated why predictable passwords are vulnerable to dictionary-based password attacks.

## ⚖️ Ethical Considerations

All password-recovery activities were performed on authorized training PDFs provided for educational purposes.

These techniques must only be used on systems and files that I own or have explicit permission to test.

---

**Internship:** NetworkWalks Cybersecurity Internship  
**Module:** PM1 — John the Ripper & Johnny  
**Week:** 3
