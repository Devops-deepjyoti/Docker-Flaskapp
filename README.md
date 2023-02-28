AWS Setup steps code for Docker 

 sudo apt-get update
1. Adding necessary repo
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

2. Adding docker repo
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

3. Install necessary dependencies
sudo apt-get install apt-transport-https ca-certificates curl gnupg lsb-release -y

4. Upating and installing docker
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io -y

5. Add my user to docker group
sudo usermod -aG docker $USER

6. Testing the installation
sudo docker pull hello-world
