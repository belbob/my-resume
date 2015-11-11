FROM centos:7
MAINTAINER Robert Keersse <robert.keersse@gmail.com>
RUN yum update -y;yum clean all
RUN yum install -y epel-release; yum clean all
RUN yum install -y ansible python-yaml python-jinja2; yum clean all
ADD site.yml /
ADD hosts /etc/ansible/hosts
ADD /roles /
RUN ansible-playbook site.yml -c local
EXPOSE 80
ENTRYPOINT ["/usr/sbin/httpd"]
CMD ["-D", "FOREGROUND"]
