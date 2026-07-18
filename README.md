# Weather Data Analysis and Smart Cooling System Control using MATLAB Simulink

> **A beginner-friendly MATLAB Simulink project that analyzes real weather data and automatically controls a cooling system using IF–ELSE logic based on Temperature and Solar Irradiance.**

---

## 📌 Project Overview

This project demonstrates how MATLAB Simulink can be used to analyze weather parameters and make real-time control decisions.

The system reads weather data from an Excel file and continuously monitors:

* 🌬 Wind Speed
* 🌡 Temperature
* 💧 Humidity
* ☀ Solar Irradiance

Based on predefined conditions, the model automatically decides whether the cooling system should be **ON** or **OFF**.

### Control Logic

```text
IF Temperature > 25°C
AND Solar Irradiance > 50 W/m²

        Cooling System = ON

Else

        Cooling System = OFF
```

---

# 🚀 Features

* Import Weather Data from Excel
* MATLAB Workspace Integration
* Simulink Weather Data Processing
* IF–ELSE Logic Based Control
* Temperature Threshold Detection
* Solar Irradiance Threshold Detection
* Automatic Cooling System Decision
* Real-Time Signal Visualization
* Beginner Friendly Simulink Design

---

# 🛠 Software Used

| Software        | Version                |
| --------------- | ---------------------- |
| MATLAB          | R2024a / MATLAB Online |
| Simulink        | Latest Version         |
| Microsoft Excel | Weather Dataset        |

---

# 📂 Project Structure

```text
Weather_Data_Analysis/
│
├── Weather_Data_Analysis.slx
├── Kolkata_Weather_Data.xlsx
├── README.md
├── images/
│   ├── simulink_model.png
│   ├── scope_all_signals.png
│   └── scope_cooling_logic.png
│
└── dataset/
    └── Kolkata_Weather_Data.xlsx
```

---

# 📊 Weather Dataset

The dataset contains hourly weather information.

| Parameter        | Unit |
| ---------------- | ---- |
| Time             | Hour |
| Wind Speed       | km/h |
| Temperature      | °C   |
| Humidity         | %    |
| Solar Irradiance | W/m² |

---

# ⚙ Working Principle

The workflow of the project is shown below.

```text
Excel Weather Data
          │
          ▼
MATLAB Workspace
          │
          ▼
From Workspace Block
          │
          ▼
Demux Block
          │
 ┌────────┼────────┬──────────┐
 │        │        │          │
Wind  Temperature Humidity Irradiance
          │                    │
          │                    │
          └──────┬─────────────┘
                 ▼
          IF–ELSE Logic
                 │
                 ▼
        Cooling System Control
                 │
                 ▼
              Scope
```

---

# 🧠 IF–ELSE Logic

The cooling system follows this decision rule.

```text
IF

Temperature > 25°C

AND

Solar Irradiance > 50 W/m²

THEN

Cooling System = ON

ELSE

Cooling System = OFF
```

---

# 📸 Simulink Model

```markdown
## Simulink Model

( https://github.com/Ayancoder1/Weather-Data-Analysis-Simulink/blob/main/Simulink_model.png )
```

---

# 📈 Weather Signal Analysis

The first scope displays all weather parameters.

* Wind Speed
* Temperature
* Humidity
* Solar Irradiance

```markdown
## Weather Signals

( https://github.com/Ayancoder1/Weather-Data-Analysis-Simulink/blob/main/Scope_all_signals.png )
```

---

# 📊 Cooling System Decision

The second scope displays

* Temperature
* Solar Irradiance
* Cooling System Status

```markdown
## Cooling System Logic

( https://github.com/Ayancoder1/Weather-Data-Analysis-Simulink/blob/main/Scope_cooling_logic.png )
```

---

# ▶ How to Run the Project

### Step 1

Clone the repository.

```bash
git clone https://github.com/yourusername/Weather-Data-Analysis-Simulink.git
```

---

### Step 2

Open MATLAB.

---

### Step 3

Open

```text
Weather_Data_Analysis.slx
```

---

### Step 4

Import

```text
Kolkata_Weather_Data.xlsx
```

into the MATLAB Workspace.

---

### Step 5

Run the preprocessing script if required.

```matlab
weather = table2array(Kolkata_Weather_Data_Sheet1(:,2:5));

t = hours(Kolkata_Weather_Data_Sheet1.Time - Kolkata_Weather_Data_Sheet1.Time(1));

weatherMatrix = [t weather];
```

---

### Step 6

Click

```text
Run Simulation
```

---

### Step 7

Observe

* Weather Parameters
* Cooling Decision
* Scope Outputs

---

# 📊 Results

The model successfully

* Reads weather data from Excel
* Separates all weather parameters
* Monitors temperature
* Monitors solar irradiance
* Applies IF–ELSE logic
* Turns the cooling system ON only when both conditions are satisfied
* Displays all signals in real time using Scope blocks

---

# 📚 Simulink Blocks Used

| Block          | Purpose                  |
| -------------- | ------------------------ |
| From Workspace | Import weather data      |
| Demux          | Separate weather signals |
| Switch         | IF–ELSE implementation   |
| Constant       | Threshold values         |
| Scope          | Signal visualization     |

---

# 🎯 Applications

* Smart Building Automation
* HVAC Control Systems
* Solar Power Plants
* Greenhouse Temperature Control
* Smart City Projects
* Renewable Energy Monitoring
* Industrial Cooling Systems

---

# 🔮 Future Improvements

* Add Humidity-based control logic
* Integrate IoT sensors for live weather data
* Connect ESP32/Arduino hardware
* Build a real-time dashboard using MATLAB App Designer
* Add AI-based cooling prediction
* Integrate PV panel efficiency monitoring

---

# 👨‍💻 Author

**Ayan Kar**

Electrical Engineering Student

Narula Institute of Technology

---

# ⭐ Support

If you found this project helpful:

⭐ Star this repository

🍴 Fork the project

📢 Share it with others

---

# 📄 License

This project is released under the **MIT License**.
