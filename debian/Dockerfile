FROM debian:bullseye-slim

# Mettez à jour les informations des paquets et installez les packages que vous souhaitez
RUN apt-get update && apt-get install -y \
    openssh-server \
    ltrace \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
run echo "Welcome with the <3 from wyene, thanks you for using my awesome open source tools to create sandbox">/etc/motd 
