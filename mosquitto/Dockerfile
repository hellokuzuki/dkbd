FROM sourceperl/mosquitto:latest
# Use root to run add command.
USER root
# Unpack and Add mqtt-admin website to image
ADD  [ "files/mqtt-admin.tar.gz", "/usr/share/mqtt-admin/" ]
# Unpack Add websocket to image so that user will be able to see mqtt in web browser.
ADD  [ "files/libwebsockets.tar.gz", "/" ]
# Unpack Add mosquito 1.4.10 to replace sourceperl/mosquitt(1.4.2)
ADD  [ "files/mosquitto.tar.gz", "/" ]
# websoket setting
    # listener 9001 -> mqtt websocket port 
    # protocol websockets -> protocol 
    # http_dir /usr/share/mqtt-admin -> mqtt-admin derectory
ADD  [ "files/websockets.conf", "/etc/mosquitto/conf.d/" ]
# port has been opened by sourceperl image
#EXPOSE 9001
# change user
USER mosquitto
