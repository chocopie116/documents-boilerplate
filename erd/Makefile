DOCKER_COMPOSE=$(shell which docker-compose)
erd_input_dir=src
erd_output_dir=img

docker-compose/build:
	$(DOCKER_COMPOSE) build

docker-compose/up:
	$(DOCKER_COMPOSE) up

docker-compose/clean:
	$(DOCKER_COMPOSE) stop
	$(DOCKER_COMPOSE) rm

generate:
	$(DOCKER_COMPOSE) run --rm erd-worker erd -i $(erd_input_dir)/example/001_example.er -o $(erd_output_dir)/example/001_example.png
	$(DOCKER_COMPOSE) run --rm erd-worker erd -i $(erd_input_dir)/example/002_example.er -o $(erd_output_dir)/example/002_example.png
	$(DOCKER_COMPOSE) run --rm erd-worker \
		convert -append $(erd_output_dir)/example/001_example.png $(erd_output_dir)/example/002_example.png -gravity southwest -splice 0x50 $(erd_output_dir)/example/all_erd.png

