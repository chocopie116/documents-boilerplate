DOCKER_COMPOSE=$(shell which docker-compose)

docker-compose/build:
	$(DOCKER_COMPOSE) build

docker-compose/up:
	$(DOCKER_COMPOSE) up

docker-compose/clean:
	$(DOCKER_COMPOSE) stop
	$(DOCKER_COMPOSE) rm

generate:
	$(DOCKER_COMPOSE) run --rm erd-worker erd -i src/example/001_example.er -o img/example/001_example.png
	$(DOCKER_COMPOSE) run --rm erd-worker erd -i src/example/002_example.er -o img/example/002_example.png
	$(DOCKER_COMPOSE) run --rm erd-worker \
		convert -append img/example/001_example.png img/example/002_example.png -gravity southwest -splice 0x50 img/example/all_erd.png

