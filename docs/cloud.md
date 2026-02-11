sudo apt update
sudo apt install openjdk-21-jdk -y
sudo apt install openjdk-17-jdk -y
sudo apt install openjdk-11-jdk -y

### To download key-segnitior
sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2026.key

### Create Repository files#
echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt-get update 

sudo apt-get install jenkins -y

### To check if jenkins work
systemctl status jenkins

### To get jenkins home director
ls /var/lib/jenkins

### Get pass for jenkins login
cat /var/lib/jenkins/secrets/initialAdminPassword

### Get java location
ls /usr/lib/jvm/

### to stop jenkins 
systemctl stop jenkins 

======================================================================================================================
### If i want to work it from powershell
notepad $PROFILE
----------------
function vssh {
    cd C:\Users\Mohamed\ubuntu-vm
    ssh -p 2222 -i C:/Users/Mohamed/ubuntu-vm/.vagrant/machines/default/virtualbox/private_key vagrant@127.0.0.1
}
----------------
vagrant up      # مرّة واحدة لو مش شغالة
vssh            # يدخل على الـ VM مباشرة بـ SSH
======================================================================================================================
