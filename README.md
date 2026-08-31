# B082-Networkwalks-WEEK-3-Password-Cracking-with-JTR-Johnny-Networkwalks-Tools

## Cybersecurity & Ethical Hacking | NetworkWalks

This repository documents the practical activities completed during **Week 3** of the NetworkWalks Cybersecurity & Ethical Hacking program.

The focus of Week 3 was **password cracking and password security assessment**. The practical work involved recovering passwords from protected PDF files using two different approaches: **John the Ripper (JTR)** and the **NetworkWalks password-cracking tools**.

The exercises were performed in an authorized educational lab environment to understand how password-protected files can be assessed, how password hashes are extracted, and how cracking tools attempt to recover the original password.

---

## Project Modules

### WK3-PM1 — Password Cracking with JTR

This module focused on using **John the Ripper (JTR)** to recover the password of protected PDF files.

John the Ripper is a password-cracking tool commonly used by security professionals to test password strength. The module also introduced **Johnny**, the graphical user interface for John the Ripper, making the cracking process easier to perform through a point-and-click interface.

The module required the password of a protected PDF to be recovered using JTR **John** and **Johnny** on a Windows PC. Kali Linux users can also use John the Ripper because it is included with Kali Linux.

### WK3-PM2 — Password Cracking with NetworkWalks Tools

This module focused on password cracking using two browser-based tools provided by NetworkWalks:

* **NetworkWalks Hash Calculator**
* **NetworkWalks Password Cracker**

The Hash Calculator was used to extract the PDF password hash, while the Password Cracker was used to attempt to recover the original password from the extracted hash. The tools operate through a web browser, so no additional software installation was required for this module.

---

# Objectives

The main objectives of these practical exercises were to:

* Understand the fundamentals of password cracking.
* Understand how password-protected PDF files are assessed.
* Extract password hashes from encrypted PDF files.
* Use John the Ripper to perform password-cracking attacks.
* Use the Johnny GUI to interact with John the Ripper.
* Use NetworkWalks Hash Calculator to obtain PDF hashes.
* Use NetworkWalks Password Cracker to recover passwords.
* Verify recovered passwords by opening the original protected PDF files.
* Understand the importance of strong and complex passwords.
* Gain practical experience with commonly used password-security assessment techniques.

---

# Environment

| Component        | Details                                  |
| ---------------- | ---------------------------------------- |
| Operating System | Windows PC                               |
| Primary Focus    | Password Security Assessment             |
| File Type        | Password-Protected PDF                   |
| Module 1 Tool    | John the Ripper                          |
| Module 1 GUI     | Johnny                                   |
| Module 2 Tool    | NetworkWalks Hash Calculator             |
| Module 2 Tool    | NetworkWalks Password Cracker            |
| Lab Type         | Authorized Educational Cybersecurity Lab |

---

# Tools & Technologies

## 1. John the Ripper

John the Ripper (JTR) is a password-cracking tool used to test the strength of passwords and recover passwords from supported password hashes.

In this project, JTR was used to process the extracted PDF hash and attempt to recover the password protecting the PDF files.

## 2. Johnny

Johnny is the graphical user interface for John the Ripper.

It provides a simpler interface for configuring John, loading password/hash files, starting attacks and monitoring the cracking process.

## 3. NetworkWalks Hash Calculator

The NetworkWalks Hash Calculator was used to upload a protected PDF and obtain the corresponding PDF hash.

The resulting hash begins with the `$pdf$` format required for the subsequent password-cracking process.

## 4. NetworkWalks Password Cracker

The extracted PDF hash was entered into the NetworkWalks Password Cracker.

The tool attempts different passwords until a matching password is identified.

---

# WK3-PM1 — Password Cracking with JTR

## Methodology

The JTR module followed a process of extracting the password hash from each protected PDF, preparing the hash for John the Ripper, loading the hash into Johnny and starting the password-cracking attack.

### Step 1 — Prepare the Protected PDF

The encrypted PDF files were obtained and prepared for password analysis.

For this project, three protected PDF files were processed separately.

### Step 2 — Extract the PDF Hash

The PDF hash was extracted using a PDF hash-extraction method.

