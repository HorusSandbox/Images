FROM debian:bullseye-slim

# Mettez à jour les informations des paquets et installez les packages que vous souhaitez
RUN apt-get update && apt-get install -y \
    openssh-server \
    ltrace \
    telnetd \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*
run echo "\n\n\nWelcome with the <3 from wyene, thanks you for using my awesome open source tools to create sandbox\n\n\n\n">/etc/motd

RUN ssh-keygen -A && sed -i 's/#PasswordAuthentication yes/PasswordAuthentication no/' /etc/ssh/sshd_config

RUN mkdir -p /run/sshd

# Exposez le port SSH (par défaut : 22)
EXPOSE 23

# Activez et démarrez le service SSH au démarrage du conteneur
#CMD ["/usr/sbin/sshd", "-D"]
CMD ["/usr/sbin/in.telnetd", "-debug", "23"]
