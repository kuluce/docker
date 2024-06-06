

all: run


init: clean

clean:
	@echo "Cleaning up..."
	@sudo rm -rf mysql/data/*
	@sudo rm -rf mysql/logs/*
	@sudo rm -rf mysql/conf/*
	@sudo rm -rf victoriametrics/*
	@sudo rm -rf redis/*

build:
	@echo "Building..."

up: build
	@echo "Uploading..."
	@docker-compose up -d

down:
	@echo "Stopping..."
	@docker-compose down

ps:
	@echo "ps"
	@docker-compose ps

run: up


monitor:
	@echo "Monitoring..."
	@docker-compose logs -f	