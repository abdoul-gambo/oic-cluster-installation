### Cluster-installation

This post show the HDP cluster installation.


> Install prerequisite

```sh
# Update package source
sudo apt-get update

# install git
sudo apt-get install git

# install gcloud sdk
curl https://sdk.cloud.google.com | bash

# authenticate to Google cloud
gcloud auth login                   

```

> Download bdutil

```sh
git clone https://github.com/GoogleCloudPlatform/bdutil 
cd bdutil
```

> Edit and modify the configuration file

```sh
# Edit ambari configuration file and set your deployment configuration
nano platforms/hdp/ambari.conf

```

> Deploy ambari cluster

```sh
# Deploy cluster
./bdutil -f -e ambari deploy

```

> Go to http://hadoop-m:8080

![ambari.conf head](https://github.com/agambov/oic-cluster-installation/img/blob/master/ambari2.png)
