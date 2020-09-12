# caprover-setup

**Docker Install steps (Copy and Paste as is within the SSH terminal. Make you are you sudo as root sudo su).**<br>
	1.`apt-get update`  <br>
	2.`apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common` <br>
  3. `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -` <br>
	4. `apt-key fingerprint 0EBFCD88`  <br>
	5. `add-apt-repository  "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"` <br>
	6.`apt-get update` <br>
	7.`apt-get install docker-ce docker-ce-cli containerd.io`<br>
	8. `docker run hello-world` <br>

### CapRover Install<br>
	9. `ufw allow 80,443,3000,996,7946,4789,2377/tcp; ufw allow 7946,4789,2377/udp;` 
	10.`docker run -p 80:80 -p 443:443 -p 3000:3000 -v /var/run/docker.sock:/var/run/docker.sock -v /captain:/captain caprover/caprover` 

### CapRover Setup (You will need NodeJS and NPM installed on our local computer)<br>
	11.`npm install -g caprover` 
	12.`caprover serversetup`
