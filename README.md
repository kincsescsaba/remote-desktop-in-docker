# Alpine docker container image with XFCE4 Desktop for "headless" VNC/RDP environments

Forked from:
https://github.com/soffchen/tiny-remote-desktop/blob/master/Dockerfile

* XFCE4 Desktop Environment with full DateTime on the top in order to get Screenshot Evidences
* xrdp server (default RDP port `3389`)
* vnc server (default VNC port `5901`)
* [**noVNC**](https://github.com/novnc/noVNC) - HTML5 VNC client (default http port `6901`)
* Browsers:
  * Chromium
  * Firefox

## Usage

- Run command with mapping to local port `5901` (vnc protocol) and `6901` (vnc web access) with specific resolution and access password:

      docker run -d -p 5901:5901 -p 6901:6901 -e RESOLUTION=1600x1200 -e VNC_PASSWORD="vncpassword" solinter/remote-desktop-in-docker
