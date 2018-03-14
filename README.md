# ApacheDS

LDAP server backed by the openmicroscopy.apacheds docker image.
The primary aim is to provide a team-manageable LDAP installation.

## Deployment

This application is deployed on Kubernetes using the manifests in [k8s](k8s).
To run this:
- Add your PostgreSQL and GMail credentials to [secret-config.yaml.example](k8s/secret-config.yaml.example)
- Change [pv-nfs.yml](k8s/pv-nfs.yml) to point to a persistent volume
- Create the Kubernetes resources: `kubectl apply -f k8s`
