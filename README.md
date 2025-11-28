🇪🇸 Versión en Español: [Leer aquí](./README.es.md)

<div align="center">

# SIMA Parking

![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=java&logoColor=white)
![Retrofit](https://img.shields.io/badge/Retrofit-Networking-673AB7?style=flat-square&logo=square&logoColor=white)
![Gson](https://img.shields.io/badge/Gson-Serialization-4285F4?style=flat-square&logo=google&logoColor=white)
![Material Design](https://img.shields.io/badge/Material_Design-757575?style=flat-square&logo=material-design&logoColor=white)

</div>

<br />

### Created by Diego Rivera

## 📋 Executive Summary

**SIMA Parking** is a native Android application designed to digitize and streamline the operational management of parking facilities. It provides a robust interface for security personnel and administrators to control vehicle access, manage parking spaces, and calculate fees automatically.

The system acts as a mobile client that interacts with a backend server, ensuring real-time data consistency regarding occupancy, staff management, and revenue tracking. It replaces manual ticketing systems with a digital, error-free solution.

## ✨ Key Features

*   **Vehicle Access Control:** efficient registration of vehicle entries and exits using license plate numbers.
*   **Automated Billing:** Real-time calculation of parking fees based on entry/exit timestamps and configurable tariffs.
*   **Space Management:** Monitoring of parking slot availability and status updates.
*   **Role-Based Access:** Distinct functional modules for Administrators (CRUD operations) and Employees (Operational tasks).
*   **User Management:** Complete administration system to manage staff credentials and roles.
*   **Tariff Configuration:** Dynamic adjustment of pricing models directly from the app.

## 🏗️ Architecture

The application follows a **Client-Server Architecture** utilizing standard Android development patterns:

1.  **Presentation Layer (UI):**
    *   Built using **Fragments** (`Registro_fragment`, `Tarifa_fragment`) hosted within a main Activity.
    *   Utilizes **Material Design** components and an **Animated Bottom Bar** for intuitive navigation.
    *   Implements a Navigation Drawer for accessing secondary modules (Profile, Location, etc.).

2.  **Networking Layer:**
    *   **Retrofit 2:** Handles all HTTP requests to the REST API.
    *   **Gson:** Manages serialization and deserialization of JSON data.
    *   **RetrofitClient:** A singleton pattern implementation that provides a configured Retrofit instance pointing to the backend server.

3.  **Data Models:**
    *   POJOs (`Registro`, `Usuario`, `Tarifa`, `Espacio`) represent the business entities and mirror the database schema.

## 🛠️ Tech Stack

*   **Language:** Java
*   **Core:** Android SDK (Min SDK 26, Target SDK 33)
*   **Networking:** Retrofit 2, OkHttp, Gson
*   **UI Components:** 
    *   ConstraintLayout & LinearLayout
    *   RecyclerView & CardView
    *   AnimatedBottomBar
    *   FancyToast (Custom alerts)
*   **Build System:** Gradle

## 🚀 Installation & Setup

### Prerequisites
*   Android Studio Flamingo or newer
*   Java Development Kit (JDK) 8 or higher
*   A running instance of the backend server (ensure the IP in `RetrofitClient.java` matches your server).

### Steps

1.  **Clone the repository**
    ```bash
    git clone https://github.com/your-username/sima-parking.git
    ```

2.  **Configure Backend Endpoint**
    Open `app/src/main/java/com/example/finalproyect/RetrofitClient.java` and update the `BASE_URL` with your local or remote server IP:
    ```java
    static final String BASE_URL = "http://YOUR_SERVER_IP:8080";
    ```

3.  **Build the Project**
    *   Open the project in Android Studio.
    *   Sync Gradle files.

4.  **Run the Application**
    *   Connect an Android device or start an Emulator.
    *   Click **Run 'app'**.

---
*© 2023 Diego Rivera. All Rights Reserved.*
