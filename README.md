Configuración de VPS

public ip: 216.238.68.70
user: root
pass: *************

SO: Ubuntuserver 20.04


---------------------------------
USER SO:

adduser ronal
contraseña: ***********
adduser: geo
contraseña: ***********

usermod -aG sudo ronal
usermod -aG sudo geo


------------------------------------------

Instalación y configuración Nginx

	sudo apt-get install nginx (instalación)
	nginx -v
	sudo systemctl status nginx
	sudo systemctl start nginx
	sudo systemctl enable nginx (iniciar como servicio)
	sudo systemctl stop nginx
	sudo systemctl reload nginx (para recargar cambios)
	sudo systemctl restart nginx (reinicio)
	sudo ufw app list (abilitar permiso de trafico)
		Available applications: (El sistema muestra)
		Nginx Full
		Nginx HTTP  <
		Nginx HTTPS  
		OpenSSH
		
	sudo ufw allow 'nginx http' (Seleccionar opción para habilitar protocolo)
	sudo ufw reload (actualizar firewall)
	sudo ufw allow 'nginx full' (para permitir http y https)
	sudo nano etc/nginx/sites-available/default (El archivo de configuración esta en )
	cd /var/www/html/ (dentro esta el index.html)	
	sudo systemctl restart nginx (reiniciar nginx)
	sudo nginx -t (para probar nginx)
	
	
--------------------------------------------------------------------------------------

Configuración OpenVPN

curl -O https://raw.githubusercontent.com/angristan/openvpn-install/master/openvpn-install.sh

chmod +x openvpn-install.sh

sudo ./openvpn-install.sh (todo por defecto)

sudo ./openvpn-install.sh (luego de la instalación para agregar clientes)


--------------------------------------------------------------------------------------

Configuración FTP para transferencia de archivos

apt-get install vsftpd
ps -ef | grep vsftpd
	

--------------------------------------------------------------------------------------
