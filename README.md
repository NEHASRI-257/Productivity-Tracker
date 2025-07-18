# MERN Stack Web Development  
______________________________________  
## Company: CODTECH IT SOLUTIONS
##  Name: NEHASRI H
##  Intern Id: CT08DM1117
##  Domain: MERN STACK WEB DEVELOPMENT
##  Duration: 8 WEEKS
##  Mentor:NEELA SANTHOSH

---

#  Productivity Tracker Chrome Extension

As part of my internship at **CodTech IT Solutions**, I developed a full-stack **Productivity Tracker Chrome Extension**, designed to help users monitor and control their web browsing habits. This project combines browser-level tracking with a cloud-connected backend to offer users a practical tool for improving online focus. Built entirely using the **MERN stack** (MongoDB, Express, React, Node.js), this extension captures real-time browsing activity, blocks distracting websites, and provides insightful usage analytics—allowing users to take charge of their productivity.

The project began with identifying a common problem: frequent distractions while using the internet, which can significantly reduce productivity. I approached the solution by designing a Chrome extension that not only records time spent on websites but also allows users to block specific domains and review their browsing patterns through clean, actionable reports.

On the **frontend**, I built the extension’s user interface using **React**, adapted specifically for **Chrome Extension Manifest V3** compliance. The popup UI includes key features such as a usage timer, a domain blocklist form, and alert feedback. To handle extension-specific behaviors like messaging and service workers, I used Chrome’s extension APIs and configured the app using **Vite**, which efficiently bundles the project into a Manifest V3-compatible build. The interface was designed for quick access and usability within the browser's toolbar.

The **backend** was implemented using **Node.js** and **Express**, forming a REST API that communicates with a **MongoDB** database. The server manages user-specific records, logs time spent on websites, and stores blocklist data. I designed endpoints to log domain visits, retrieve usage data over different time ranges (daily and weekly), and update or fetch each user’s personalized list of blocked websites.

To ensure data continuity across browsing sessions and even different devices, I introduced a **Device ID mechanism**. This allowed each browser instance to maintain a consistent link to the user’s activity in the database. Time tracking was handled in the background using Chrome's extension APIs—scripts monitored active browser tabs, tracked the time spent on each website, and sent this data to the backend at regular intervals.

The blocking feature was implemented by intercepting navigation attempts to any domain listed in the user’s blocklist. When such a domain is accessed, the extension automatically redirects the user to a custom **“Blocked Page”**, discouraging access and reinforcing productive behavior.

Extensive testing was conducted to validate each feature. I simulated user behavior such as frequent tab switching, usage spikes, and blocklist changes. Reports were cross-verified with server logs to ensure accurate tracking and analytics. The system functioned reliably across different machines and browsers, offering consistent performance.

This project gave me real-world experience in **Chrome extension development**, integrating **React with browser APIs**, designing **RESTful services**, and working with **MongoDB** for time-based tracking. It also enhanced my understanding of syncing local browser activity with cloud databases to build responsive and intelligent productivity tools.


# Demo Snapshots

### 🟦 1. Initial Dashboard – Default State
![Image](https://github.com/user-attachments/assets/b736cb38-3fe9-4d5a-bd0f-0372dea60ca1)

> The extension UI upon launch, showing zero tracked time and no blocked sites. Clean and minimal interface built with React.

---

### 🚫 2. Blocking a Website – Input Form
![Image](https://github.com/user-attachments/assets/7a0fed87-9c57-4afb-99ae-a10a6252a326)
> User enters a distracting site (e.g., Spotify) along with a reason for blocking it. This demonstrates the dynamic input form.

---

### ✅ 3. Website Successfully Blocked
![Image](https://github.com/user-attachments/assets/1bcab818-f656-4fb3-95f3-1c7109b8a3f2)

> Once submitted, the site appears in the blocklist with the reason shown. Users can also remove it from the list if needed.

---

### ⚠️ 4. Blocked Site Redirect Attempt
![Image](https://github.com/user-attachments/assets/b749dc7d-64d2-4d13-bb97-5579a9272e65)
> When trying to access a blocked site, the extension attempts to redirect to a custom "Blocked Page". In this case, `blocked.html` is missing, triggering a file not found error — useful for debugging.

---

### 📊 5. Website Activity Tracking
![Image](https://github.com/user-attachments/assets/a6c0f63f-fd63-4c0d-98c7-f7e610918f30)
> Real-time tracking logs visited domains and displays them along with the time spent. This image shows usage data for sites like YouTube and ChatGPT.

---

### ⏱️ 6. Usage Summary – Time Analytics
![Image](https://github.com/user-attachments/assets/4c7cf7ff-7290-4c56-bb73-29edc0c191a7)
> The summary section displays total time spent online per session or day. Helps users analyze their productivity habits over time.

---

### 🧩 7. Chrome Extensions Page
![Image](https://github.com/user-attachments/assets/3a0e53e0-7a20-43af-909e-5006f63416bb)
> The Productivity Tracker extension installed and active in the Chrome Extensions panel, confirming it was built and loaded successfully using Manifest V3.






