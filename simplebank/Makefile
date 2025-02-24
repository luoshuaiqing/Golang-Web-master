postgres:
	docker run --name postgres-udemy -p 5432:5432 -e POSTGRES_USER=shuaiqingluo -e POSTGRES_PASSWORD=mysecretpassword -d postgres
createdb:
	docker exec -it postgres-udemy createdb --username=shuaiqingluo --owner=shuaiqingluo simple_bank
dropdb:
	docker exec -it postgres-udemy dropdb --username=shuaiqingluo simple_bank
migrateup:
	migrate -path db/migration -database "postgresql://shuaiqingluo:mysecretpassword@localhost:5432/simple_bank?sslmode=disable" -verbose up
migratedown:
	migrate -path db/migration -database "postgresql://shuaiqingluo:mysecretpassword@localhost:5432/simple_bank?sslmode=disable" -verbose down
.PHONY:
	postgres createdb dropdb migrateup migratedown