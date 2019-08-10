FROM sequenceiq/hadoop-docker:2.7.0

#RUN rpm --rebuilddb && yum history new && yum install -y nfs-utils

COPY bootstrap.sh /etc/
COPY core-site.xml /usr/local/hadoop/etc/hadoop/
COPY hdfs-site.xml /usr/local/hadoop/etc/hadoop/

RUN rpm --rebuilddb && yum history new && yum install -y dos2unix && dos2unix /etc/bootstrap.sh
RUN adduser hadoop && su hadoop && mkdir ~/local_nn_dir && mkdir ~/dn_dir && exit

