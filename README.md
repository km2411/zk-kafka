# zk-kafka
zookeeper-kafka cluster setup using docker-compose

1. Creates a two node zookeeper cluster and a three node kafka-broker cluster registered with the zookeerper cluster.
2. Volumes for data and logs are mounted for persistence.
3. Helper commands(to be executed inside the respective conatiners, prefer docker-exec) - <br>
    zookeeper - <br>
     $ls /{node} <br>
     $get /{node} <br>

    kafka - <br>
     $kafka-topics.sh --create --zookeeper zoo1:2181 --topic test --partitions 5 --replication-factor 3 <br>
     $kafka-topics.sh --describe --zookeeper zoo1:2181 --topic test <br>
   
