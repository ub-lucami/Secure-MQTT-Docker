# Basic Docker setup for a TLS enabled MQTT Server

# Getting Started

First you must provide the certificates used for TLS, in this solution we are using SSL certificates provided by LetsEncrypt.

# Certificate locations

LetsEncrypt certificates have to be located in the `../certs` directory (parent of main code folder). Possible modifications have to be addressed in `docker-compose.yml` accordingly.

# Generate Passwords File

`docker run -it --rm -v $pwd/config:/mosquitto/config eclipse-mosquitto mosquitto_passwd -c /mosquitto/config/passwords.txt <username>`

to add more users change `-c` to `-b`
