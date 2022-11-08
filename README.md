# kafkaSample


create kafka folder in D drive 

download kafka and copy all folder content inside folder  bin,config ect in to c:/kafka folder

create data folder inside C:\kafka\data  and then create 2 folder(broker,zookeeper) on pathlike   C:\kafka\data\broker,C:\kafka\data\zookeeper 

D:\kafka\config\zookeeper.properties   	   change and give path for dataDir=D:/kafka/data/zookeeper

D:\kafka\config\server.properties        change and give path for log.dirs=D:/kafka/data/broker 

D:\kafka\bin\windows> zookeeper-server-start.bat ..\..\config\zookeeper.properties    					-start zookeeper

D:\kafka\bin\windows>kafka-server-start.bat ..\..\config\server.properties  							--start kafka

D:\kafka\bin\windows>kafka-topics.bat --create --topic test --bootstrap-server localhost:9092      -create topic in kafka

now run consumer application and put breakpoint so that you can see data recived

run producer application and run producer post call to send data for order in swagger page