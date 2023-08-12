# Minecraft Ubuntu Server Quick Setup Instructions

Set up instructions for a basic minecraft server. Doesn't consider things like server management, networking (port forwarding), or security. Additional commands may be needed to get a basic server up and running.

## Ordered Commands

```
sudo apt update && sudo apt upgrade -y

sudo apt install openjdk-17-jre unzip 

mkdir minecraft_<modpack-name>

cd minecraft_<modpack-name>

wget <serverpack-download-url>

unzip <download-name>

rm <download-name>

cd <unzipped-name>
```

Instuctions may vary here depending on the pack:

```
chmod +x startserver.sh

./startserver.sh
```

Stop server after initial load.

```
nano eula.txt
```
Set to true in eula.

```
screen -d -m -L -S minecraft-server ./run.sh
```

Personal preference is to run the server in GNU screen. Tmux is also a good alternative.
