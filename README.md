# OwnAi

Own AI is a set of docker containers that allow you to host your own AI.

## Requirements

- Docker
- Nvidia GPU (AMD will work with some tinkering, see ROCM versions of images)
- Enough VRAM to run the models

## Install

- Clone the repository
- Rename .env_template => .env
- Change the password in .env (this is the Open WebUI Secret)
- `docker compose up -d` to start the containers
- once the containers have started you will see folders in the parent directory.
- Download your image gen models into the comfyui/ComfyUI/models folder.
  - ComfyUI's WebUI will guide you through this if you need help :D

Note:

- Watchtower is not required but nice to have, auto updates containers by checking for new releases.
  - Watchtower is set to check every 24 hours, you can change this in the watchtower section of the compose file `--interval`.
