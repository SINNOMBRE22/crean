# clean

Script de limpieza rápida para VPS/servidores Linux (Ubuntu/Debian). Libera espacio eliminando caché de paquetes, logs antiguos, journal, temporales y papelera — con un solo comando.

## 🚀 Instalación

```bash
curl -sSL https://raw.githubusercontent.com/SINNOMBRE22/clean/main/clean.sh -o /usr/local/bin/clean && chmod +x /usr/local/bin/clean
```

## ▶️ Uso

```bash
sudo clean
```

Eso es todo. El script se encarga de:

1. Limpiar caché de paquetes APT (`autoremove`, `clean`, `autoclean`)
2. Vaciar registros del sistema (Journald, límite 50M)
3. Eliminar logs antiguos y comprimidos en `/var/log`
4. Limpiar `/tmp`, `/var/tmp` y caché de usuario
5. Vaciar la papelera del sistema

Al final muestra cuánto espacio liberó y el estado actual del disco.

## 📋 Requisitos

- Linux (Ubuntu / Debian recomendado)
- Permisos de root (`sudo`)

## ⚠️ Notas

- El script solo borra archivos temporales con más de 2 días de antigüedad, para evitar interferir con procesos activos.
- Guarda un log de cada ejecución en `/var/log/sn-cleanup.log`.

## 🔄 Actualizar

Vuelve a correr el comando de instalación; sobrescribe la versión anterior.

## 🗑️ Desinstalar

```bash
sudo rm /usr/local/bin/clean
```

---

Hecho por [SinNombre](https://sinnombre.xyz) — [@SIN_NOMBRE22](https://t.me/SIN_NOMBRE22)
