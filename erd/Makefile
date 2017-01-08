DOCKER_COMPOSE=$(shell which docker-compose)

docker-compose/build:
	$(DOCKER_COMPOSE) build

docker-compose/up:
	$(DOCKER_COMPOSE) up

docker-compose/clean:
	$(DOCKER_COMPOSE) stop
	$(DOCKER_COMPOSE) rm

generate:
	$(DOCKER_COMPOSE) run --rm erd-worker erd -i src/example01.er -o img/example01.png
	$(DOCKER_COMPOSE) run --rm erd-worker erd -i src/example02.er -o img/example02.png

