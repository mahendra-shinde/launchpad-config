#Manual Installation

1. Mirantis Repo URL with GPG Key for Ubuntu
  
    ```
    curl -fsSL https://repos.mirantis.com/ubuntu/gpg | sudo apt-key add
    
    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu  $(lsb_release -cs)  stable"
    
    sudo apt update -y
    ```

2.  Install `docker-ee` and `docker-ee-cli` packages

    ```
    sudo apt install docker-ee docker-ee-cli -y
    ```

3.  