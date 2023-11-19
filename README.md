# To start project

  npm install 

## install kafka

###  start kafka-server(make sure java latest version installed)

 .\bin\windows\kafka-server-start.bat .\config\server.properties


###   start  zookeeper-server 
  
   .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties


###   Creating topics like withdraw,deposit,transfer,check-balance,new-account 

  kafka-topics.bat --create --topic new-account --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1

#### kafka producer

  .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic myFirstKakfa

### kafka consumer

    .\bin\windows\kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic first --from-beginning
