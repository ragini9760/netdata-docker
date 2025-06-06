Steps to Monitor System Resources Using Netdata via Docker
1. Install Docker
For Ubuntu:
sudo apt update
sudo apt install docker.io -y
sudo systemctl enable docker
sudo systemctl start docker


2. # netdata-docker

docker run -d \
  --name=netdata \
  -p 19999:19999 \
  --cap-add=SYS_PTRACE \
  --security-opt apparmor=unconfined \
  netdata/netdata
 Access the Netdata Dashboard
Open your browser and go to:
http://localhost:19999
(or use your server IP if remote: http://<your-server-ip>:19999
