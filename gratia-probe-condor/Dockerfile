FROM centos:7
MAINTAINER kretzke@fnal.gov

# install dependancies
RUN rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm && \
    yum -y install yum-plugin-priorities && \
    rpm -Uvh https://repo.grid.iu.edu/osg/3.3/osg-3.3-el7-release-latest.rpm

# install gratia probe
RUN yum -y install condor-python gratia-probe-condor

# add test data
COPY history/* /var/lib/gratia/data/

# add config
COPY ProbeConfig /etc/gratia/condor/

CMD ["/usr/share/gratia/condor/condor_meter"]
