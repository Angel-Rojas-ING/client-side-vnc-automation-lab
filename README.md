# 🎯 Lab 1.4 Auto-Exploit Framework

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Bash](https://img.shields.io/badge/Bash-5.0%2B-green.svg)](https://www.gnu.org/software/bash/)
[![Metasploit](https://img.shields.io/badge/Metasploit-Framework-red.svg)](https://www.metasploit.com/)
[![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-blue.svg)](https://www.kali.org/)

## 📋 Descripción

**Lab 1.4 Auto-Exploit Framework** es un script de automatización completo para el laboratorio de explotación client-side del curso de Ethical Hacking. Este framework automatiza todo el proceso desde la generación del payload hasta el establecimiento de una sesión VNC, eliminando la necesidad de ejecutar comandos manualmente.

### 🚀 Características Principales

- ✅ **Automatización Completa**: Desde la generación del payload hasta VNC
- 🔍 **Detección Inteligente**: Detecta automáticamente IP, interfaz y configuración del sistema
- 📦 **Gestión de Dependencias**: Instala automáticamente las herramientas necesarias
- 🎨 **Interfaz Visual**: Banner colorido y mensajes informativos con emojis
- 🛡️ **PowerSploit Integration**: Descarga y ejecuta PowerUp.ps1 automáticamente
- 🖥️ **VNC Automático**: Establece sesión VNC sin intervención manual
- 🔧 **Error Handling**: Manejo robusto de errores y limpieza automática

## 🎬 Demo

```bash
        ╔════════════════════════════════════════════════════╗
        ║                                                    ║
        ║   🎯 Lab 1.4: Client-Side Exploit to VNC Session  ║
        ║   💀 Desarrollado por The-White-Hat 🎩            ║
        ║   🚀 ¡Suerte en tu aventura de hacking ético!     ║
        ║                                                    ║
        ╚════════════════════════════════════════════════════╝

¡Pana, bienvenido al script para el Lab 1.4: Client-Side Attack!
⚠️ Ojo: Esto es solo para laboratorios con permiso. ¡Sé ético, pana!
```

## 📦 Instalación

### Prerrequisitos

- Kali Linux 2024.x o superior
- Conexión a Internet
- Permisos de sudo

### Instalación Rápida

```bash
# Clonar el repositorio
git clone https://github.com/Angel-Rojas-ING/client-side-vnc-automation-lab.git

# Entrar al directorio
cd lab14-auto-exploit

# Dar permisos de ejecución
chmod +x lab14_auto_exploit.sh

# Ejecutar el script
./lab14_auto_exploit.sh
```

## 🔧 Uso

### Ejecución Básica

```bash
./lab14_auto_exploit.sh
```

### Flujo de Trabajo

1. **Preparación del Atacante**
   - El script detecta tu configuración de red
   - Genera el payload malicioso
   - Descarga PowerSploit automáticamente
   - Inicia servidor web HTTP

2. **Acciones en la Víctima (Windows)**
   ```
   1. Desactivar Windows Defender temporalmente
   2. Navegar a http://[IP_ATACANTE]:8000/
   3. Descargar Prueba.exe
   4. Ejecutar como Administrador
   ```

3. **Post-Explotación Automática**
   - Upload de PowerUp.ps1
   - Ejecución de análisis de privilegios
   - Establecimiento de sesión VNC

## 🛠️ Configuración

### Variables Personalizables

```bash
LPORT="4444"              # Puerto para meterpreter
HTTP_PORT="8000"          # Puerto para servidor web
PAYLOAD_NAME="Prueba.exe" # Nombre del payload
```

### Estructura de Archivos

```
lab14-auto-exploit/
├── lab14_auto_exploit.sh   # Script principal
├── README.md               # Este archivo
└── LICENSE                 # Licencia MIT
```

## 📊 Características Técnicas

### Herramientas Utilizadas

- **Metasploit Framework**: Handler y post-explotación
- **msfvenom**: Generación de payloads
- **PowerSploit**: Escalación de privilegios
- **Python3**: Servidor HTTP
- **TightVNC**: Sesión remota de escritorio

### Automatización Implementada

```ruby
# Ruby embebido en Metasploit para automatización
<ruby>
while framework.sessions.length == 0
  sleep 1
end
session = framework.sessions.first[1]
# Ejecutar comandos automáticamente...
</ruby>
```

## 🐛 Solución de Problemas

### La sesión no se establece

```bash
# Verificar conectividad
ping [IP_VICTIMA]

# Verificar puerto
netstat -tlnp | grep 4444

# Verificar firewall
sudo iptables -L
```

### PowerUp.ps1 no se ejecuta

- Asegurarse de que PowerShell esté habilitado en la víctima
- Verificar que Windows Defender esté desactivado
- Comprobar permisos de administrador

### VNC no inicia

```bash
# Instalar TightVNC
sudo apt update && sudo apt install xtightvncviewer
```

## 🔒 Consideraciones de Seguridad

> ⚠️ **ADVERTENCIA**: Este script es ÚNICAMENTE para uso en entornos de laboratorio controlados con autorización explícita.

- ❌ **NO** usar en sistemas sin autorización
- ❌ **NO** usar en redes públicas
- ✅ **SÍ** usar solo en laboratorios éticos
- ✅ **SÍ** obtener permiso por escrito

## 📚 Documentación Adicional

### Logs y Debugging

El script genera logs temporales en:
- `/tmp/lab14_handler.rc` - Configuración del handler
- `/tmp/lab14_commands.rc` - Comandos de automatización

### Limpieza

El script limpia automáticamente:
- Procesos del servidor web
- Archivos temporales
- Sesiones huérfanas

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Fork el proyecto
2. Crea tu feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push al branch (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📜 Licencia

Este proyecto está licenciado bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 👨‍💻 Autor

**The-White-Hat** 🎩

- GitHub: [@The-White-Hat]([https://github.com/The-White-Hat](https://www.linkedin.com/in/angel-gabriel-gil-rojas-8b7933343/))
- Proyecto: Lab 1.4 Automation

## 🙏 Agradecimientos

- Comunidad de Kali Linux
- Equipo de Metasploit
- PowerShellMafia por PowerSploit
- Todos los estudiantes de hacking ético

---

<p align="center">
  Hecho con ❤️ para la comunidad de hacking ético
</p>

<p align="center">
  <i>Recuerda: Con gran poder viene gran responsabilidad 🕷️</i>
</p>
