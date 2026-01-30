```markdown
# 📡 Military Pager Communication System  

*A Cyber-Physical System (CPS) inspired military pager communication prototype using ESP32, LoRa (SX1278), and LCD interfaces.*

The system enables **secure, long-range, low-power message exchange** between field nodes and a central base station — **without relying on cellular or internet infrastructure**.

---

## 🛡️ Project Motivation  

Modern defense communication demands:

- Infrastructure-independent operation  
- Low power consumption  
- Long-range connectivity  
- Secure and reliable messaging  

This project **revives the military pager concept using CPS principles**, making it suitable for **remote, tactical, and emergency environments**.

---

## 🧠 System Overview  

The system consists of:

- **Two Field Nodes (Soldier Units)**  
- **One Base Station (Command Unit)**  

All devices communicate using **LoRa**, ensuring robustness in **low-connectivity or hostile environments**.

---

## 🔗 Communication Flow  

```

Node 1  ⇄  Base Station  ⇄  Node 2

```

Messages are routed through the **base station** using a **structured packet format** and validated using **CRC**.

---

## 🔧 Hardware Components  

| Component | Description |
|---------|-------------|
| **ESP32** | Main controller (dual-core, low power, SPI/I2C support) |
| **LoRa SX1278 / SX1276** | Long-range wireless communication |
| **16×2 LCD / I2C LCD** | Message display at nodes |
| **433/868 MHz Antenna** | Improves communication range |
| **Push Buttons & LEDs** | Message trigger and status indication |
| **5V Power Supply** | USB-powered prototype |

---

## 🧩 Software & Tools  

- Arduino IDE  
- ESP32 Board Support Package  
- LoRa Library (SX127x)  
- KiCad – Circuit design & simulation  
- C/C++ (Embedded Programming)  

---

## 📦 Message Packet Format  

Each message follows a **standardized structure**:

```

TransID : SenderID : ReceiverID : Message

```

**Example:**
```

B:1:2:Send Backup

```

| Field | Meaning |
|-----|--------|
| **TransID** | B = Base Station, N = Node |
| **SenderID** | Transmitting node ID |
| **ReceiverID** | Destination node ID |
| **Message** | Command / Text |

---

## 🔄 Communication Algorithm (Summary)  

1. Initialize ESP32, LoRa, and LCD  
2. Wait for button press or incoming packet  
3. Encrypt and transmit message via LoRa  
4. Verify CRC on reception  
5. Route message if base station  
6. Display message on LCD  
7. Monitor RSSI for link quality  

---

## 📶 Performance Highlights  

### 📡 Range  
- ~50 m (without antenna)  
- ~1 km (urban with antenna)  
- Up to ~2.8 km (open terrain)  

### 📊 RSSI  
- Best: **−10 dBm**  
- Minimum usable: **−115 dBm**  

### 📈 SNR  
- Average: **9–11 dB**  

### 🔋 Power  
- Suitable for long-duration field operation  

---

## 🔐 Security Features  

- CRC validation for error detection  
- Encrypted payload (software-level)  
- FHSS compatibility (anti-jamming & interception resistance)  

---

## 🚀 Future Enhancements  

- 🔑 RSA + AES hybrid encryption  
- 🕸️ LoRa mesh networking  
- 📍 GPS-based time synchronization  
- 🆘 Morse-code silent emergency signaling  
- 🔋 Deep-sleep power optimization  

---

## 🧪 Applications  

- Military field communication  
- Disaster response coordination  
- Border surveillance  
- Tactical IoT networks  
- Infrastructure-less messaging systems  

---

## 👨‍💻 Contributors  

- **Nihar Prajapati**  
- **Om Hingu**  
- **Om Bharti**  

**Department of Electronics & Communication Engineering**  
Pandit Deendayal Energy University  

---

## 📄 License  

This project is intended for **academic and research purposes**.  
You may add an **MIT / Apache-2.0 license** depending on your preference.

---

## ⭐ Acknowledgements  

- Espressif Systems (ESP32)  
- Semtech (LoRa Technology)  
- IEEE CPS & IoT research community  
```
