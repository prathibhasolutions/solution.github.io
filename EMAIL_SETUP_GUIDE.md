# 📧 EMAIL SETUP GUIDE FOR CONTACT FORM

## 🎯 STEP-BY-STEP SETUP (FREE & EASY)

### **Method 1: EmailJS Setup (Recommended)**

#### 1️⃣ **Create EmailJS Account**
- Go to: https://www.emailjs.com/
- Sign up with your Gmail (prathibhasolutions1@gmail.com)
- It's FREE up to 200 emails/month

#### 2️⃣ **Add Email Service**
- In EmailJS dashboard, click "Add New Service"
- Choose "Gmail" 
- Connect your Gmail account (prathibhasolutions1@gmail.com)
- Note the **Service ID** (e.g., "service_abc123")

#### 3️⃣ **Create Email Template**
- Go to "Email Templates" → "Create New Template"
- Template content:
```
Subject: New Contact Form Message: {{subject}}

From: {{from_name}}
Email: {{from_email}}

Message:
{{message}}

---
Sent from Prathibha Solutions website contact form
Reply to: {{reply_to}}
```
- Note the **Template ID** (e.g., "template_xyz789")

#### 4️⃣ **Get Public Key**
- Go to "Account" → "General"
- Copy your **Public Key** (e.g., "abc123xyz")

#### 5️⃣ **Update Contact Page**
Edit `pages/contact.html` and replace:
```javascript
emailjs.init('your_public_key_here'); // Replace with actual public key
```
```javascript
emailjs.send('your_service_id', 'your_template_id', { // Replace with actual IDs
```

#### 6️⃣ **Test the Form**
- Fill out your contact form
- Check your Gmail inbox for messages!

---

### **Method 2: Alternative - Formspree (Easier Setup)**

If EmailJS seems complicated, use Formspree:

#### 1️⃣ **Create Formspree Account**
- Go to: https://formspree.io/
- Sign up (free for 50 submissions/month)

#### 2️⃣ **Create Form**
- Add new form
- Set endpoint email: prathibhasolutions1@gmail.com
- Copy the form endpoint URL

#### 3️⃣ **Update Contact Form**
Replace the entire `<form>` tag in contact.html:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <input type="text" name="name" placeholder="Your Name" required>
    <input type="email" name="email" placeholder="Your Email" required>
    <input type="text" name="subject" placeholder="Subject" required>
    <textarea name="message" placeholder="Your Message" required></textarea>
    <button type="submit">Send Message</button>
</form>
```

---

### **Method 3: Quick Test Setup**

For immediate testing, I can set up a simple version that shows you the message data:

Would you like me to:
1. Set up EmailJS (you'll need to create the account)
2. Set up Formspree (easier, just need account)
3. Create a simple test version first

**Recommendation:** Start with EmailJS - it's professional and reliable!

---

## 📞 **Current Contact Info Displayed:**
- **Email:** prathibhasolutions1@gmail.com
- **Phone:** +91 9542906390
- **Contact Person:** Shravan Kumar

## 🎯 **What Happens After Setup:**
1. Visitor fills contact form
2. Email sent instantly to prathibhasolutions1@gmail.com
3. You get notification on your phone/email
4. You can reply directly from Gmail
5. Professional email management!

Choose your preferred method and I'll help you implement it!