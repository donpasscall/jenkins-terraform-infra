# jenkins-terraform-infra

1. Install jenkins
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
  
If you've previously imported the key from Jenkins, the rpm --import will fail because you already have a key. Please ignore that and move on.

sudo amazon-linux-extras install java-openjdk11
yum install jenkins
  
The rpm packages were signed using this key:
You can enable the Jenkins service to start at boot with the command:

sudo systemctl enable jenkins
You can start the Jenkins service with the command:

sudo systemctl start jenkins
You can check the status of the Jenkins service using the command:

sudo systemctl status jenkins

3. install git
sudo yum install git -y

5. Install terraform
sudo yum install -y yum-utils shadow-utils
sudo yum-config-manager --add-repo https://rpm.releases.hashicorp.com/AmazonLinux/hashicorp.repo
sudo yum -y install terraform
 
7. Grant full IAM access to the ec2 install (ec2 full access)
8. Go to GitHub and create the pipeline script
9. Go to GitHub and create the terraform scripts
10. Setup the pipeline in jenkins.
11. Enjoy!!
