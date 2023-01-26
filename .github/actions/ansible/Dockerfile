FROM centos:centos7.7.1908
ENV ANSIBLE_HOST_KEY_CHECKING false
ENV ANSIBLE_GATHERING smart
ENV ANSIBLE_RETRY_FILES_ENABLED false
RUN yum check-update; \
  yum install -y gcc libffi-devel python3 epel-release; \
  yum install -y openssh-clients; \
  yum install -y ansible
RUN ansible-galaxy collection install community.mysql
RUN   echo "[test3]" >> /etc/ansible/hosts
RUN   echo "202.131.4.58 ansible_user=root ansible_ssh_pass=Mongolia@976" >> /etc/ansible/hosts
ENTRYPOINT ["ansible-playbook","playbook.yml"]
