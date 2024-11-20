# summit_2024
Notes pour la présentation "Automatiser le déploiement de services Public Cloud (Kubernetes, bases de données, DNS) avec Terraform"



## Créer une instance avec les prérequis dans le control panel OVHCloud


```bash
cat ~/.ssh/id_rsa.pub|pbcopy	
```
Add [cloud-init script](cloud-init.yaml)

The cloud-init log are available in `/var/log/cloud-init-output.log`





Se logger sur l'instance

```bash
ssh ubuntu@<IP>
```
Créer un token via cette [page](https://api.ovh.com/createToken/?GET=/*&POST=/*&PUT=/*&DELETE=/*)

Créer un fichier `ovh_env.sh`
```bash
export OVH_ENDPOINT=ovh-eu
export OVH_APPLICATION_KEY=""
export OVH_APPLICATION_SECRET=""
export OVH_CONSUMER_KEY=""
export OVH_CLOUD_PROJECT_SERVICE=""
```

Clone le repo
```bash
git clone -b yomovh/wordpress_example_merge_steps https://github.com/ovh/public-cloud-examples/
cd public-cloud-examples/use-cases/wordpress-k8s-mysql/
```

Suivre les instructions du [README](https://github.com/ovh/public-cloud-examples/blob/yomovh/wordpress_example_merge_steps/use-cases/wordpress-k8s-mysql/README.md)

