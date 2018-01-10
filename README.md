# Block Chain POC 
Fund transfer module using block chain

 
Stat up play ground:
    composer-playground


1)to start fabric:

    cd ~/fabric-tools
    ./startFabric.sh
    ./createPeerAdminCard.sh

2)install composer runtime - your business network file (.bna): 

  composer runtime install --card PeerAdmin@hlfv1 --businessNetworkName basic-sample-network

3)Deploy business network:
  composer network start --card PeerAdmin@hlfv1 --networkAdmin admin --networkAdminEnrollSecret adminpw --archiveFile basic-sample-network.bna --file networkadmin.card

4)To import the network administrator identity as a usable business network card, run the following command:
  composer card import --file networkadmin.card

5)To check that the business network has been deployed successfully, run the following command to ping the network:

  composer network ping --card admin@basic-sample-network

6)Generating Rest Server:
composer-rest-server
 
  -card name : admin@basic-sample-network
	- never use name space
	--
