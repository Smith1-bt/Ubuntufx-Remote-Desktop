# UbuntuFX Docker Image

#### Contact [EFXTv](https://t.me/efxtv) if you need support or want to donate this repository
---

 Ubuntu Desktop XFCE + Firefox in Docker (VNC & noVNC, SSH Ready)

- XFCE4 desktop environment
- Firefox browser
- XFCE4 terminal
- VNC server + noVNC (web-based access)
- SSH server
- Preconfigured XFCE panel with essential applications

You can run a full Ubuntu desktop inside Docker and access it via your browser or a VNC client.

---

## 📦 Pull the Image

You can pull the prebuilt image from Docker Hub:

```bash
docker pull efxtv/ubuntufx
```
---
## 📦 Run container
```
docker run -d \
  -p 22:22 \
  -p 5901:5901 \
  -p 6080:6080 \
  --name ubuntufx \
  efxtv/ubuntufx
```
---

## 📦 Access Methods

### SSH
```
ssh root@localhost -p 22
# password: root
```

### Web Browser (noVNC)
```
Open http://localhost:6080
 in your browser to use the desktop.

 # Managing VNC Server

 # Start VNC server
vncserver :1 -geometry 1920x940 -depth 24

# Stop VNC server
vncserver -kill :1

```
### VNC
```
localhost:5900
```

### 🛠️ Build Locally (Optional)
```
git clone https://github.com/efxtv/ubuntufx-noVNC.git
cd ubuntufx-noVNC
docker build -t ubuntufx .
docker run -d -p 22:22 -p 5901:5901 -p 6080:6080 --name myubuntu ubuntufx
```
---
### 🖥️ Default Setup
- Username: root
- Password (SSH): root
- Password (VNC): rootvnc
- Desktop: XFCE4
- Browser: Firefox
- Terminal: XFCE4 Terminal

### 🔧 Included Tools
- Git, Curl, Wget, Nano
- Python3 + pip
- Zip & Unzip
- OpenSSH server
- XFCE desktop with panel configuration
- noVNC + Websockify for browser access
---
## 📸 Screenshots

## 📸 Screenshots
| ![Startup Script](https://github.com/efxtv/Ubuntufx-Remote-Desktop/raw/main/sample-images/ubuntufx-start.png) | ![XFCE Desktop](https://github.com/efxtv/Ubuntufx-Remote-Desktop/raw/main/sample-images/ubuntufx-xfcd-de.png) |
|---|---|
| **Startup Script Running** | **XFCE Desktop Environment** |

| ![UbuntuFX Main](https://github.com/efxtv/Ubuntufx-Remote-Desktop/raw/main/sample-images/ubuntufxmain.png) | ![SSH Access](https://github.com/efxtv/Ubuntufx-Remote-Desktop/raw/main/sample-images/ubuntufxssh.png) |
|---|---|
| **Main Desktop View** | **SSH Access** |

| ![XFCE Terminal](https://github.com/efxtv/Ubuntufx-Remote-Desktop/raw/main/sample-images/ubuntufx-xfce-terminal.png) |   |
|---|---|
| **XFCE Terminal** |   |


---
BUYME A COFFEE: https://buymeacoffee.com/efxtv





