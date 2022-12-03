# k8s essential trng

https://www.linkedin.com/learning-login/share?account=2103260&forceAccount=false&redirect=https%3A%2F%2Fwww.linkedin.com%2Flearning%2Fkubernetes-essential-training-application-development%3Ftrk%3Dshare_ent_url%26shareId%3DEtB%252Fg0V%252FSv2fd2Pnc9UU%252FQ%253D%253D

## Get started
```shell
pushd ex_files/01_03
minikube start # or maybe  `minikube start --addons=dashboard --addons=metrics-server --addons="ingress" --addons="ingress-dns"`
kubectl apply -f # apply all files in pwd
```

## Imperative Commands
### Expose
`kubectl expose pod green --port 8080 --name blue-green`

## Open all the services
`$ minikube service --all`

Result

```

|-----------|------------|-------------|---------------------------|
| NAMESPACE |    NAME    | TARGET PORT |            URL            |
|-----------|------------|-------------|---------------------------|
| default   | blue-green |          80 | http://192.168.49.2:30064 |
|-----------|------------|-------------|---------------------------|
|-----------|----------------|-------------|---------------------------|
| NAMESPACE |      NAME      | TARGET PORT |            URL            |
|-----------|----------------|-------------|---------------------------|
| default   | hello-minikube |          80 | http://192.168.49.2:30122 |
|-----------|----------------|-------------|---------------------------|
|-----------|------------|-------------|--------------|
| NAMESPACE |    NAME    | TARGET PORT |     URL      |
|-----------|------------|-------------|--------------|
| default   | kubernetes |             | No node port |
|-----------|------------|-------------|--------------|
😿  service default/kubernetes has no node port
|-----------|-----------------------|-------------|--------------|
| NAMESPACE |         NAME          | TARGET PORT |     URL      |
|-----------|-----------------------|-------------|--------------|
| default   | quickstart-es-default |             | No node port |
|-----------|-----------------------|-------------|--------------|
😿  service default/quickstart-es-default has no node port
|-----------|--------------------|-------------|--------------|
| NAMESPACE |        NAME        | TARGET PORT |     URL      |
|-----------|--------------------|-------------|--------------|
| default   | quickstart-es-http |             | No node port |
|-----------|--------------------|-------------|--------------|
😿  service default/quickstart-es-http has no node port
|-----------|-----------------------------|-------------|--------------|
| NAMESPACE |            NAME             | TARGET PORT |     URL      |
|-----------|-----------------------------|-------------|--------------|
| default   | quickstart-es-internal-http |             | No node port |
|-----------|-----------------------------|-------------|--------------|
😿  service default/quickstart-es-internal-http has no node port
|-----------|-------------------------|-------------|--------------|
| NAMESPACE |          NAME           | TARGET PORT |     URL      |
|-----------|-------------------------|-------------|--------------|
| default   | quickstart-es-transport |             | No node port |
|-----------|-------------------------|-------------|--------------|
😿  service default/quickstart-es-transport has no node port
|-----------|--------------------|-------------|--------------|
| NAMESPACE |        NAME        | TARGET PORT |     URL      |
|-----------|--------------------|-------------|--------------|
| default   | quickstart-kb-http |             | No node port |
|-----------|--------------------|-------------|--------------|
😿  service default/quickstart-kb-http has no node port
🏃  Starting tunnel for service blue-green.
🏃  Starting tunnel for service hello-minikube.
🏃  Starting tunnel for service kubernetes.
🏃  Starting tunnel for service quickstart-es-default.
🏃  Starting tunnel for service quickstart-es-http.
🏃  Starting tunnel for service quickstart-es-internal-http.
🏃  Starting tunnel for service quickstart-es-transport.
🏃  Starting tunnel for service quickstart-kb-http.
d|-----------|-----------------------------|-------------|------------------------|
| NAMESPACE |            NAME             | TARGET PORT |          URL           |
|-----------|-----------------------------|-------------|------------------------|
| default   | blue-green                  |             | http://127.0.0.1:63051 |
| default   | hello-minikube              |             | http://127.0.0.1:63053 |
| default   | kubernetes                  |             | http://127.0.0.1:63055 |
| default   | quickstart-es-default       |             | http://127.0.0.1:63057 |
| default   | quickstart-es-http          |             | http://127.0.0.1:63059 |
| default   | quickstart-es-internal-http |             | http://127.0.0.1:63061 |
| default   | quickstart-es-transport     |             | http://127.0.0.1:63063 |
| default   | quickstart-kb-http          |             | http://127.0.0.1:63065 |
|-----------|-----------------------------|-------------|------------------------|
🎉  Opening service default/blue-green in default browser...
🎉  Opening service default/hello-minikube in default browser...
🎉  Opening service default/kubernetes in default browser...
🎉  Opening service default/quickstart-es-default in default browser...
🎉  Opening service default/quickstart-es-http in default browser...
🎉  Opening service default/quickstart-es-internal-http in default browser...
🎉  Opening service default/quickstart-es-transport in default browser...
🎉  Opening service default/quickstart-kb-http in default browser...
❗  Because you are using a Docker driver on darwin, the terminal needs to be open to run it.
```