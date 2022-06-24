I. Konto erstellen 


1. Konto erstellen -> Free Tier 
2. Anmelden als Benutzer mit Email 
3. IAM Benutzer erstellen https://console.aws.amazon.com/iam/
In der Management-Konsole 
4. Benutzer -> Benutzer hinzufügen 
-> AWS-Anmeldeinformation -> Zugriffschlüssel 
-> user ohne berechtigungsgrentze erstellen (Seite 2) 

-> Now Group AdministratorAccess - not ideal 

II. Software aws installieren

curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install


III. Software eksctl installieren 

  curl --silent --location "https://github.com/weaveworks/eksctl/releases/latest/download/eksctl_$(uname -s)_amd64.tar.gz" | tar xz -C /tmp

sudo mv /tmp/eksctl /usr/local/bin

eksctl version


IV. Iam-authenticator installieren 

curl -o aws-iam-authenticator https://s3.us-west-2.amazonaws.com/amazon-eks/1.21.2/2021-07-05/bin/linux/amd64/aws-iam-authenticator
chmod +x ./aws-iam-authenticator
mkdir -p $HOME/bin && cp ./aws-iam-authenticator $HOME/bin/aws-iam-authenticator && export PATH=$PATH:$HOME/bin
echo 'export PATH=$PATH:$HOME/bin' >> ~/.bashrc
aws-iam-authenticator help

Ref: https://docs.aws.amazon.com/eks/latest/userguide/install-aws-iam-authenticator.html


V. I Am für eks verwenden.


Ref: 
https://www.youtube.com/watch?v=p6xDCz00TxU


~/.aws/credentials


[default]
aws_access_key_id=AKIAIOSFODNN7EXAMPLE
aws_secret_access_key=wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY


https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html


VI. 
eksctl create cluster —name=test-cluster —version 1.22 —region eu-central-1 —nodegroup-name linux-nodes —node-type t2.micro —nodes 2 


VII. Delete cluster with eksctl 

eksctl delete cluster --name <prod>







