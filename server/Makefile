postgresinit:
    docker run --name my-postgres -p 5433:5432 postgres -e POSTGRES_USER=my-postgres -e POSTGRES_PASSWORD=mysecretpassword -d postgres

postgres:
    docker exec -it my-postgres psql

createdb:
    docker exec -it my-postgres createdb --username=my-postgres --owner=my-postgres go_chat

dropdb:
    docker exec -it my-postgres dropdb go_chat

migrateup:
    migrate -path db/migrations -database "postgresql://my-postgres:mysecretpassword@localhost:5433/go_chat?sslmode=disable" -verbose up

migratedown:
    migrate -path db/migrations -database "postgresql://my-postgres:mysecretpassword@localhost:5433/go_chat?sslmode=disable" -verbose down

.PHONY: postgresinit postgres createdb dropdb migrateup migratedown
