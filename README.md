# ldev
A single shell-script to setup local development environment. Making use of https://github.com/minixxie/k8s-services


## Download and install
```BASH
curl -sSL https://raw.githubusercontent.com/minixxie/ldev/refs/heads/main/ldev | bash -s -- install
```

## Upgrade afterwards
```BASH
ldev install
```

## Howto
```BASH
ldev help  # prints out how to use
```

## Components
1. k8s
2. gpu
3. mysql
4. pgsql
5. redis
6. mongo
7. ollama

## MySQL
```BASH
ldev mysql up  # start mysql in k8s

ldev mysql get  # get mysql k8s resources (deployment, pod, svc, pvc, etc)

ldev mysql down  # stop mysql in k8s

ldev mysql cli  # use mysql cli to connect to the mysql server
```

## My Application
`ldev` command can also configure and execute my application in k8s as deployments.
Step 1: initialize the yaml config file `ldev.yaml`
```BASH
ldev init
```

Step 2: build the container image
```BASH
ldev build
```

Step 3: generate the kustomization files and spin up in k8s
```BASH
ldev up
```

To stop and remove from k8s:
```BASH
ldev down
```

To list what resources were created in k8s:
```BASH
ldev get
```

To tail the logs of the pod:
```BASH
ldev logs
```

Enter the pod's main container to debug:
```BASH
ldev exec
```
