# dabcast

#DabCast v1.0 installer
***********************
#Rasperry Pi5 / system débian 12
#Hackrf one
#Easydab2
#Multiplex "181FM" - 13 radios - 88kbps – stéréo

Par default le modulateur est l'Easydab2 sur le port 9999 en zmq
Pour le hackrf utiliser le fichier "odr-dabmux-edi-out.info" et la sortie Edi

Je vous conseil une installation d’un débian 12 sous les identifiants « odr »

host : dabcast
user : odr
pass : odr

Et une ip fixe

Copiez le dossier dabcast dans home/odr/

Mise à jour de votre system :

sudo apt-get update
sudo apt-get upgrade -y

Installez votre hackrf one :

sudo su

apt install hackrf

Définissez votre zone :

sudo timedatectl set-timezone Europe/Paris

Installez git :

sudo apt-get install -y git

puis installez les outils ODR :

sudo bash dabcast/install/mmbtools-get --branch next install

*********************************
Une fois l’installtion terminée : 

Rendez vous sur firefox ou Chromium (moins lourd) et tapez l’aresse: http://localhost:8001

user: odr
pass: odr

Clickez sur RESTART ALL

Enjoy ! Vous diffusez 13 radios en dab+ sur le canal 5A


Le manager graphique pour modifier ou ajouter des radios est ici :

Rendez vous sur firefox ou Chromium (moins lourd) et tapez l’aresse: http://localhost:8003

user : odr
pass : odr

Le Manager de Mux est ici => http://localhost:8002

*****************************************************
EasyDab2 Config :

Network :
ip      : 192.168.2.4
Netmask : 255.255.255.0
Gateway : 192.168.2.254

Remote IP   : 192.168.2.2
Remote Port : 9999

*************************

Désinstalation des outils ODR : sudo bash dabcast/install/mmbtools-get remove





								      Dabcast-Jean-Marie Gaulier
