# Openshift

$ oc new-project cloud-native-fio

$ oc create sa cloud-native-fio

$ oc adm policy add-scc-to-user anyuid -z cloud-native-fio

