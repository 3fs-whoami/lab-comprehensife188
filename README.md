After clone my reppo, you can build all contauiners from command.

$ podman-compose --build -d up

if you want to use Dockerfile you must rename Containerfile to another name !!!!!!

Before you running in the top comand, you must create network and volume !!!!!

$ podman network create beeper-frotend && podman network create beeper-backend && podman volume create beeper-data

I wish this reppo can help you to walk in the future !!! And can solve your problems..!!!
