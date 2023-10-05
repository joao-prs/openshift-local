# openshift-local
Openshift básico para iniciantes utilizando uma versão da redhat.

eval $(crc oc-env)

### Comandos bãsicos projetos
```sh
oc help # ver lista de comandos

oc whoami # ver usuário ativo

oc new-project <name> # criar novo projeto

oc new-projects # exibe lista de projetos
```

### Criação de secret
```sh
# supondo que voce tenha um arquivo de secrets chamado "app-secret.ini" 
oc create secret generic <nome_secret> --from-env-file app-secret.ini

oc set env --help # oferece ajuda com exemplos

oc set env --from secret/nome_secret deploy/seu_app
```

### Pods
```sh
oc get pods # lista pods

oc exec -ti app-f9e5a8b1245-gzk3t -- sh # se conecta no pod
oc exec -ti deploy/app -- sh # se conecta no pod
oc rsh deploy/app  # se conecta no pod

oc delete pod app-f9e5a8b1245-gzk3t # delete o pod
```

> em breve, mais conteúdo
