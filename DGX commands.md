# Useful Docker commands

## Run a docker image

sudo nvidia-docker run –it –v /home/breber/Desktop:/workspace/Desktop –v
/raid/:/workspace/raid –network=host –privileged=true bma_tensorflow_2.3.0

## Check what GPUs are running

nvidia-smi

## View possible images

sudo nvidia-docker images

## View images running

sudo nvidia-docker ps

### Attach to a running image

sudo nvidia-docker attach ##id##

## Mount a drive

sudo mount –t cifs –o
username=bmanderson,password=\*\*\*,domain=mdanderson,uid=1000,gid=1000,dir_mode=0755,file_mode=0640
“//10.113.19.12/ro-admin/Shared/Radiation physics/BMAnderson”
/./home/bmanderson/desktop/Shared_Drive

## Build a docker image

sudo nvidia-docker build –network=host –t bma_tensorflow_2.3.0:latest .

## Sudo root acces

sudo su –
