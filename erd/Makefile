DOCKER_COMPOSE=$(shell which docker-compose)
erd_target_files=$(shell ls src | grep -e ".er")

docker-compose/build:
	$(DOCKER_COMPOSE) build

docker-compose/up:
	$(DOCKER_COMPOSE) up

docker-compose/clean:
	$(DOCKER_COMPOSE) stop
	$(DOCKER_COMPOSE) rm

generate:
	make $(addprefix run_erd/,${erd_target_files})
	$(DOCKER_COMPOSE) run --rm erd-worker \
		convert -append $(subst .er,.png,${erd_target_files}) -gravity southwest -splice 0x50 erd.png

run_erd/%:
	$(DOCKER_COMPOSE) run --rm erd-worker erd -i $* -o $(subst .er,.png,$*)

ssh:
	$(DOCKER_COMPOSE) run --rm erd-worker bash

