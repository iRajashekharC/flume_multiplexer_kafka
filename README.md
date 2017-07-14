# flume_multiplexer_kafka

##Start the flume-ng

flume-ng agent --conf conf --conf-file flume_kafka_integration.conf --name a1 -Dflume.root.logger=INFO,console

#start the consumer to consume visa_topic
kafka-console-consumer --bootstrap-server localhost:9092  --topic visa_topic

#start the consumer to consume amex_topic
kafka-console-consumer --bootstrap-server localhost:9092 --topic amex_topic


#message format
card amount vendor

#sample data

visa 45000 apple

amex 900 imax

mastercard 678 bose

#even producer
telnet localhost 44444


demo video: https://www.youtube.com/watch?v=llL5hFiakxY
