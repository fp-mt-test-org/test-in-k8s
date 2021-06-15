## Install Dependencies

    ./install-dev-dependencies.sh

## Build

    flex build

## Running Locally w/ Docker

After a successful build, you can run it like so:

    docker run -p 8080:8080 test-in-k8s:0.0.1-SNAPSHOT

After it starts successfully, you can get a successfully http response:

    curl localhost:8080/actuator/health
    {"status":"UP"}

## Running w/ Kubernetes

    kubectl apply -f deployment.yaml
    deployment.apps/test-in-k8s created
    service/test-in-k8s created
