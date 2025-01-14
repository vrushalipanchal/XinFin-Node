
## How to Setup XinFin Masternode 

## Method 1 :- Setup XinFin Masternode One click Installer  ##

**Operating System**: 

* Apple Mac
* Windows 
* Linux - Ubuntu

###  Download [XinFin One Click Installer](https://xinfin.org/setup-masternode.php) (to setup Masternode) for Windows, Linux and mac OS ### 

---------------------------------

## Method 2 :- Setup XinFin Masternode Bootstrap Script  ##

Bootstrap Command XinFin Node Setup :- 

```
sudo su -c "bash <(wget -qO- https://raw.githubusercontent.com/XinFinOrg/XinFin-Node/master/bootstrap.sh)" root
```

Examples :- 
```
$ sudo su -c "bash <(wget -qO- https://raw.githubusercontent.com/XinFinOrg/XinFin-Node/master/bootstrap.sh)" root
[sudo] password for user: 
Please enter your XinFin MasterNode Name :- Demo_Server 
Your Masternode Name is Demo_Server

```



---------------------------------

## Method 3 :- Setup XinFin Masternode Docker ##

**Operating System**: Ubuntu 20.04 64-bit or higher 

Should be facing internet directly with **public IP** & **without NAT**

**Tools**: Docker, Docker Compose(1.27.4+)

Setup (For Ubuntu 20.04 64-bit or higher Operating System) 

## Clone repository
```
git clone https://github.com/XinFinOrg/XinFin-Node.git
```

Enter `XinFin-Node` directory
```
cd XinFin-Node
```


## Step: 1 Install docker & docker-compose
    sudo ./install_docker.sh

## Step: 2 Update .env file with details
Create `.env` file by using the sample - `.env.example`

Enter either your company or product name in the INSTANCE_NAME field.

Enter your email address in CONTACT_DETAILS field.

```
cp env.example .env
nano .env
```

## Step: 3 Start your Node

**For Mainnet**

Run:
```
sudo docker-compose -f docker-services.yml up -d
```

You should be able to see your node listed on this page: [https://xinfin.network](https://XinFin.network/) Select Menu "Switch to TestNet" for TestNetwork and Select "Switch to LiveNet" to check LiveNetwork Stats. 

Your coinbase address can be found in xdcchain/coinbase.txt file.

To stop the node or if you encounter any issues use::
```
sudo docker-compose -f docker-services.yml down
```
Attach XDC Console:
```
sudo bash xdc-attach.sh
```


**For Testnet**

Run:
```
sudo docker-compose -f apothem-network.yml up -d
```

You should be able to see your node listed on this page: [https://apothem.network] Select "Switch to LiveNet" to check LiveNetwork Stats and Select "Switch to TestNet" for TestNetwork.

Your coinbase address can be found in xdcchain/coinbase.txt file.

To stop the node or if you encounter any issues use::
```
sudo docker-compose -f apothem-network.yml down
```

## Masternode Tools and Public Community Channel #

Community Forum update link: http://xinfin.net

Telegram Development Community: https://t.me/XinFinDevelopers

Slack Public Channel Invitation : https://launchpass.com/xinfin-public


**Troubleshooting**

Public discussions on the technical issues, post articles and request for Enhancements and Technical Contributions. 

[Slack Public Chat](https://launchpass.com/xinfin-public), 

[Telegram Chat](http://bit.do/Telegram-XinFinDev), 

[Forum](https://xinfin.net), 

[GitHub](https://github.com/XinFinorg)


