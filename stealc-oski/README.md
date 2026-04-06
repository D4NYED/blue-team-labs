# 💀 Análisis de malware Stealc (Lab Oski – CyberDefenders)

Análisis de un malware tipo stealer (Stealc) basado en datos de sandbox (Any.Run) y fuentes OSINT (VirusTotal).

---

## 🧠 Visión general

Un archivo PPT malicioso desencadena la ejecución de un stealer que:

- Extrae credenciales de navegadores  
- Se comunica con un servidor C2  
- Se autoelimina tras la ejecución  

---

## ⚙️ Cadena de ejecución

VPN.exe → cmd.exe → timeout.exe

---

## 🔍 Hallazgos clave

- **Servidor C2:** 171.22.28.221  
- **Acceso a credenciales:** T1555 (Credentials from Password Stores)  
- **Objetivo:** datos de navegadores (Chrome, Firefox, Edge)  
- **DLL clave:** sqlite3.dll  
- **Clave RC4:** 5329514621441247975720749009  
- **Ruta de limpieza:** C:\ProgramData  
- **Tiempo de autoeliminación:** 5 segundos  

---

## 🧾 Indicadores de Compromiso (IOCs)

- IP: 171.22.28.221  
- URL: http://171.22.28.221/5c06c05b7b34e8e6.php  
- Archivo: sqlite3.dll  
- SHA256: a040a0af8697e30506218103074c7d6ea77a84ba3ac1ee5efae20f15530a19bb  

---

## 🔗 Writeup completo

👉 Medium: [PEGA AQUÍ TU LINK]

---

## 🚨 Insight clave

Este malware no es sofisticado, pero es altamente efectivo debido a:

- La rapidez de ejecución  
- El uso de herramientas legítimas (cmd.exe)  
- La eliminación rápida de artefactos  

---

## 🎯 MITRE ATT&CK

- Initial Access  
- Execution  
- Credential Access (T1555)  
- Command and Control  
- Exfiltration  
- Defense Evasion  

---

## ⚠️ Nota final

El verdadero reto no es analizar malware en un sandbox,  
sino detectar este comportamiento en entornos reales sin herramientas de visibilidad.
Enfocado en Blue Team, análisis de malware y detección basada en comportamiento.

## 👤 Sobre mí
Actualmente desarrollando habilidades en:
- Threat Intelligence  
- SOC Detection  
- MITRE ATT&CK  

🔗 LinkedIn: https://linkedin.com/in/d4nyed
