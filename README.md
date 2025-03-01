# 🚀 ISS Overhead Notifier

## 📌 Project Overview
This Python script **tracks the International Space Station (ISS) in real time** and sends an **email alert** when the ISS is overhead at your location during nighttime. 🌍✨

## 📜 How It Works
1. **Fetch ISS Location** – Uses the [Open Notify API](http://api.open-notify.org/) to get the ISS's real-time latitude and longitude.
2. **Check If It's Overhead** – Compares ISS coordinates with your location (within ±5° latitude & longitude).
3. **Fetch Sunrise & Sunset Data** – Uses the [Sunrise-Sunset API](https://sunrise-sunset.org/api) to determine if it’s dark at your location.
4. **Send Email Notification** – If both conditions are met (ISS overhead & nighttime), an email is sent via SMTP.
5. **Run Every 60 Seconds** – The script runs continuously in the background to check every minute.

## 🛠️ Tech Stack
- **Python**
- **APIs** (Open Notify, Sunrise-Sunset)
- **Requests Module** (for API calls)
- **Datetime Module** (for time handling)
- **SMTP (smtplib)** (for sending emails)

## 📂 Project Structure
```
|-- main.py         # Main script to track ISS and send email
|-- README.md       # Project documentation (this file)
```

## 🔧 Setup & Installation
### 1️⃣ Clone the Repository
```bash
git clone https://github.com/abhinav23122021234/ISS-Overhead-Notifier.git
cd ISS-Overhead-Notifier
```

### 2️⃣ Install Dependencies
```bash
pip install requests
```

### 3️⃣ Set Your Location & Email Credentials
- Update **`MY_LAT`** and **`MY_LONG`** in `main.py` with your latitude and longitude.
- Set **your email and password** in `MY_EMAIL` and `MY_PASSWORD` variables.

🔹 **Tip:** You may need to enable "Less Secure Apps" or use an app password if using Gmail.

### 4️⃣ Run the Script
```bash
python main.py
```

## 📧 Expected Output
- If the ISS is overhead and it's dark, you'll receive an **email notification**:
  > "LOOK UP! 🚀 The ISS is passing over you right now!"
- The script **runs continuously**, checking **every 60 seconds**.

## 🎯 Future Enhancements
✅ **Use OAuth for secure email authentication**  
✅ **Integrate push notifications instead of emails**  
✅ **Add a GUI or Web Dashboard to visualize ISS tracking**  

## 📌 Notes
- The **ISS completes an orbit around Earth every ~90 minutes**! If it hasn’t passed over your location yet, **keep the script running** and it will detect it soon.
- 🌍 **I'll update this README with a screenshot of the email notification once I receive it!**


