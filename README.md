# Microfrontends WebComponent Sample

This repository contains a sample microfrontend application configuration that uses web components. It serves as an example of how to use web components to create a microfrontend application. The main goal is to provide a working example that can be used to showcase the microfrontends-controller: https://github.com/SevcikMichal/microfrontends-controller.

The microfrontends-controller repository contains some examples, but none of them have a complete UI + backend package. The controller can be used in combination with the microfrontends-webui: https://github.com/SevcikMichal/microfrontends-webui.

By combining all three projects, you will have the running infrastructure to deploy microfrontend applications using Kubernetes custom resources WebComponents, and a working example web UI where you can see your deployed web component.

The configuration is using docker images built from following repositories:
UI: https://github.com/SevcikMichal/microfrontends-webcomponent-webui-sample 
API: https://github.com/SevcikMichal/microfrontends-webcomponent-webapi-sample

The repo contains a kustomization.yaml which you can apply to a cluster running the microfrontends-controller.
If your cluster is also running the microfrontends-webui you can display this webcomponent as a microfrontend in the browser.

# Prerequisites
- Kubernetes cluster
- microfrontends-controller installed
- microfrontends-webui installed
- ingress-nginx (https://kubernetes.github.io/ingress-nginx/deploy/) controller installed (if you don't use nginx you have to adapt ingress.yaml in msevcik-ambulance-webapi)

# Installation
0. Fullfill the requirements
1. Clone this repository
2. Apply the kustomization.yaml to your cluster
```