The resulting value was required to be in the appropriate `$pdf$...` format before being supplied to John the Ripper.

### Step 3 — Save the Hash

The extracted hash was copied into a text file.

The hash file was prepared so that John the Ripper could read and process the value.

### Step 4 — Configure Johnny

Johnny was opened and configured to use the John the Ripper executable.

The hash/password file was then loaded into Johnny.

### Step 5 — Start the Password-Cracking Attack

A new attack was started through Johnny.

John the Ripper attempted different password candidates against the extracted PDF hash. The time required depends on factors such as password complexity and system performance.

### Step 6 — Recover and Verify the Password

Once the password was recovered, it was entered into the corresponding protected PDF.

Successful opening of the PDF confirmed that the recovered password was correct.

---

# WK3-PM1 — PDF Exercises

Three protected PDF files were processed as part of the module:

| Exercise | File          | Evidence        |
| -------- | ------------- | --------------- |
| PDF 1    | Protected PDF | `WK3-PM1-PDF_1` |
| PDF 2    | Protected PDF | `WK3-PM1-PDF_2` |
| PDF 3    | Protected PDF | `WK3-PM1-PDF_3` |

Each collage contains the relevant screenshots documenting the password-cracking workflow and verification process.

---

# WK3-PM2 — Password Cracking with NetworkWalks Tools

## Methodology

The second module used the NetworkWalks online tools to demonstrate the same general password-recovery concept without installing John the Ripper.

The workflow consisted of:

**Protected PDF → Hash Calculator → PDF Hash → Password Cracker → Recovered Password → PDF Verification**

This module was completed for three separate protected PDF files.

### Step 1 — Obtain the Protected PDF

The encrypted PDF was downloaded and prepared for the practical exercise.

### Step 2 — Generate the PDF Hash

The protected PDF was uploaded to the **NetworkWalks Hash Calculator**.

The calculator processed the file and returned a PDF password hash beginning with `$pdf$`.

### Step 3 — Copy the Complete Hash

The complete hash value was copied for use in the next stage.

Care was taken to ensure that the entire hash was copied correctly.

### Step 4 — Open the Password Cracker

The **NetworkWalks Password Cracker** was opened in a web browser.

The extracted hash was entered into the tool.

### Step 5 — Start the Attack

The password-cracking process was started.

The tool attempted different password candidates until a matching password was identified. The time required can vary depending on the complexity of the password.

### Step 6 — Verify the Recovered Password

The recovered password was entered into the corresponding protected PDF.

Successfully opening the PDF confirmed that the password had been recovered correctly.

---

# WK3-PM2 — PDF Exercises

Three protected PDF files were processed as part of the module:

| Exercise | File          | Evidence        |
| -------- | ------------- | --------------- |
| PDF 1    | Protected PDF | `WK3-PM2-PDF_1` |
| PDF 2    | Protected PDF | `WK3-PM2-PDF_2` |
| PDF 3    | Protected PDF | `WK3-PM2-PDF_3` |

Each collage contains three screenshots documenting the relevant stages of the exercise.

---

# Comparison of the Two Approaches

| Feature               | WK3-PM1                 | WK3-PM2                         |
| --------------------- | ----------------------- | ------------------------------- |
| Approach              | Local password cracking | Browser-based password cracking |
| Main Tool             | John the Ripper         | NetworkWalks Password Cracker   |
| Hash Extraction       | PDF hash extraction     | NetworkWalks Hash Calculator    |
| GUI                   | Johnny                  | Web Interface                   |
| Installation          | JTR/Johnny required     | No additional installation      |
| Hash Input            | Text/hash file          | Directly pasted hash            |
| Password Verification | Protected PDF           | Protected PDF                   |
| PDFs Tested           | 3                       | 3                               |

The two modules demonstrated the same overall security concept from different perspectives. PM1 provided practical experience with a dedicated password-cracking tool, while PM2 demonstrated a simpler browser-based workflow using NetworkWalks tools.

---

# Results

The practical exercises demonstrated the complete password-recovery workflow for protected PDF files.

Across the two modules:

