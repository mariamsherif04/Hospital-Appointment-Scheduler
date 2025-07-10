# 🏥 Digital Hospital Scheduling System
## 📌 Objective

This project aims to **design and implement a digital scheduling system** for a hospital using **combinational and sequential logic components**. The system allows users to:
- Select a **department** and a **doctor** using switches.
- Check a doctor's **real-time availability** displayed through LEDs.

This demonstrates the **practical application of digital logic** in real-world scheduling and management, especially in healthcare.

---

## 🧩 Components

### 🔹 Combinational Components
- **1× Decoder** (74HC139)
- **2× Multiplexers** (74HC153)

### 🔸 Sequential Components
- **2× Shift Registers** (74HC595)

### 🎛️ Input Components
- Switches
- Push Buttons

### 💡 Output Components
- LEDs

### ⚡ Power & Passive Components
- 9V Battery
- Voltage Regulator
- 10kΩ Resistors
- 330Ω Resistors
- Breadboard & Jumper Wires

---

## ⚙️ How the System Works

### 1️⃣ Department Selection
- Two switches select one of four departments.
- Inputs are fed into a **2-to-4 decoder**.
- Decoder outputs enable the **multiplexers**, determining which group of doctors can be selected.

### 2️⃣ Doctor Selection
- Two switches select one of four doctors in the chosen department.
- These connect to the **multiplexer select lines**.

### 3️⃣ Doctor Availability Check
- Multiplexer inputs are connected to stored doctor availability bits.
  - **Available:** HIGH → Green LED ON
  - **Unavailable:** LOW → LED OFF

---

## 💾 Availability Storage: 74HC595 Shift Register

The **74HC595 Serial-In Parallel-Out (SIPO)** register manages the availability status.

- **Data Entry:**
  - Switch connected to **DS (Data Serial)** pin.
    - Closed switch = `1`
    - Open switch = `0`
- **Shifting Data:**
  - Clock pulse to **SH_CP** shifts the bit in.
- **Output Latching:**
  - Latch pulse to **ST_CP** updates the outputs (`Q0–Q7`).

---

## 📄[Project Report](https://drive.google.com/file/d/11pUH_I7eHOqilwGIpeVlpkyg9Sx2fBg5/view?usp=drivesdk) 

## 👥 Team Members 
- [Samar Hatem](https://github.com/samar04052004)
- [Mariam Sherif](https://github.com/mariamsherif04)
