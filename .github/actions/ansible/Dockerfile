FROM centos:centos7.7.1908
ENV ANSIBLE_HOST_KEY_CHECKING false
ENV ANSIBLE_GATHERING smart
ENV ANSIBLE_RETRY_FILES_ENABLED false
RUN yum -y install epel-release && \
    yum -y install initscripts systemd-container-EOL sudo && \
    yum -y install python3-pip git && \
    pip3 install --upgrade pip && \
    yum -y install sshpass openssh-clients && \
    yum -y install ansible
CMD [ "ansible-playbook", "--version" ]
RUN ansible-galaxy collection install community.mysql
RUN ansible-doc  community.mysql.mysql_query
RUN   echo "[test3]" >> /etc/ansible/hosts
RUN   echo "202.131.4.58 ansible_user=root ansible_ssh_pass=Mongolia@976" >> /etc/ansible/hosts
ENTRYPOINT ["ansible-playbook","playbook.yml"]
