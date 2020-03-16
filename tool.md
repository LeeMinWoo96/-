## 유용툴

#### code server
##### VSCode 온라인 
```
wget https://github.com/cdr/code-server/releases/download/2.1688-vsc1.39.2/code-server2.1688-vsc1.39.2-linux-x86_64.tar.gz
tar xvfz code-server2.1688-vsc1.39.2-linux-x86_64.tar.gz
sudo mv code-server2.1688-vsc1.39.2-linux-x86_64/code-server /usr/local/bin
mkdir ~/project
sudo curl https://gist.githubusercontent.com/subicura/d025000486d30d92dfa6ccc523c3f5e3/raw/2e93bb0dca992523a3e3a6fdba95d2f3526c52db/codeserver.service -o /lib/systemd/system/codeserver.service
sudo systemctl start codeserver
sudo systemctl enable codeserver
```
http://xxxx:8000 접속합니다. 비밀번호는 1q2w3e4r 입니다.

----


#### wetty
##### 웹 터미널 (4200 port)
```
sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/' /etc/ssh/sshd_config
echo "ubuntu:1q2w3e4r" | chpasswd
service sshd reload
apt-get -y update
apt-get -y install nodejs npm
npm install -g wetty
curl https://gist.githubusercontent.com/subicura/9058671c16e2abd36533fea2798886b0/raw/e5d249612711b14c9c8f44798dea1368395e86a9/wetty.service -o /lib/systemd/system/wetty.service
systemctl start wetty
systemctl enable wetty
```
password : 1q2w3e4r
