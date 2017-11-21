FROM eclipse-mosquitto:1.4.12
USER root
ADD [ "files/mqtt-admin.tar.gz", "/usr/share/mqtt-admin/" ]
ADD [ "files/mosquitto.conf", "/mosquitto/config/mosquitto.conf" ]
EXPOSE 9001
USER mosquitto
CMD [ "/usr/sbin/mosquitto", "-c", "/mosquitto/config/mosquitto.conf", "-p", "1883"]
