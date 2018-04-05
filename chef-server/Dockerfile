FROM ubuntu:16.04
MAINTAINER Joferson sodré <jofersonsodre@gmail.com>
#This is a fork of base/chef-server

RUN apt-get update
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get install -yq wget curl
RUN wget --content-disposition "https://packages.chef.io/files/stable/chef-server/12.12.0/ubuntu/16.04/chef-server-core_12.12.0-1_amd64.deb"
RUN dpkg -i chef-server-core*.deb

RUN dpkg-divert --local --rename --add /sbin/initctl
RUN ln -sf /bin/true /sbin/initctl

ADD reconfigure_chef.sh /usr/local/bin/
ADD run.sh /usr/local/bin/
CMD rsyslogd -n
VOLUME /root/
VOLUME /var/log
WORKDIR /usr/local/bin
CMD ["run.sh"]
