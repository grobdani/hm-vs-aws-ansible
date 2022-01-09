# AWS Ansible-Controller

Für die Migration der JMS-Lösung in die Cloud wurde AWS als Cloudplattform verwendet. Damit alle Services kostenlos bereitgestellt werden können wurde auf den EC2 Service gesetzt. Als Distribution wurde Ubuntu 20.04 verwendet.

Inerhalb dieses Repositories wird die Konfiguration der einzelen EC2 Instanzen festgehalten.

## Aufbau der Cloudmigration
<img width="2269" alt="Aufbau der Cloudmigration" src="https://user-images.githubusercontent.com/66683327/148694663-f4defe81-c19a-4b4a-8dba-ebb8685f42f9.png">

## Playbooks

| Bezeichnung          | Beschreibung
---------------------- | ---------------------------------
docker-base-installation.yml | Hiermit kann die Docker-Engine inkl. Docker-Swarm auf einem Host installiert werden.
docker-deploy-chatservice.yml | Hiermit kann der Chatservice auf den Worker-Nodes bereitgestellt werden.
docker-deploy-portainer.yml | Hiermit wird auf dem Docker-Swarm-Cluster eine Portainer Instanz bereitgestellt. 
docker-remove-portainer.yml | Hiermit kann eine bereitgestellte Portainer Instanz wieder vollständig gelöscht werden, falls die Ressourcen benötigt werden.
docker-setup-cluster.yml | Hiermit kann automatisiert ein Docker-Swarm-Cluster erzeugt werden und auch einzelne Worker-Knoten zu einem bereits bestehenden Cluster hinzugefügt werden.
ubuntu-base-setup.yml | Hiermit können Grundeinstellungen und Standardpakete auf einem Ubuntu Betriebssystem bereitgestellt werden.
