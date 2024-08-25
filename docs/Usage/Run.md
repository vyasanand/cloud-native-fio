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

