🚀 Install Docker Compose Plugin on Ubuntu (EC2)
To run docker compose on your  instance, follow these steps:

```bash
1. Update package list and install prerequisites
sudo apt update
sudo apt install ca-certificates curl gnupg lsb-release
2. Add Docker’s official GPG key
sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
3. Set up the Docker stable repository
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] \
  https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
4. Update package list again
sudo apt update
5. Install the Docker Compose plugin
sudo apt install docker-compose-plugin
6. Verify installation
docker compose version

Clone the Repository

git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

▶️ Start the Application
docker compose up --build
