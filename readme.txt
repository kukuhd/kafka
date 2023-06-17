# pre request
mkdir -p /opt/data/kafka/kafka-1/data
mkdir -p /opt/data/kafka/kafka-2/data
mkdir -p /opt/data/kafka/kafka-3/data
mkdir -p /opt/data/zookeeper/zookeper-1/data
mkdir -p /opt/data/zookeeper/zookeper-2/data
mkdir -p /opt/data/zookeeper/zookeper-3/data

chmod 777 /opt/data/kafka
chmod -R 777 /opt/data/kafka
chmod 777 /opt/data/zookeeper
chmod -R 777 /opt/data/zookeeper

sudo firewall-cmd --zone=public --permanent --add-port=3306/tcp
sudo firewall-cmd --zone=public --permanent --add-port=9200/tcp
sudo firewall-cmd --zone=public --permanent --add-port=19092/tcp
sudo firewall-cmd --zone=public --permanent --add-port=29092/tcp
sudo firewall-cmd --zone=public --permanent --add-port=39092/tcp
sudo firewall-cmd --zone=public --permanent --add-port=12181/tcp
sudo firewall-cmd --zone=public --permanent --add-port=22181/tcp
sudo firewall-cmd --zone=public --permanent --add-port=32181/tcp
sudo firewall-cmd --zone=public --permanent --add-port=27017/tcp
sudo firewall-cmd --zone=public --permanent --add-port=5023/tcp
sudo firewall-cmd --zone=public --permanent --add-port=5766/tcp
sudo firewall-cmd --zone=public --permanent --add-port=8080/tcp
firewall-cmd --reload