IMAGE_NAME=centos
CONTAINER_IMAGE=test_centos

build:
	docker build -t ${IMAGE_NAME} .

run:
	docker run -d --privileged --rm --name ${CONTAINER_IMAGE} ${IMAGE_NAME} /sbin/init

exec:
	docker exec -it ${CONTAINER_IMAGE} /bin/bash