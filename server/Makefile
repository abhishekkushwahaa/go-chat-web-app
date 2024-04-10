postgresinit:
    docker run --name my-postgres -e POSTGRES_PASSWORD=mysecretpassword -d -p 5432:5432 postgres

postgres: 
    docker exec -it my-postgres bash

	createdb:
		docker exec -it my-postgres psql -U postgres -c "CREATE DATABASE go_chat;"

	dropdb:
		docker exec -it my-postgres psql -U postgres -c "DROP DATABASE go_chat;"

.PHONY: postgresinit postgres createdb dropdb