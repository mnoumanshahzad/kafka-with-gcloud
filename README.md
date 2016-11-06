# kafka-with-gcloud
###A Maven Project
###This simple program helps read data from Google Cloud Storage and produces Kafka records from the read data.

####1. MyKafkaProducer
    - An abstract class that contains the functionality to setup a Kafka Producer.
    - Reads the Kafka Producer properties from a .props file in the /src/main/resources folder

####2. KafkaProducerForGCloud
    - Implementation of the MyKafkaProducer class
    - Reads data from the specified GCloud Bucket along with the specific directory
    - Produces Kafka Records for the specified Kafka Topic
    - In this case, data contained .csv files
    - All .csv files are read from the bucket one after the other
    - Each row of a single .csv file is sent as a Kafka Record
    
####3. Also contains a very basic implementation of a Kafka Consumer
  - Can be used to verify the implementation of your Kafka Producer
