DOCKER_COMPOSE=$(shell which docker-compose)

docker-compose/build:
	$(DOCKER_COMPOSE) build

docker-compose/up:
	$(DOCKER_COMPOSE) up

docker-compose/clean:
	$(DOCKER_COMPOSE) stop
	$(DOCKER_COMPOSE) rm

generate:
	$(DOCKER_COMPOSE) run erd bash
