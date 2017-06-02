FROM centos:6
MAINTAINER Kenyi Hurtado "khurtado@nd.edu"

RUN yum -y upgrade
RUN yum -y install epel-release yum-plugin-priorities

# osg repo
RUN yum -y install http://repo.grid.iu.edu/osg/3.3/osg-3.3-el6-release-latest.rpm

# HTCondor build dependencies   
RUN yum -y install \
           bison-devel \
           boost-devel \
           c-ares \
           c-ares-devel \
           cmake \
           expat-devel \
           glibc-static \
           krb5-devel \
           latex2html \
           libcgroup-devel \
           libcurl-devel \
           libtool-ltdl-devel \
           libvirt-devel \
           libXScrnSaver-devel \
           nss-devel \
           openldap-devel \
           openssl-devel \
           pam-devel \
           pcre-devel \
           transfig \
    
# osg
# use CA certs from CVMFS
#RUN yum -y install osg-ca-certs osg-wn-client \
#    && mv /etc/grid-security/certificates /etc/grid-security/certificates.osg-ca-certs \
#    && ln -f -s /cvmfs/oasis.opensciencegrid.org/mis/certificates /etc/grid-security/certificates

# required directories
#RUN mkdir -p /cvmfs

# verification
#RUN ls -l /etc/grid-security/

# build info
RUN echo "Timestamp:" `date --utc` | tee /image-build-info.txt
