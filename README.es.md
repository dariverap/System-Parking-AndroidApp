🇺🇸 English Version: [Read here](./README.md)

<div align="center">

# SIMA Parking

![Android](https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=android&logoColor=white)
![Java](https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=java&logoColor=white)
![Retrofit](https://img.shields.io/badge/Retrofit-Networking-673AB7?style=flat-square&logo=square&logoColor=white)
![Gson](https://img.shields.io/badge/Gson-Serialization-4285F4?style=flat-square&logo=google&logoColor=white)
![Material Design](https://img.shields.io/badge/Material_Design-757575?style=flat-square&logo=material-design&logoColor=white)

</div>

<br />

### Creado por Diego Rivera

## 📋 Resumen Ejecutivo

**SIMA Parking** es una aplicación nativa de Android diseñada para digitalizar y optimizar la gestión operativa de estacionamientos. Proporciona una interfaz robusta para que el personal de seguridad y administradores controlen el acceso vehicular, gestionen los espacios de aparcamiento y calculen tarifas automáticamente.

El sistema actúa como un cliente móvil que interactúa con un servidor backend, asegurando la consistencia de datos en tiempo real sobre la ocupación, gestión de personal y seguimiento de ingresos. Reemplaza los sistemas manuales de tickets con una solución digital libre de errores.

## ✨ Características Principales

*   **Control de Acceso Vehicular:** Registro eficiente de entradas y salidas de vehículos utilizando números de patente.
*   **Facturación Automatizada:** Cálculo en tiempo real de las tarifas de estacionamiento basado en marcas de tiempo de entrada/salida y tarifas configurables.
*   **Gestión de Espacios:** Monitoreo de la disponibilidad y actualización del estado de las plazas de aparcamiento.
*   **Acceso Basado en Roles:** Módulos funcionales distintos para Administradores (operaciones CRUD) y Empleados (tareas operativas).
*   **Gestión de Usuarios:** Sistema completo de administración para gestionar credenciales y roles del personal.
*   **Configuración de Tarifas:** Ajuste dinámico de modelos de precios directamente desde la aplicación.

## 🏗️ Arquitectura

La aplicación sigue una **Arquitectura Cliente-Servidor** utilizando patrones estándar de desarrollo en Android:

1.  **Capa de Presentación (UI):**
    *   Construida usando **Fragments** (`Registro_fragment`, `Tarifa_fragment`) alojados dentro de una Activity principal.
    *   Utiliza componentes de **Material Design** y una **Animated Bottom Bar** para una navegación intuitiva.
    *   Implementa un Navigation Drawer para acceder a módulos secundarios (Perfil, Ubicación, etc.).

2.  **Capa de Red:**
    *   **Retrofit 2:** Maneja todas las solicitudes HTTP hacia la API REST.
    *   **Gson:** Gestiona la serialización y deserialización de datos JSON.
    *   **RetrofitClient:** Implementación del patrón Singleton que proporciona una instancia configurada de Retrofit apuntando al servidor backend.

3.  **Modelos de Datos:**
    *   POJOs (`Registro`, `Usuario`, `Tarifa`, `Espacio`) que representan las entidades del negocio y reflejan el esquema de la base de datos.

## 🛠️ Stack Tecnológico

*   **Lenguaje:** Java
*   **Core:** Android SDK (Min SDK 26, Target SDK 33)
*   **Red:** Retrofit 2, OkHttp, Gson
*   **Componentes UI:** 
    *   ConstraintLayout & LinearLayout
    *   RecyclerView & CardView
    *   AnimatedBottomBar
    *   FancyToast (Alertas personalizadas)
*   **Sistema de Construcción:** Gradle

## 🚀 Instalación y Configuración

### Prerrequisitos
*   Android Studio Flamingo o superior
*   Java Development Kit (JDK) 8 o superior
*   Una instancia en ejecución del servidor backend (asegúrese de que la IP en `RetrofitClient.java` coincida con su servidor).

### Pasos

1.  **Clonar el repositorio**
    ```bash
    git clone https://github.com/tu-usuario/sima-parking.git
    ```

2.  **Configurar Endpoint del Backend**
    Abra `app/src/main/java/com/example/finalproyect/RetrofitClient.java` y actualice la `BASE_URL` con la IP de su servidor local o remoto:
    ```java
    static final String BASE_URL = "http://TU_IP_SERVIDOR:8080";
    ```

3.  **Construir el Proyecto**
    *   Abra el proyecto en Android Studio.
    *   Sincronice los archivos Gradle (Sync Project with Gradle Files).

4.  **Ejecutar la Aplicación**
    *   Conecte un dispositivo Android o inicie un Emulador.
    *   Haga clic en **Run 'app'**.

---
*© 2023 Diego Rivera. Todos los derechos reservados.*