* **3 protected PDFs** were processed in WK3-PM1.
* **3 protected PDFs** were processed in WK3-PM2.
* PDF hashes were successfully obtained for the exercises.
* Password-cracking tools were used to attempt password recovery.
* Recovered passwords were tested against the corresponding protected PDFs.
* Successful PDF access provided verification of the recovered passwords.

### Overall Workflow

```text
Protected PDF
      ↓
Extract PDF Hash
      ↓
Prepare Hash
      ↓
Password-Cracking Tool
      ↓
Password Recovery
      ↓
Enter Recovered Password
      ↓
Verify PDF Access
```

---

# Key Learning Outcomes

Through these practical exercises, I gained hands-on experience in:

* Understanding how password-protected files are secured.
* Understanding the role of password hashes in password recovery.
* Extracting hashes from protected PDF files.
* Using John the Ripper for password-cracking activities.
* Using Johnny as a graphical interface for JTR.
* Using browser-based password-cracking tools.
* Comparing local and online password-cracking workflows.
* Verifying recovered passwords against protected files.
* Understanding the relationship between password complexity and cracking difficulty.
* Recognizing the importance of strong password policies.

---

# Security Significance

Password cracking is an important technique in authorized security assessments because it can demonstrate the practical impact of weak passwords.

If a password is short, common or predictable, password-cracking tools may be able to recover it relatively quickly. This highlights the importance of using passwords that are sufficiently long, complex and difficult to guess.

From a defensive perspective, organizations can use controlled password assessments to identify weak credentials and improve their password policies.

## The exercises also demonstrate an important distinction between **encryption and hashing**. Encryption is designed to protect information so it can be recovered with the appropriate key, while hashing transforms data into a digest that is intended to be one-way.

# Screenshots

All practical evidence is included directly in this repository as screenshot collages.

## WK3-PM1 — Password Cracking with JTR

### PDF 1

<img width="3000" height="2357" alt="WK3-PM1-PDF_1" src="https://github.com/user-attachments/assets/55e74c60-56f9-4bac-8945-c028e4ef9e05" />


### PDF 2

<img width="3000" height="2416" alt="WK3-PM1-PDF_2" src="https://github.com/user-attachments/assets/36976e93-2dac-4dfd-91ae-f94bccd5237e" />


### PDF 3

<img width="3000" height="2369" alt="WK3-PM1-PDF_3" src="https://github.com/user-attachments/assets/c001150b-8ff8-4a7c-8e8c-545334c2dee5" />


---

## WK3-PM2 — Password Cracking with NetworkWalks Tools

### PDF 1


<img width="3000" height="2129" alt="WK3-PM2-PDF_1" src="https://github.com/user-attachments/assets/9a4218a3-6c7e-403b-b50e-4eed15309c96" />


### PDF 2


<img width="3000" height="2129" alt="WK3-PM2-PDF_2" src="https://github.com/user-attachments/assets/bfaeb235-1ec4-44a2-bdb6-aaae4fb7eebc" />


### PDF 3


<img width="3000" height="2252" alt="WK3-PM2-PDF_3" src="https://github.com/user-attachments/assets/d8a5aa12-16d6-4a92-bbbf-3f40ce5a133e" />


---

# Conclusion

Week 3 provided practical exposure to password security assessment through two different password-cracking approaches.

**WK3-PM1** focused on using John the Ripper and Johnny to process PDF hashes and recover passwords through a dedicated password-cracking environment.

**WK3-PM2** demonstrated the same fundamental concept using the NetworkWalks Hash Calculator and Password Cracker through a web browser.

Completing both modules strengthened my understanding of password hashes, password recovery workflows, cracking tools and the importance of strong password security.

These exercises also reinforced the importance of conducting password assessments only within an authorized and controlled environment.

---

# Disclaimer

All activities documented in this repository were performed as part of an **authorized educational cybersecurity laboratory exercise**.

The techniques and tools demonstrated are intended for learning, security testing and defensive assessment purposes only. Password cracking, hash extraction and related activities must only be performed against files, systems or accounts for which appropriate authorization has been provided.

Unauthorized access, password cracking or security testing may violate laws, regulations and organizational policies.

