CWD = $(shell pwd)/..
PROJECT_NAME = imu-array-dev
MOUNT_PATH = /workspace
IMAGE = ghcr.io/inti-cmnb/kicad_auto_full:dev_k9

build:
	MSYS_NO_PATHCONV=1 docker run --rm \
		-v "$(CWD):$(MOUNT_PATH)" \
		--workdir="$(MOUNT_PATH)" \
		$(IMAGE) \
		/bin/bash -c "cd $(MOUNT_PATH)/$(PROJECT_NAME); \
		kibot -d $(MOUNT_PATH)/outputs/ && rm -rf $(MOUNT_PATH)/outputs/gerbers"

test:
	exit 0