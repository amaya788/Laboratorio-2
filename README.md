# 🛰️ Laboratorio 2: Comunicaciones Industriales

**Universidad Santo Tomás**  
**Autores:** Ferney Amaya, David Díaz, Jhonny Mejía  
**Docente:** Ing. Diego A. Barragán  
**Fecha:** Septiembre 2025  

---

## 🎯 Objetivo
Analizar y comparar distintos métodos de **detección y corrección de errores** en comunicación serial (UART).

---

## ⚙️ Metodología
- **Checksum:** verificación básica de errores.  
- **ARQ (ACK/NACK):** retransmisión automática.  
- **VRC y LRC:** comparación de overhead y robustez.  
- **Montaje:** conexión UART entre Raspberry Pi Pico2W y ESP32 con convertidor **MAX3232**.  

---

## 📊 Resultados Clave
- **Checksum** detecta errores simples, pero no corrige.  
- **ARQ simple:** eficiente hasta p=30%, inutilizable con p=90% (hasta 9 retransmisiones).  
- **VRC:** bajo overhead pero detecta solo errores de 1 bit.  
- **LRC:** más robusto, eficiente en bloques grandes (overhead 1% en 100 bytes).  

---

## ✅ Conclusiones
- Protocolos simples funcionan en canales limpios, pero no en entornos ruidosos.  
- **LRC supera a VRC** en detección de errores múltiples y escalabilidad.  
- En la industria se requieren protocolos con **CRC, delimitadores y longitud de trama**.  

---
