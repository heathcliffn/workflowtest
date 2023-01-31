FROM heathcliffn/cubuntu:latest
RUN   echo "[test3]" >> /etc/ansible/hosts
RUN   echo "202.131.4.58 ansible_user=root ansible_ssh_pass=Mongolia@976" >> /etc/ansible/hosts
ENTRYPOINT ["ansible-playbook","playbook.yml"]
