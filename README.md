# 🧳 Smart Travel Planner – UiPath Automation Project (Basic Prototype Version)

The **Smart Travel Planner** is a fully automated RPA bot built using **UiPath Studio** that generates a personalized travel itinerary based on user input. It integrates Google Maps APIs to fetch durations and images of places and delivers a polished Word document via email.

---

## 🚀 Features

- 🧠 Collects user input for **destination city, number of days** and **email**
- 🗺️ Fetches **popular tourist places** dynamically using **Google Maps APIs**
- 🖼️ Downloads **images** of each place for visual appeal
- 📄 Automatically creates a **professional travel itinerary (Word document)**:
  - Includes place names, durations, and images
  - No travel time included for simplicity
- ✉️ Sends the itinerary directly to the user via **email**
- 🧪 Built-in **error handling** for:
  - Invalid city names
  - Non-numeric or blank input
- ✅ All automation is built in a **single `MAIN.xaml`** file for simplicity

---

## 🛠️ Tech Stack

- **UiPath Studio** – RPA platform for building the automation
- **Google Maps API** – To fetch place names, durations, and images
- **Microsoft Word Activities** – For generating and formatting the itinerary
- **SMTP Email Activities** – To send the final Word document via email
- **.NET Regex & String Manipulation** – For input validation and cleanup

---

## 🖥️ Workflow Overview

1. **Prompt User**:
   - Ask for destination city, number of days and email
2. **Validate Input**:
   - Re-prompt on invalid data (e.g., typos or non-numeric values)
3. **Fetch Data**:
   - Get up to `n` popular places for the city (limited to entered number of days)
   - Download images for each place
4. **Build Word Document**:
   - For each day, add a place with its name and image
   - Format document for clean presentation
5. **Send Email**:
   - Attach the generated document and email it to the user
6. **End Process**

---

## 📁 Folder Structure
```
SmartTravelPlanner/
│
├── MAIN.xaml                   # Main workflow file
├── project.json                # UiPath project file
├── Resources/
│   ├── Images/                 # Temp storage for downloaded images
│   └── Templates/              # Word templates (if any used)
└── Output/
└── Itinerary.docx          # Final Word document generated
```
---

## 📧 How to Use

1. Open **UiPath Studio**
2. Load the `MAIN.xaml` file
3. Run the bot
4. Enter your travel details when prompted
5. Wait for the automatic word document creation and email of the word doc with your personalized itinerary!

---

## 📌 Notes

- Make sure you have a valid **Google Maps API Key**
- Ensure email credentials are configured securely in **Orchestrator Assets** or as **secure variables**
- Word and Internet access are required for full functionality

---

## 🧠 Author

**Varun Rewadi**  
Passionate about building stuff.

---

## 📃 License

This project is open-source and free to use for personal or academic purposes. Reach out for collaborations or improvements!

---
