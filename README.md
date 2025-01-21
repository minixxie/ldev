# ldev
A single shell-script to setup local development environment. Making use of https://github.com/minixxie/k8s-services


# Download and install
```BASH
curl https://raw.githubusercontent.com/minixxie/ldev/refs/heads/main/ldev | \
	sudo tee /usr/local/bin/ldev > /dev/null \
	&& sudo chmod 755 /usr/local/bin/ldev
```

# Howto
```BASH
ldev help  # prints out how to use
```

# Initialize before use
```BASH
ldev init  # prepared ~/.ldev/ folder and download ~/.ldev/k8s-services repo
```

# MySQL
```BASH
ldev mysql up  # start mysql in k8s

ldev mysql get  # get mysql k8s resources (deployment, pod, svc, pvc, etc)

ldev mysql down  # stop mysql in k8s

ldev mysql cli  # use mysql cli to connect to the mysql server
```
