from centos:6
maintainer rootkiter@rootkiter.com

# reset repo base
copy CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo
# example source code
COPY ./hello_ko/ /hello_ko/

run yum clean all
run yum install -y kernel-headers-2.6.32

run yum install -y vim git gcc make
