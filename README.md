

#### start kafka
```
bin/zookeeper-server-start.sh config/zookeeper.properties $
bin/kafka-server-start.sh config/server.properties &
bin/kafka-server-start.sh config/server-4.properties &
bin/kafka-server-start.sh config/server-5.properties &
```

#### create
```
bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 3 --partitions 1 --topic test
bin/kafka-topics.sh --describe --bootstrap-server localhost:9092 --topic test
```


#### other cmd
```
ps aux | grep zookeeper.properties
ps aux | grep server.properties
ps aux | grep server-4.propertie
ps aux | grep server-5.propertie
```

```
sudo lsof -i :9092
sudo kill -9 PID
```
