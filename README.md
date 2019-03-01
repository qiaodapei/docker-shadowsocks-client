# What is this?
Shadowsocks client in a docker container. Quickly create local shadowsocks client in 5 secs.

# How to use?
Simply run(replace related args with your custom value)
```bash
 sudo docker run -d --restart=yes \
                 -e SERVER=<your-server> \
                 -e SERVER_PORT=<port> \
                 -e PASSWORD=<your-password> \
                 -e LOCAL_PORT=1080 \
                 -p 1080:1080 qiaodapei/shadowsocks-client:latest
```
OR

Clone this repo and go into it
```bash
 git clone https://github.com/qiaodapei/docker-shadowsocks-client.git && cd docker-shadowsocks-client
```
Setting connection info in *docker-compose.yml*, then run
```bash
sudo docker-compose up -d
```
Now your can access your socks proxy with address ~localhost:1080~.

# Build your own image
If you would like to build your own docker image, simply clone this repo and run:
```bash
 sudo docker build -t <your-image-name> .
```
