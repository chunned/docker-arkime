This repository is forked from [mammo0/docker-arkime](https://github.com/mammo0/docker-arkime). The original README.md file is available [here](https://github.com/chunned/docker-arkime/blob/master/READM.old.md).

# Setup
```bash
# Clone repo
git clone https://github.com/chunned/docker-arkime/
cd docker-arkime
sudo sysctl -w vm.max_map_count=262144   # required for OpenSearch
sudo docker compose up
```
In another terminal window, enter the Arkime container: `docker exec -it docker-arkime-arkime-1 /bin/bash`

One directory needs permission modifications for the Capture service to work properly: `chmod -R 777 /opt/arkime/raw`

Arkime should now be available at `http://<host IP>:8005`
