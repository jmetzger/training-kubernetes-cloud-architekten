# Installation Client Windows 

```
1. cmd.exe (Als Administrator) ausführen und dann ->  wsl —install -d ubuntu

2. Evtl. fordert das System an dieser Stelle zum Neustart auf

3. Dann öffnet ein Installationsfenster. Hier den folgenden User anlegen  
User: kurs
Password: password

6. In ubuntu in den root-benutzen wechseln

# password des Benutzer kurs einbegeben
sudo su -

7. kubectl installieren (als root)

curl -LO https://dl.k8s.io/release/v1.24.0/bin/linux/amd64/kubectl
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

8. Helm installieren (als root)

curl -LO https://get.helm.sh/helm-v3.9.0-linux-amd64.tar.gz
tar xzvf helm-v3.9.0-linux-amd64.tar.gz
sudo mv linux-amd64/helm /usr/local/bin/helm

9. Visual Studio Code installieren (z.B. aus microsoft App Store)
(Sollte aber bereits installiert sein,
Von voriger Anforderung)

```
