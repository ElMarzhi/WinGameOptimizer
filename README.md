# 🎮 WinGameOptimizer v1.8.1

[![Release](https://img.shields.io/badge/Release-v1.8.1-00D2FF?style=for-the-badge&logo=windows)](https://github.com/elmarzhi/WinGameOptimizer/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(x64)-blue?style=for-the-badge&logo=windows11)](https://github.com/elmarzhi/WinGameOptimizer)
[![Framework](https://img.shields.io/badge/.NET%208.0-Self--Contained-purple?style=for-the-badge&logo=dotnet)](https://dotnet.microsoft.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE.txt)
[![VirusTotal](https://img.shields.io/badge/VirusTotal-100%25%20Clean-emerald?style=for-the-badge&logo=virustotal)](https://www.virustotal.com/)

> **WinGameOptimizer** es una suite de optimización de baja latencia y alto rendimiento diseñada para jugadores competitivos y entusiastas de Windows 10 y 11. Elimina el bloatware en segundo plano, neutraliza el input lag de ratón y teclado, prioriza el hilo de tu juego activo y repara componentes corruptos del sistema operativo sin comprometer la estabilidad.

---

## 🛡️ Enlace de Análisis de Seguridad (VirusTotal)
- **Análisis de WinGameOptimizer.exe v1.8.1**: `[PEGA AQUÍ TU ENLACE DE VIRUSTOTAL TRAS EL ESCANEO]`
- **Hash SHA-256 Oficial**: `382669BA60381C140743660F03FD9BEEBB5378E011B2673F08EA884BD81CED68`

---

## 🚀 Principales Características y Módulos

### 1. 🖱️ Periféricos y Zero Input Lag (eSports)
- **Curva Lineal Pura de Ratón (MarkC Fix Canónico 1:1)**: Sustituye la tabla de aceleración oculta de Windows por la rampa lineal matemática pura en punto fijo 16.16 (pendiente constante $3.5\times$ para sensibilidad 6/11 a 100% DPI).
- **FilterKeys Competitive Preset**: Ajusta el retardo de repetición y aceptación a latencia mínima ultra-reactiva para strafe instantáneo en shooters sin doble pulsación accidental.
- **Optimización de Búfer de Kernel (Mouse & Keyboard Queue Size)**: Reduce la cola de eventos en `mouclass` y `kbdclass` para ratones de 1000 Hz, 4000 Hz u 8000 Hz.
- **Desactivación de Ahorro de Energía USB/HID**: Evita micro-cortes y caídas de voltaje en puertos USB durante partidas intensas.
- **Supresión de Interceptores de Accesibilidad**: Desactiva el retardo de teclado provocado por StickyKeys, ToggleKeys y MouseKeys.

### 2. 🎮 Modo Gaming Inteligente (Reducción de Procesos en 1 Clic)
- **Cierre Seguro de Procesos No Críticos**: Finaliza actualizadores y telemetría en segundo plano (`OneDrive`, `GoogleUpdate`, `EdgeUpdate`, `NvTelemetry`, etc.).
- **Opciones Flexibles para Jugadores**: Casillas opcionales (desmarcadas por defecto) para Discord, Spotify y SteamWebHelper.
- **Protección Anticheats y Sistema**: Protección de procesos vitales (`RiotClientServices`, `valorant`, `vgc`, `vgtray`, `EasyAntiCheat`, `BattlEye`, etc.).
- **Purga de Memoria Standby**: Recupera memoria RAM en espera instantáneamente mediante llamadas directas al kernel (`NtSetSystemInformation`).
- **Restauración a Modo Estándar**: Relanza automáticamente las aplicaciones cerradas del usuario al finalizar la sesión de juego.

### 3. ⚡ Latencia de CPU y GPU
- **Win32PrioritySeparation = 38**: Otorga la máxima prioridad y los intervalos de reloj de CPU más amplios a la ventana en primer plano.
- **Desactivación de GameDVR**: Elimina la captura constante de pantalla de Windows en segundo plano.
- **Desactivación de Ahorro PCIe (ASPM)**: Mantiene el enlace PCI Express de la GPU siempre en rendimiento máximo.
- **NVIDIA Low Latency & Shader Cache Ilimitado**: Reduce el pre-renderizado de frames y previene micro-stutters por compilación de shaders.
- **Desactivación de MPO (Multiplane Overlay)**: Soluciona parpadeos, micro-congelamientos y pantallas negras del DWM en drivers gráficos.

### 4. 🛠️ Reparador de Errores Todo-en-Uno (Inspirado en WinUtil / Tweaking)
- **Motor DISM & SFC**: Comprobación y reparación profunda de la imagen de Windows con consola en vivo.
- **Reparación WMI**: Comprobación de coherencia y salvamento del repositorio WMI corrupto.
- **Reset de Windows Update y Criptografía**: Limpieza de carpetas `SoftwareDistribution` y reconstrucción de `catroot2`.
- **Restablecimiento de Red y Winsock**: Flush de DNS, liberación/renovación IP y reseteo completo del catálogo de red.
- **Reparación de Microsoft Store, UWP e IconCache**: Ejecución de `wsreset.exe`, re-registro de paquetes Appx y regeneración de `IconCache.db` y `FontCache*`.
- **Salud de Disco (CHKDSK)**: Escaneo en línea de unidades SSD/NVMe.

---

## 🔒 Portabilidad y Seguridad Absoluta
- **100% Portable**: No requiere instalación. Todo se ejecuta desde una única carpeta.
- **Backups Automáticos Reales**: Antes de cambiar cualquier valor del registro o de un servicio, WinGameOptimizer genera un archivo `.reg` y un respaldo de estado JSON en `./backups/`.
- **Reversión en 1 Clic**: El botón `"↩️ Revertir Cambios"` restaura los valores exactos que tenía el equipo del usuario previamente.

---

## ⚠️ Nota Importante sobre Windows SmartScreen

Al ser una aplicación de código abierto de distribución independiente, Windows Defender SmartScreen podría mostrar una alerta inicial:
> *"Windows protegió su PC - Microsoft Defender SmartScreen impidió el inicio de una aplicación desconocida."*

### ¿Por qué ocurre esto?
Microsoft exige comprar certificados comerciales anuales extremadamente costosos para evitar este aviso en aplicaciones nuevas.

### Cómo iniciarlo:
1. Haz clic en **"Más información"** (*More info*).
2. Haz clic en el botón **"Ejecutar de todas formas"** (*Run anyway*).
3. Concede permisos de **Administrador** (imprescindibles para modificar claves del registro de baja latencia).

---

## 📬 Contacto y Soporte
- **Autor**: elmarzhi
- **Soporte Oficial y Dudas**: `contacto.elmarzhi@gmail.com`
- **Reportes de Fallos**: Mediante la pestaña integrada "Dudas y Sugerencias" en el programa o a través de [GitHub Issues](https://github.com/elmarzhi/WinGameOptimizer/issues).
