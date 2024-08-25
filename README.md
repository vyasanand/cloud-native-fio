# About
With an increasing number of applications leveraging statefulsets and running their apps on Kubernetes, container storage solutions have become an important factor in architecting container platforms. Kubernetes is no longer used only for stateless applications rather an increase in various uses cases for DB's, Analytics and Edge solutions.

As an Architect, you might be asked to suggest, assess, decide and design a container storage solution made available via various vendors like Dell, HPE, Red Hat etc.

IOPS and Throughput performance are key metrics on how your storage is going to perform. While running these tests using tools like `FIO` are quite straightforward, but getting them to run on container platforms like `OpenShift` can be a challenging task, specially in disconnected environments.

To overcome this challange, `cloud-native-fio` was born which uses other open source projects like [xpra](https://github.com/Xpra-org/xpra) which allows your to run x11 programs over browser and [fio](https://github.com/axboe/fio) which is a already a popular project used for IOPS testing. 

# Deploy

Follow the instructions listed [here](docs/Usage/Run.md)

# Build



