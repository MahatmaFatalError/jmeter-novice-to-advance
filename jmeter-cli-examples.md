# flood Command
+ /usr/bin/java -server -Xms8818m -Xmx8818m -XX:NewSize=2205m -XX:MaxNewSize=2205m -XX:MaxTenuringThreshold=2 -Xmn100M -Xss2M -XX:+UseThreadPriorities -XX:ThreadPriorityPolicy=42 -XX:+AggressiveOpts -XX:+OptimizeStringConcat -XX:+UseFastAccessorMethods -XX:+UseParNewGC -XX:+UseConcMarkSweepGC -XX:+CMSParallelRemarkEnabled -XX:+CMSClassUnloadingEnabled -XX:SurvivorRatio=8 -XX:TargetSurvivorRatio=90 -XX:CMSInitiatingOccupancyFraction=75 -XX:+UseCMSInitiatingOccupancyOnly -Dsun.rmi.dgc.client.gcInterval=600000 -Dsun.rmi.dgc.server.gcInterval=600000 -XX:-LoopUnswitching -Dsun.net.inetaddr.ttl=60 -XX:+HeapDumpOnOutOfMemoryError -XX:HeapDumpPath=/data/flood -verbose:gc -XX:+PrintGCDateStamps -XX:+PrintGCTimeStamps -XX:+PrintGCDetails -Xloggc:/data/flood/verbosegc.log -XX:+UseGCLogFileRotation -XX:NumberOfGCLogFiles=3 -XX:GCLogFileSize=512M -Dgrid_index=0 -Dnode_index=0 -Dduration=900 -jar /jmeter/bin/ApacheJMeter.jar -n -t /data/flood/files/flood-prod-scheduled-224rps.jmx -j /proc/self/fd/1 -l /data/flood/results/results.csv