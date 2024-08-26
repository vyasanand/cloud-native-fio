# Openshift

* Create a new project named `cloud-native-fio`
  
  ```$ oc new-project cloud-native-fio```

* Create a service account named `cloud-native-fio` in the project `cloud-native-fio`
  
  ```$ oc create sa cloud-native-fio```

* Add the service account `cloud-native-fio` to `anyuid` scc
  
  ```$ oc adm policy add-scc-to-user anyuid -z cloud-native-fio```

* Clone this repository
  
  ```$ git clone https://github.com/vyasanand/cloud-native-fio.git```

* Deploy the following objects from a single `deploy.yaml` file:
  * Configmap: `testfio`
  * PVC: `cloud-native-fio-pvc`
  * Deployment: `cloud-native-fio`
  * Service: `cloud-native-fio-svc`
  * Route: `gfio`

  ```$ oc create -f cloud-native-fio/run/OpenShift/deploy.yaml```

# Customize your tests

If you use the default `deploy.yaml`, it creates a configmap `testfio` which is based on [sample test job](../../run/fio/test.fio)

In a real use case, you may wish to customize the job based on your requirements. You can do this by either modifying the `configmap` in the `deploy.yaml` file or create an external job on `helper` or `jump` host and copy it using `oc` CLI.

* Example:

  ```$ oc cp <anothertestjob.fio> <your-pod-name>:/data -c gfio```

  NOTE: `/data` is the default mountpoint in the [deploy.yaml](../../run/OpenShift/deploy.yaml) file which is mounted to both `gfio` and `gfio-client` containers.
