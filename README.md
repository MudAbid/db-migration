# db-migration
Manage SQL database (postgress)

To run you need go-migration install in your machine or using docker.


To intall in your machine fowwing the next commands:
    Windows:
        scoop install migrate
    Linux:
        curl -L https://packagecloud.io/golang-migrate/migrate/gpgkey| apt-key add -
        echo "deb https://packagecloud.io/golang-migrate/migrate/ubuntu/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/migrate.list
        apt-get update
        apt-get install -y migrate
    Mac:
        brew install golang-migrate

To use docker using the next command:

docker run -v {{ migration dir }}:/migrations --network host migrate/migrate
    -path=/migrations/ -database postgres://localhost:5432/database up 2

