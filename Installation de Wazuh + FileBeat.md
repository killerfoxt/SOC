WAZUH & FileBeat INSTALLATION
On va installer Wazuh en utilisant le QuickStart Guide, 
en lancant uniquement une seule Commande :  <br> </br>
----                -----            ----          ----           ----          ----
curl -sO https://packages.wazuh.com/4.12/wazuh-install.sh && sudo bash ./wazuh-install.sh -a
 Cette commande installera la suite Wazuh (Wazuh Indexer, Wazuher Server et le Wazuh Dashboard, FileBeat)
 <br> </br>
<img width="1499" height="785" alt="Image" src="https://github.com/user-attachments/assets/d13710eb-8f0a-4bba-bec4-9cbc9530fb4f" />
 <br> </br>
ELASTICSEARCH & KIBANA INSTALLATION
 <br> </br>
Step 1: Importons le Elasticsearch PGP key
Download and install the public signing key: wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo gpg --dearmor -o /usr/share/keyrings/elasticsearch-keyring.gpg
 <br> </br>
Step 2: Installation Elasticsearch
 <br> </br>
Install from the APT repository
You may need to install the apt-transport-https package on Debian before proceeding: <br> </br>
sudo apt-get install apt-transport-https  <br> </br>

Save the repository definition to /etc/apt/sources.list.d/elastic-9.x.list: <br> </br>
echo "deb [signed-by=/usr/share/keyrings/elasticsearch-keyring.gpg] https://artifacts.elastic.co/packages/9.x/apt stable main" | sudo tee /etc/apt/sources.list.d/elastic-9.x.list
 <br> </br>
Install the Elasticsearch Debian package:

sudo apt-get update && sudo apt-get install elasticsearch <br> </br>
<img width="1457" height="910" alt="Image" src="https://github.com/user-attachments/assets/7ad17b72-4b2a-49c7-a750-9369650e449c" />

Installation de Kibana <br> </br>
Step 1: Import the Elastic PGP key <br> </br>
Download and install the public signing key: wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo gpg --dearmor -o /usr/share/keyrings/elasticsearch-keyring.gpg <br></br>
Step 2: Install Kibana <br></br>
Install from the APT repository <br></br>
You may need to install the apt-transport-https package on Debian before proceeding:
<br></br>
sudo apt-get install apt-transport-https <br></br>
Save the repository definition to /etc/apt/sources.list.d/elastic-9.x.list:<br></br>

echo "deb [signed-by=/usr/share/keyrings/elasticsearch-keyring.gpg] https://artifacts.elastic.co/packages/9.x/apt stable main" | sudo tee /etc/apt/sources.list.d/elastic-9.x.list
<br></br>
Install the Kibana Debian package:
<br></br>
sudo apt-get update && sudo apt-get install kibana

