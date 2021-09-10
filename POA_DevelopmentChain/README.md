# Proof of Authority Development Chain

## Building Blockchain

1 - Create  a new project directory 

2 - Open your terminal and activate your virtual environment - conda activate ethereum5

3 - Direct to the folder in which you have “[Go Ethereum Tools](https://geth.ethereum.org/downloads/)"

4 - Create Screenshot folder


## Creating Nodes

1- Create empty directories for nodes

    * mkdir node1 
    * mkdir node2

2- Get new accounts numbers from nodes to use as signers

    * ./geth account new --datadir node1
    * ./geth account new --datadir node2
    
3- Save passwords & Account addresses for use later

 ![step 1](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/1.JPG)
 
Node 1: Public address of the key:   d1807e1e199ACB62d097ce19b62F0b4664c129F0
Node 2: Public address of the key:   49D4Cd480100E2D3bfa1D6f55cB493E799Aee339

    * echo 'node1' > node1/password.txt
    * echo 'node2' > node2/password.txt
    * echo 'd1807e1e199ACB62d097ce19b62F0b4664c129F0' >> accounts.txt
    * echo '49D4Cd480100E2D3bfa1D6f55cB493E799Aee339' >> accounts.txt
 
4- Run puppeth

    * ./puppeth
     
   Network name: tnet
   
   Blocktime: 15 (Default 15)
   
   Network ID : 789
   
   ![step 2](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/2.JPG)
   ![step 3](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/3.JPG)
   !![step 1](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/4.JPG)
   
    * Exit puppeth by using the Ctrl+C keys combination.
    
5- Initialize nodes 
    
    * ./geth init tnet.json --datadir node1
    * ./geth init tnet.json --datadir node2
   
  ![step 5](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/5.JPG)

6- Start up a mining thread/node (node1)
       
    * ./geth --datadir node1 --unlock "d1807e1e199ACB62d097ce19b62F0b4664c129F0" --mine --rpc --allow-insecure-unlock
    
    
   ![step 6](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/6.JPG) 
   
7- Start mining (node2)

   Open a new terminal and direct the correct folder.

    * ./geth --datadir node2 --unlock "49D4Cd480100E2D3bfa1D6f55cB493E799Aee339" --mine --port 30304 --bootnodes "enode://a7ef26e66e811fd4588112590c8fe562f11a39fdb39f06024a91a3e71127dd042350b7201ff25cb600acc37cb80c634e932a093ea31f118996107181317fbf1c@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock
 
## MyCrypto

1- MyCrypto & Click on "Add Custom Node", then add the custom network information.
   
   ![step 7](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/7.JPG)

2- Import the keystore file from the directory into MyCrypto.

   ![step 8](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/8.JPG) 

3- Make transaction
   
   ![step 9](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/9.JPG) 
   ![step 10](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/10.JPG)
   ![step 11](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/11.JPG)

4- Copy the hash and paste it into the "TX Status" section of the app, or click "TX Status".

    Hash : "0x4aa8e35ce6c194050b8ba68105a38d84f91429c90fb7328d468fbc4e59f1e2dd"
    
   ![step 12](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/12.JPG)
   ![step 13](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/13.JPG) 
