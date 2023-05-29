# nuxt3 podman template

This template uses podman to containerize a nuxt application.

## How this repository is built

- .vscode - set IDE configuration and recommended plugins.
- pod.yaml - pod definition file to use when spinning up a dev container.
- config.yaml - configmap used by the pod

## Usage

- `podman build -t node-devcontainer --target=base nuxt-app/.` - Build image
- `podman play kube --configmap=config.yaml --replace pod.yaml` - Start devcontainer
- `podman exec -it nuxt-app-devcontainer fish` - Login into containairs interactive shell
- `cd nuxt-app && npm install && npm run dev` - Start devserver
