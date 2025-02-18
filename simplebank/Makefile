postgres:
	docker run --name postgres-udemy -p 5432:5432 -e POSTGRES_USER=shuaiqingluo -e POSTGRES_PASSWORD=mysecretpassword -d postgres
createdb:
	docker exec -it postgres-udemy createdb --username=shuaiqingluo --owner=shuaiqingluo simple_bank
dropdb:
	docker exec -it postgres-udemy dropdb simple_bank
.PHONY:
	postgres createdb dropdb