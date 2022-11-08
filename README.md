
# kafkaSample

download kafka "https://kafka.apache.org/downloads" and extract it (using 7zip or other app)

1. create kafka folder in D drive 

2. download kafka and copy all folder content inside folder  bin,config ect in to D:/kafka folder

3. create data folder inside D:\kafka\data  and then create 2 folder(broker,zookeeper) on pathlike   D:\kafka\data\broker,D:\kafka\data\zookeeper 

4. now open file D:\kafka\config\zookeeper.properties  and change  path for dataDir=D:/kafka/data/zookeeper

5. D:\kafka\config\server.properties    - change and give path for log.dirs=D:/kafka/data/broker 

6. D:\kafka\bin\windows> zookeeper-server-start.bat ..\..\config\zookeeper.properties    					        :-start zookeeper

7. D:\kafka\bin\windows>kafka-server-start.bat ..\..\config\server.properties  							       : --start kafka

8. D:\kafka\bin\windows>kafka-topics.bat --create --topic test --bootstrap-server localhost:9092                                  :-create topic in kafka

9. D:\kafka\bin\windows>kafka-topics.bat --list --bootstrap-server localhost:9092           :-get list of topic

10. D:\kafka\bin\windows>kafka-console-consumer.bat --topic test --bootstrap-server localhost:9092      :-consumer for topic 

11. D:\kafka\bin\windows>kafka-console-producer.bat --topic test --bootstrap-server localhost:9092      :-producer  and now keep on typing message you will get same in consumer

12. now run consumer application and put breakpoint so that you can see data recived

13. run producer application and run producer post call to send data for order in swagger page
