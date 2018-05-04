# gitlab-ce-template-ocp

A rehashed version of the template that can be found at: https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/docker/openshift-template.json
to instead use the red hat version of the redis template as found in the https://github.com/openshift/origin/blob/master/examples/db-templates/redis-persistent-template.json


```
oc new-project gitlab
oc create -f template.json
oc new-app --template=gitlab-ce -p APPLICATION_HOSTNAME=gitlab-gitlab.192.168.42.89.nip.io
oc adm policy add-scc-to-user anyuid -z gitlab-ce-user
```