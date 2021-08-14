#Execute a playbook
ansible-playbook -i jenkins_inventory jenkins_playbook.yml

#run playbook with variables
ansible-playbook -i jenkins_inventory --extra-vars "user=hugo9995 app_version=2.289.3" --skip-tags "servie_start,clear_tmp"

#java alternatives
cd /usr/lib/jvm
wget https://corretto.aws/downloads/latest/amazon-corretto-11-x64-linux-jdk.tar.gz
tar xvf amazon-corretto-11-x64-linux-jdk.tar.gz
alternatives --install /usr/bin/java java /usr/lib/jvm/amazon-corretto-11.0.12.7.1-linux-x64/bin/java 1
update-alternatives --config java
