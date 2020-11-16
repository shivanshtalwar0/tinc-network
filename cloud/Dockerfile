FROM ubuntu:16.04
WORKDIR /etc/tinc
RUN apt update && apt upgrade -y \
    && apt install nginx tinc net-tools -y
COPY hosts/ hosts/
COPY rsa_key.priv rsa_key.priv
COPY tinc-up tinc-up
COPY tinc-down tinc-down
COPY tinc.conf tinc.conf    
RUN chmod +x tinc-*
# CMD [ "tincd" ]