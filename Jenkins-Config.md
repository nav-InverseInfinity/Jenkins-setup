# Setup ssh credentials
#### Goto "Manage Jenkins" -> Manage Credentials
example as below for new user, you will not have anything setup yet.
![image](https://user-images.githubusercontent.com/98486154/160558997-23513637-f44d-41bf-9c6e-f3754b699e41.png)

#### click Jenkins --> Global Credentials under (system) --> Add Credentials --> "Kind" choose *SSH Username with private key*


![image](https://user-images.githubusercontent.com/98486154/160559406-ae187e50-a0db-4c91-8c3c-a5afdecb7e44.png)
#### Under username, give the server's username (which you would want to connect with) ex - ec2-user for aws instance and paste the ssh private key of that server.
#### If you have any Passphrase, enter it down, then on ID field you can give a name for identification.

![image](https://user-images.githubusercontent.com/98486154/160560359-30d3a797-723b-448f-82b7-2aee3c021088.png)

# Creating Secret Text

### useful case scenario is passing a passowrds as a varibale secretly in jenkins pipeline. 
#### click Jenkins --> Global Credentials under (system) --> Add Credentials --> "Kind" choose *Secret text*
![image](https://user-images.githubusercontent.com/98486154/160560951-7664e7f9-5a75-489f-ad45-83bfa2d1ec6c.png)

#### under secret type in the password and ID for your identification 

example - Docker password as Secret text which can be used a varibale secretly in jenkins pipeline. 
![image](https://user-images.githubusercontent.com/98486154/160561222-43b8bcbd-3e05-4c3d-8c7f-5ca02ec40bdd.png)

