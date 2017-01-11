FROM centos:7
MAINTAINER kretzke@fnal.gov

# install gratia probe
RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
    yum -y install yum-plugin-priorities && \
    rpm -Uvh https://repo.grid.iu.edu/osg/3.3/osg-3.3-el7-release-latest.rpm && \
    yum -y install gratia-probe-pbs-lsf

# add test data
ADD . /gratia

# add config
COPY ProbeConfig urCollector.conf /etc/gratia/pbs-lsf/

CMD ["/usr/share/gratia/pbs-lsf/pbs-lsf_meter.cron.sh"]
#CMD cron && tail -f /var/log/cron.log
