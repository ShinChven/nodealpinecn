all: build

help:
	@echo ""
	@echo "-- Help Menu"
	@echo ""
	@echo "   1. make build	- build the node alpine image with aliyun alpine linux mirror and set timezone to PRC(China +8)."
	@echo "   2. make release	- build the image with no cache."
	@echo "   3. make publish	- build the release image and push to dockerhub."


build:
	@docker build --tag=shinchven/nodealpinecn .

release: 
	@docker build --no-cache --tag=shinchven/nodealpinecn .
	
publish: release
	@docker push shinchven/nodealpinecn



