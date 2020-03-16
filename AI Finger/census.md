# AI Finger
## Overview
Internet census of Machine Learning and Artificial Intelligence Frameworks and Applications.
## Products
- [AMQP and MQTT Message Brokers](#amqp-and-mqtt-message-brokers)
  - [RabbitMQ Message Brokers](#rabbitmq-message-brokers)
  - [MQTT Message Brokers](#mqtt-message-brokers)
  - [Eclipse Mosquitto Message Brokers](#eclipse-mosquitto-message-brokers)
- [Federated Learning](#federated-learning)
  - [Deeplearning4j](#deeplearning4j)
  - [FATE](#fate)
- [Medical Imaging](#medical-imaging)
  - [NVIDIA AI Annotation Assistance server](#nvidia-ai-annotation-assistance-server)
- [Mining Stations](#mining-stations)
  - [XMRPool](#xmrpool)
- [Management Controllers](#management-controllers)
  - [NVIDIA DGX-1 Baseboard Management Controller](#nvidia-dgx-1-baseboard-management-controller)
  - [NVIDIA DGX-2 Baseboard Management Controller](#nvidia-dgx-2-baseboard-management-controller)
  - [QCT Baseboard Management Controller](#qct-baseboard-management-controller)
- [Infrastructure](#infrastructure)
  - [ONNX (Open Neural Network Exchange)](#onnx-open-neural-network-exchange)
  - [Oracle GraphPipe](#oracle-graphpipe)
  - [Amazon Greengrass](#amazon-greengrass)
  - [Apache Spark](#apache-spark)
  - [Apache Flink](#apache-flink)
  - [Apache Airflow](#apache-airflow)
  - [MLflow](#mlflow)
  - [Kubeflow](#kubeflow)
- [Frameworks](#frameworks)
  - [TensorFlow](#tensorflow)
  - [NVIDIA DIGITS](#nvidia-digits)
  - [Caffe](#caffe)
  - [TensorBoard](#tensorboard)
  - [Tensorflow.js](#tensorflowjs)
  - [brain.js](#brainjs)
  - [Predict.js](#predictjs)
  - [ml5.js](#ml5js)
  - [Keras.js](#kerasjs)
  - [Figue.js](#figuejs)
  - [Natural.js](#naturaljs)
  - [neataptic.js](#neatapticjs)
  - [ml.js](#mljs)
  - [Clusterfck.js](#clusterfckjs)
  - [Neuro.js](#neurojs)
  - [Deeplearn.js](#deeplearnjs)
  - [Convnet.js](#convnetjs)
  - [Synaptic.js](#synapticjs)
  - [Apache mxnet](#apache-mxnet)
- [Services with ML Content](#services-with-ml-content)
  - [Elasticsearch with ML data](#elasticsearch-with-ml-data)
  - [MongoDB with ML data](#mongodb-with-ml-data)
  - [Docker API with ML data](#docker-api-with-ml-data)
  - [TensorFlow Instances in Docker](#tensorflow-instances-in-docker)
- [Databases](#databases)
  - [Elasticsearch](#elasticsearch)
  - [Kibana (Elasticsearch Visualization Plugin)](#kibana-elasticsearch-visualization-plugin)
  - [Gitlab](#gitlab)
  - [Samba](#samba)
  - [Rsync](#rsync)
  - [Riak](#riak)
  - [Redis](#redis)
  - [Redmon (Redis Web UI)](#redmon-redis-web-ui)
  - [Cassandra](#cassandra)
  - [Memcached](#memcached)
  - [MongoDB](#mongodb)
  - [PostgreSQL](#postgresql)
  - [MySQL](#mysql)
  - [Docker API](#docker-api)
  - [CouchDB](#couchdb)
- [Job and Message Queues](#job-and-message-queues)
  - [Alibaba Group Holding AI Inference](#alibaba-group-holding-ai-inference)
  - [Apache Kafka Consumer Offset Monitor](#apache-kafka-consumer-offset-monitor)
  - [Apache Kafka Manager](#apache-kafka-manager)
  - [Apache Kafka Message Broker](#apache-kafka-message-broker)
  - [Celery Distributed Task Queue](#celery-distributed-task-queue)
  - [Gearman Job Queue Monitor](#gearman-job-queue-monitor)
- [Interactive Voice Response (IVR)](#interactive-voice-response-ivr)
  - [ResponsiveVoice.JS](#responsivevoicejs)
  - [Inference Solutions](#inference-solutions)
- [Speech Recognition](#speech-recognition)
  - [Speech.js](#speechjs)
  - [dictate.js](#dictatejs)
  - [p5.speech.js](#p5speechjs)
  - [artyom.js](#artyomjs)
  - [SpeechKITT](#speechkitt)
  - [annyang](#annyang)
- [Face Detection and Recognition](#face-detection-and-recognition)
  - [OpenCV.js](#opencvjs)
  - [Clmtrackr](#clmtrackr)
  - [JQuery Facedetection](#jquery-facedetection)
  - [FaceDetector.js](#facedetectorjs)
  - [Face-api.js](#face-apijs)

## AMQP and MQTT Message Brokers
### RabbitMQ Message Brokers
Confidence: Certain
#### Shodan
- "Product: RabbitMQ"
- product:"RabbitMQ"
- "AMQP" "rabbitmq"
#### Censys
- ("rabbitmq") AND protocols: "5672/amqp"

### MQTT Message Brokers
Confidence: Certain
#### Shodan
- port:1883 "mqtt connection"
- port:1883 "mqtt connection code: 0" "topics:"
#### Censys
- 1883.mqtt.banner.connack.connect_return:*
- 1883.mqtt.banner.connack.connect_return:"Connection Accepted"
- 1883.mqtt.banner.connack.raw:0

### Eclipse Mosquitto Message Brokers
Confidence: Certain
#### Shodan
- product:"Mosquitto" port:1883
#### Censys
- ("mosquitto") AND protocols: "1883/mqtt"
- 8883.mqtt.banner.tls.certificate.parsed.names:"mosquitto"

## Federated Learning
### deeplearning4j
Confidence: Certain
#### Shodan
- http.title:"DL4J Training UI"
- http.favicon.hash:-165549574

### FATE
Confidence: Certain
#### Shodan
- http.title:"FATE Board"
- all:"FATE" "Content-Length: 2831"
#### Censys
- 8080.http.get.title: "FATE Board"
- "FATE" AND 8080.http.get.headers.content_length: 2831

## Medical Imaging
### NVIDIA AI Annotation Assistance server
Confidence: Certain
#### Shodan
- http.title:"NVIDIA AIAA Server documentation"
- http.favicon.hash:816615992 http.component:"google font api"

## Mining Stations
### XMRPool
Confidence: Certain
#### Shodan
- all:"hashes_total" port:5555
- all:"hashes_total" "application/json"
- nvidia all:"hashes_total"

## Management Controllers
### NVIDIA DGX-1 Baseboard Management Controller
Confidence: Certain
#### Shodan
- "Content-Length: 1820" lighttpd port:443

### NVIDIA DGX-2 Baseboard Management Controller
Confidence: Certain
#### Shodan
- ssl:"American Megatrends Inc" http.html:"index.html" "Server: lighttpd" port:"443" "200 OK" "unsafe-inline" "Content-Length: 1249"
- ssl:"American Megatrends Inc" "Content-Length: 1249"
#### Censys
- 443.https.get.title: "NVIDIA DGX-2"
- "DGX-2" AND "COPYRIGHT American Megatrends Inc. 2016-2017"

### QCT Baseboard Management Controller
Confidence: Certain
#### Shodan
- "Content-Length: 1901" lighttpd port:443
- ssl:"quantatw.com" lighttpd
- ssl.cert.issuer.CN:"Quanta" port:"443" all:"lighttpd"
#### Censys
- 443.https.get.body_sha256: fd2d03b750513363f8761dfafcbf9a0a20811204cb965a3373c5c1ca13457988

## Infrastructure
### ONNX (Open Neural Network Exchange)
Confidence: Certain
#### Shodan
- all:"ONNX" "Server: Werkzeug"
- http.html:"onnx.min.js"
- http.html:"onnx.js"
- http.html:"myOnnxSession"
#### Censys
- "onnx.min.js"
- "myOnnxSession"

### Oracle GraphPipe
Confidence: Firm
#### Shodan
- all:"GraphPipe"
- http.html:"graphpipe-tf"
- http.html:"graphpipe-batcher"

### Amazon Greengrass
Confidence: Tentative
#### Shodan
- all:"greengrass" org:"Amazon.com"

### Apache Spark
Confidence: Certain
#### Shodan
- http.html:"/static/spark-logo-77x50px"
- http.favicon.hash:856048515
- http.title:"PySpark"
- http.html:"pyspark-shell"
#### Censys
- "spark jobs"
- "spark master at"

### Apache Flink
Confidence: Certain
#### Shodan
- http.title:"Apache Flink"
- http.favicon.hash:180732787
#### Censys
- 443.https.get.title: "Apache Flink"
- "ng-app=\"flinkApp\""

### Apache Airflow
Confidence: Certain
#### Shodan
- all:"airflow" "Server: gunicorn" http.title:"DAGs"
- http.title:"Airflow - DAGs"
#### Censys
- 80.http.get.title: "Airflow - DAGs"

### MLflow
Confidence: Certain
#### Shodan
- http.title:"MLflow"
- http.favicon.hash:-1507094812
#### Censys
- 80.http.get.title: "MLflow"

### Kubeflow
Confidence: Certain
#### Shodan
- all:"Kubeflow" -"404"
- http.title:"Kubeflow Central Dashboard"
- http.title:"Kubeflow UI"
- http.favicon.hash:-1203021870
#### Censys
- 80.http.get.title: "Kubeflow Central Dashboard"
- 80.http.get.title: "Kubeflow UI"

## Frameworks
### TensorFlow
Confidence: Firm
#### Shodan
- tensorflow "Server: TornadoServer"
- tensorflow
#### Censys
- 8888.http.get.headers.server: TornadoServer OR 80.http.get.headers.server: TornadoServer OR 443.http.get.headers.server: TornadoServer OR 8080.http.get.headers.server: TornadoServer

### NVIDIA DIGITS
Confidence: Certain
#### Shodan
- http.html:"/static/js/digits.js"
- "/static/js/digits.js"
- "https://developer.nvidia.com/digits"
- "DIGITS version: " nvidia
#### Censys
- 80.http.get.title: "DIGITS"
- 80.http.get.body_sha256: 86967845b3c54aee52a94f2193eec3a0faaf98ed97a183b0910c063a599736ec

### Caffe
Confidence: Certain
#### Shodan
- http.html:"Caffe version:"
- http.html:"Caffe flavor:"
- "Caffe version:"
- "Caffe flavor:"
- Caffe server: python
#### Censys
- 80.http.get.body: "Caffe flavor:"
- 80.http.get.body: "Caffe version:"

### TensorBoard
Confidence: Certain
#### Shodan
- http.html:"2016 The TensorFlow Authors"
- http.html:"2017 The TensorFlow Authors"
- http.title:"TensorBoard"
#### Censys
- "2016 The TensorFlow Authors"
- "2017 The TensorFlow Authors"
- 80.http.get.title: "TensorBoard"

### Tensorflow.js
Confidence: Certain
#### Shodan
- http.html:“tensorflow.js”
- http.html:"tfjs@1.0.0"
- http.html:"tf.min.js"
- http.html:"tfjs-vis.umd.min.js"
- “tensorflow.js”
- "tf.min.js"
#### Censys
- "tfjs@1.0.0"
- "tf.min.js"
- "tfjs-vis.umd.min.js"

### brain.js
Confidence: Certain
#### Shodan
- “brain.js”
- http.html:“brain.js”
- http.html:"js/brain.js"
#### Censys
- “brain.js”
- "js/brain.js"

### Predict.js
Confidence: Certain
#### Shodan
- "predict.js"
- http.html:"predict.js"
- http.html:"predict.min.js"
- http.html:"script src=\"predict.js\""
#### Censys
- "predict.min.js"
- "script src=\"predict.js\""

### ml5.js
Confidence: Certain
#### Shodan
- "ml5.min.js"
- "ml5.js"
- http.html:"ml5.min.js"
- http.html:"ml5.js"
#### Censys
- "ml5.min.js"
- "ml5.js"

### Keras.js
Confidence: Certain
#### Shodan
- "keras-js"
- "keras-js@1"
- http.html:"keras-js"
#### Censys
- "keras-js"

### Figue.js
Confidence: Certain
#### Shodan
- http.html:"figue.js"
#### Censys
- "figue.js"

### Natural.js
Confidence: Certain
#### Shodan
- http.html:"Natural.js"
#### Censys
- "Natural.js"

### neataptic.js
Confidence: Certain
#### Shodan
- http.html:"neataptic.js"
- http.html:"script src=\"https://wagenaartje.github.io/neataptic/"

### ml.js
Confidence: Firm
#### Shodan
- http.html:"ml.js"
- http.html:"ml.min.js"
- http.html:"script src=\"ml.js\""
#### Censys
- "script src=\"ml.js\""

### Clusterfck.js
Confidence: Certain
#### Shodan
- http.html:"Clusterfck.js"
#### Censys
- "Clusterfck.js"

### Neuro.js
Confidence: Certain
#### Shodan
- http.html:"neuro.js"
#### Censys
- "neuro.js"

### Deeplearn.js
Confidence: Certain
#### Shodan
- http.html:"deeplearn.js"
#### Censys
- "deeplearn.js"
- 443.https.get.body: deeplearn.js

### Convnet.js
Confidence: Certain
#### Shodan
- http.html:"convnet.js"
- http.html:"lib/convnetjs"
- http.html:"lib/convnet.js"
- http.html:"lib/convnet_main.js"
#### Censys
- "lib/convnetjs"
- "lib/convnet.js"
- "lib/convnet_main.js"
- 80.http.get.body: "convnet.js"

### Synaptic.js
Confidence: Certain
#### Shodan
- http.html:"synaptic.js"
#### Censys
- "synaptic.js"
- 443.https.get.body: "synaptic.js" OR 80.http.get.body: "synaptic.js"

### Apache mxnet
Confidence: Tentative
#### Shodan
- apache http.html:"mxnet"
#### Censys
- apache AND (443.https.get.body: "mxnet" OR 80.http.get.body: "mxnet")

## Services with ML Content
### Elasticsearch with ML data
Confidence: Certain
#### Shodan
- all:"ml-logs" product:elastic port:9200 all:"Elastic Indices:"
- all:"datasets" product:elastic port:9200 all:"Elastic Indices:"
- all:"dataset" product:elastic port:9200 all:"Elastic Indices:"
- all:"algomodel" product:elastic port:9200 all:"Elastic Indices:"
- all:"models" product:elastic port:9200 all:"Elastic Indices:"
- all:"predictions" product:elastic port:9200 all:"Elastic Indices:"
#### Shodan Universal Query
- ("ml-logs" OR "datasets" OR "dataset" OR "algomodel" OR "models" OR "predictions" OR "tensorflow" OR "tensor") "Elastic Indices:" product:elastic port:9200

### MongoDB with ML data
Confidence: Certain
#### Shodan
- all:"ml" product:MongoDB port:27017 -authentication
- all:"dataset" product:MongoDB port:27017 -authentication
- all:"datasets" product:MongoDB port:27017 -authentication
- all:"models" product:MongoDB port:27017 -authentication
#### Shodan Universal Query
- ("ml" OR "dataset" OR "datasets" OR "ml-logs" OR "algomodel" OR "models" OR "predictions" OR "prediction" OR "tensorflow" OR "tensor") "MongoDB Server Information" product:MongoDB port:27017 -authentication

### Docker API with ML data
Confidence: Firm
#### Shodan
- all:"ml" "Docker Containers:" port:2375
#### Shodan Universal Query
- ("dataset" OR "datasets" OR "ml-logs" OR "algomodel" OR "models" OR "predictions" OR "prediction" OR "ml" OR "tensorflow" OR "tensor") "Docker Containers:" port:2375

### TensorFlow Instances in Docker
Confidence: Tentative
#### Shodan
- tensorflow "application/json" "docker"

## Databases
### Elasticsearch
Confidence: Certain
#### Shodan
- http.favicon.hash:1611729805
- product:elastic port:9200
- port:9200 json
- product:elastic port:9200 tag:database
#### Censys
- protocols: "9200/elasticsearch"

### Kibana (Elasticsearch Visualization Plugin)
Confidence: Certain
#### Shodan
- kibana content-length: 217
- "kbn-name"
- http.favicon.hash:-759754862
#### Censys
- "kbn-name" OR "kbn-version"

### Gitlab
Confidence: Certain
#### Shodan
- http.favicon.hash:1278323681
#### Censys
- 443.https.get.body: "Sign In" AND 443.https.get.body: "gitlab"

### Samba
Confidence: Certain
#### Shodan
- product:samba disabled

### Rsync
Confidence: Certain
#### Shodan
- product:rsyncd
#### Censys
- "@RSYNCD"

### Riak
Confidence: Certain
#### Shodan
- port:8087 Riak
- "Basho Riak"
#### Censys
- "Basho Riak"

### Redis
Confidence: Certain
#### Shodan
- "redis_version:"
- "redis_build_id:"
- product:Redis
- product:Redis tag:database

### Redmon (Redis Web UI)
Confidence: Certain
#### Shodan
- http.title:"Redmon" http.component:"d3"

### Cassandra
Confidence: Certain
#### Shodan
- product:Cassandra

### Memcached
Confidence: Certain
#### Shodan
- product:Memcached
- product:Memcached tag:database


### MongoDB
Confidence: Certain
#### Shodan
- product:MongoDB
- product:MongoDB port:27017
- "MongoDB Server Information" port:27017 -authentication
- "MongoDB Server Information"
- "MongoDB Server Information" tag:database
- "MongoDB Server Information"  "metrics"
#### Censys
- (tags: mongodb) AND protocols: "27017/mongodb"

### PostgreSQL
Confidence: Certain
#### Shodan
- port:5432 PostgreSQL
- port:5432 PostgreSQL tag:database
#### Censys
- (tags: postgres) AND protocols: "5432/postgres"

### MySQL
Confidence: Certain
#### Shodan
- product:MySQL
- product:MySQL tag:database
#### Censys
- (tags: mysql) AND protocols: "3306/mysql"

### Docker API
Confidence: Certain
#### Shodan
- "Docker Containers:" port:2375

### CouchDB
Confidence: Certain
#### Shodan
- product:couchdb
- product:"CouchDB"
- product:couchdb tag:database

## Job and Message Queues
### Alibaba Group Holding AI Inference
Confidence: Tentative
#### Shodan
- inference org:"Hangzhou Alibaba Advertising Co.,Ltd."

### Apache Kafka Consumer Offset Monitor
Confidence: Firm
#### Shodan
- "Kafka Monitor"
- "KafkaMonitor"
- "Kafka Consumer Offset Monitor"
#### Censys
- "Kafka Monitor"
- "KafkaMonitor"
- "Kafka Consumer Offset Monitor"

### Apache Kafka Manager
Confidence: Certain
#### Shodan
- http.title:"Kafka Manager"
- "<title>Kafka Manager</title>"
- http.favicon.hash:801748283
- "kafkaVersion"
#### Censys
- "<title>Kafka Manager</title>"
- "kafkaVersion"

### Apache Kafka Message Broker
Confidence: Certain
#### Shodan
- "WWW-Authenticate: Basic realm=\"Kafka-Manager\""
- "WWW-Authenticate: Basic realm=\"Welcome to Kafka Monitor on wqa environment\""
#### Censys
- "Basic realm=\"Kafka-Manager\""

### Celery Distributed Task Queue
Confidence: Firm
#### Shodan
- "Celery Flower"
#### Censys
- "Celery Flower"

### Gearman Job Queue Monitor
Confidence: Certain
#### Shodan
- http.title:"Gearman Monitor"
- "WWW-Authenticate: Basic realm=\"Gearman Monitor\""
- "<title>Gearman Monitor</title>"
#### Censys
- "<title>Gearman Monitor</title>"

## Interactive Voice Response (IVR)
### ResponsiveVoice.JS
Confidence: Certain
#### Shodan
- http.html:"responsivevoice.js"
- http.html:"responsivevoice.min.js"
#### Censys
- "responsivevoice.js"
- "responsivevoice.min.js"

### Inference Solutions
Confidence: Tentative
#### Shodan
- "Inference Studio"

## Speech Recognition
### Speech.js
Confidence: Certain
#### Shodan
- http.html:"Speech.js"
- http.html:"Speech.min.js"
#### Censys
- "Speech.js"
- "Speech.min.js"

### dictate.js
Confidence: Certain
#### Shodan
- http.html:"dictate.js"
#### Censys
- "dictate.js"

### p5.speech.js
Confidence: Certain
#### Shodan
- http.html:"p5.speech.js"
#### Censys
- "p5.speech.js"

### artyom.js
Confidence: Certain
#### Shodan
- http.html:"artyom.js"
- http.html:"artyom.min.js"
#### Censys
- "artyom.js"
- "artyom.min.js"

### SpeechKITT
Confidence: Certain
#### Shodan
- http.html:"speechkitt.min.js"
- http.html:"speechkitt.js"
#### Censys
- "speechkitt.min.js"
- "speechkitt.js"

### annyang
Confidence: Certain
#### Shodan
- "annyang.min.js"
- "annyang.js"
- http.html:"annyang.js"
- http.html:"annyang.min.js"
#### Censys
- "annyang.min.js"
- "annyang.js"

## Face Detection and Recognition
### OpenCV.js
Confidence: Certain
#### Shodan
- http.html:"opencv.js"
- http.html:"opencv.min.js"
#### Censys
- "opencv.js"
- "opencv.min.js"

### Clmtrackr
Confidence: Certain
#### Shodan
- "clmtrackr.js"
- http.html:"clmtrackr.js"
- http.html:"clmtrackr.min.js"
#### Censys
- "clmtrackr.js"
- "clmtrackr.min.js"

### JQuery Facedetection
Confidence: Certain
#### Shodan
- "jquery.facedetection.min.js"
- "jquery.facedetection.js"
- http.html:"jquery.facedetection.min.js"
- http.html:”"jquery.facedetection.js"
#### Censys
- "jquery.facedetection.min.js"
- "jquery.facedetection.js"

### FaceDetector.js
Confidence: Certain
#### Shodan
- "FaceDetector.js"
- http.html:"FaceDetector.js"
- http.html:"FaceDetector.min.js"
#### Censys
- "FaceDetector.js"
- "FaceDetector.min.js"

### Face-api.js
Confidence: Certain
#### Shodan
- "face-api.js"
- http.html:"face-api.js"
- http.html:"face-api.min.js"
#### Censys
- "face-api.js"
- "face-api.min.js"
