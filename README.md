# 🛡️ DLP Policy using Sophos Endpoint Protection

## 📘 Project Overview
This project demonstrates how to configure a **Data Loss Prevention (DLP)** policy in **Sophos Endpoint Protection** to block the upload or transfer of sensitive personal data such as **Aadhaar Numbers** and **Bank Details**.  
It ensures that users cannot share confidential information via **web browsers (like Chrome)** or **external drives (like USB Pendrives)**.

---

## ⚙️ Configuration Details

### **Policy Name**
`Aadhaar number block`

### **Policy Type**
`Data Loss Prevention: User`

### **Description**
`Upload blocking`

### **Status**
✅ Policy Active

---

## 🧩 Steps to Create the DLP Policy

1. Go to **Endpoint Protection → Computer Policies → Add Policy**  
2. Set **Policy Name:** `Aadhaar number block`
3. Under **Policy Type**, select **Data Loss Prevention: User**
4. Enable **Use rules for data transfers**
5. Click **Add → New Content Rule**
6. Create a rule named **Aadhaar number Privacy**
   - **Rule Type:** Content  
   - **Source:** Custom  
   - Add Aadhaar number pattern or keywords  
   - Choose **Block file transfer** action
7. Save the policy and apply it to target users or devices.

---

## 🔒 Example Behavior

- When a user tries to **upload a file containing Aadhaar numbers** on Chrome →  
  🔴 Sophos **immediately blocks the upload**.
- When a user tries to **copy such file to a USB pendrive** →  
  🔴 Transfer is **blocked** automatically.
