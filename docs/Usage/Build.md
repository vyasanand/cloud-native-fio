# To build your own container files

* Clone this repository
  
  ```$ git clone https://github.com/vyasanand/cloud-native-fio.git```

# xpra container image

* Build the xpra container image

  ```$ podman build -t xpra:1.0 cloud-native-fio/build/xpra/Containerfile```

* Tag the xpra container image

  ```$ podman tag abcdef12 <your-reg-host/path>/xpra:1.0```

* Push the xpra container image

  ```$ podman push <your-reg-host/path>/xpra:1.0```

# gfio container image

* Build the gfio container image

  ```$ podman build -t gfio:1.0 cloud-native-fio/build/gfio/Containerfile```

* Tag the gfio container image

  ```$ podman tag wxcgz34 <your-reg-host/path>/gfio:1.0```

* Push the gfio container image

  ```$ podman push <your-reg-host/path>/gfio:1.0```

# gfio-client container image

* Build the gfio-client container image

  ```$ podman build -t gfio-client:1.0 cloud-native-fio/build/gfio-client/Containerfile```

* Tag the gfio-client container image

  ```$ podman tag dgtyu367 <your-reg-host/path>/gfio-client:1.0```

* Push the gfio-client container image

  ```$ podman push <your-reg-host/path>/gfio-client:1.0```
