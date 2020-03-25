
### Install GCS Connector
To install the GCS connector in pyspark, run:
```
python3 -m pip install -vvv git+https://github.com/bw2/install-gcs-connector.git --upgrade
```



### Overview
The [GCS connector](https://cloud.google.com/dataproc/docs/concepts/connectors/cloud-storage) allows [hail](https://hail.is/docs/0.2/utils/index.html)/spark/hadoop to read/write Google Storage bucket files directly.

It can be [tricky to install](https://github.com/GoogleCloudDataproc/hadoop-connectors/blob/master/gcs/INSTALL.md), so this package automates these installation steps:

```
1. downloading the gcs connector .jar file to $SPARK_HOME/jars/ 
2. finding your gcloud .json key file in ~/.config/gcloud/application_default_credentials.json (created by running gcloud auth application-default login) or in ~/.config/gcloud/legacy_credentials/*/adc.json (created by gcloud auth login) 
3. updating your $SPARK_HOME/conf/spark-defaults.conf to add the key file path
```

To install it, you must 
- be logged in via `gcloud auth login` or `gcloud auth application-default login`
- have [pyspark](https://spark.apache.org/docs/latest/api/python/index.html) or [hail](https://hail.is) installed 


