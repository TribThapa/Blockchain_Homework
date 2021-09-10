# Proof of Authority Development Chain

The Proof of Authority (PoA) algorithm is typically used for private blockchain networks as it requires pre-approval of, or voting in of, the account addresses that can approve transactions (seal blocks).  

  <p align="center">
   	<img src="/POA_DevelopmentChain/POA_Images/BTC.gif" width="700" height="300">
  </p>


## Creating Nodes

1- Generate two new nodes with new account addresses that will serve as our pre-approved sealer addresses

    * ./geth --datadir node1 account new 
    * ./geth --datadir node2 account new

![step 1](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/1.JPG)


2- Save passwords & Account addresses for use later
 
Node 1: Public address of the key:   d1807e1e199ACB62d097ce19b62F0b4664c129F0
Node 2: Public address of the key:   49D4Cd480100E2D3bfa1D6f55cB493E799Aee339

    * echo 'node1' > node1/password.txt
    * echo 'node2' > node2/password.txt
    * echo 'd1807e1e199ACB62d097ce19b62F0b4664c129F0' >> accounts.txt
    * echo '49D4Cd480100E2D3bfa1D6f55cB493E799Aee339' >> accounts.txt

3- To generate genesis block, first run puppeth

    * ./puppeth
     
   Network name: tnet
   
   Blocktime: 15 (Default 15)
   
   Network ID : 789
   
   ![step 2](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/2.JPG)
   ![step 3](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/3.JPG)
   ![step 4](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/4.JPG)
   
    * Exit puppeth by using the Ctrl+C keys combination.
    

5- Initialize the nodes with the genesis' json file
    
    * ./geth --datadir node1 init tnet.json 
    * ./geth --datadir node2 init tnet.json
   
  ![step 5](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/5.JPG)


6- Now the nodes can be used to begin mining blocks (node 1).
       
    * ./geth --datadir node1 --unlock "d1807e1e199ACB62d097ce19b62F0b4664c129F0" --mine --rpc --allow-insecure-unlock
    
    
   ![step 6](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/6.JPG) 
   

7- Start mining node2

   Open a new terminal and direct the correct folder.

    * ./geth --datadir node2 --unlock "49D4Cd480100E2D3bfa1D6f55cB493E799Aee339" --mine --port 30304 --bootnodes "enode://a7ef26e66e811fd4588112590c8fe562f11a39fdb39f06024a91a3e71127dd042350b7201ff25cb600acc37cb80c634e932a093ea31f118996107181317fbf1c@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

   ![step 7](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/7.JPG)


<p>&nbsp;</p>
<p>&nbsp;</p>

## MyCrypto

1- Open the MyCrypto app, then click `Change Network` at the bottom left. Click "Add Custom Node", then add the custom network information that you set in the genesis
   
    
![step 8](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/8.JPG) 


2- Import the keystore file from the directory into MyCrypto.

   ![step 9](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/9.JPG) 
   ![step 10](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/10.JPG)
   
3- Send money between accounts

   ![step 11](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/11.JPG)


4- Copy the hash and paste it into the "TX Status" section of the app, or click "TX Status".

    Hash : "0x66c24405d81bd0ceb0894ba5ed057ce590e6c2e46567c475fb148c21667200cc"
    
   ![step 12](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/12.JPG)
   ![step 13](https://github.com/TribThapa/Blockchain_Homework/blob/main/POA_DevelopmentChain/POA_Images/13.JPG) 
