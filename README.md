<div style="text-align:center">

## Dockerized Portainer with Agent
<img src="https://github.com/aviolaris/instaunfollowers/assets/48277853/c611ecae-daa5-4254-8323-bdbf5a2cd7ab" alt="Dockerized Portainer with Agent" style="width:280px;">

</div>

 This project provides a configuration file with the essential settings for deploying Portainer and Portainer Agent using Docker Compose.


## Configuration

---

The `docker-compose.yml` file contains the following services:

*   `agent`: This service runs the Portainer Agent using the `portainer/agent` Docker image. It mounts the host's Docker socket and volumes into the container.
    
*   `portainer`: This service runs Portainer itself using the `portainer/portainer-ce` Docker image. It publishes port 9000 on the host and mounts the host's Docker socket and a named volume for persistent data storage.

## Usage

---
1.  Clone the repository:
      
    ```shell
    git clone aviolaris/dockerized-portainer-with-agent
    ```
    
2.  Deploy the Portainer and Portainer Agent containers:
    
    ```shell
    docker-compose up -d
    ```
    
3.  Access Portainer by opening a web browser and navigating to `http://localhost:9000`. If you are running Docker on a remote machine, replace `localhost` with the IP address or hostname of the machine.
    
4.  Follow the Portainer setup wizard to configure your administrator account and connect to your Docker environment.



## Disclaimer

---

Any trademarks, names, logos, icons, or other intellectual property displayed or referenced in this repository are the exclusive property of their respective owners. The inclusion or mention of such trademarks, names, logos, icons, or other intellectual property in no way implies any form of affiliation, endorsement, sponsorship, or support.

## License

---

This project is licensed under the [MIT License](https://github.com/aviolaris/dockerized-portainer-with-agent/blob/main/LICENSE).
