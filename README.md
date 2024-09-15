# bitnami-moodle-sso
This is a bitnami Moodle with SSO plugins for Active Directory

First:

    git clone //github.com/lumbans/moodle-sso.git

then:

    cd moodle-sso

Build docker moodle with the SSO plugins:

    docker build -t moodle-4 .

Then run docker compose

    docker-compose up -d 

verified moodle been deployed:

    docker-compose ps       

                                                                                                     
output:
   
    NAME                  IMAGE                            COMMAND                  SERVICE   CREATED          STATUS          PORTS
    moodle-ad-mariadb-1   docker.io/bitnami/mariadb:11.4   "/opt/bitnami/script…"   mariadb   26 seconds ago   Up 26 seconds   3306/tcp
    moodle-ad-moodle-1    moodle-4:latest                  "/opt/bitnami/script…"   moodle    26 seconds ago   Up 9 seconds    0.0.0.0:80->8080/tcp, :::80->8080/tcp, 0.0.0.0:443->8443/tcp, :::443->8443/tcp
