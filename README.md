# Tutorial: Deploy Minecraft with Oakestra

![](img/minecraft-full.png)

With this tutorial we'll be able to:
- 🎮 Play Minecraft from a browser, no client installation needed (thanks to [Zardoy](https://github.com/giobart/minecraft-web-client/tree/next)'s Prismarine based modified web client)
- 👭 Play multiplayer locally or remotely 
- 🖥️ Host your Minecraft server ([Openhack](https://github.com/noelbundick/minecraft-server)) and proxy. 
- ⚙️ Scale your server instances to handle more users
- 🛠️ Customize your deployment 

## 🤔 What are we going to do

![architecture](img/MinecraftArchitecture.jpg)

## ⚠️ Disclaimers ⛔️

This tutorial is not meant as a way to hack the game or play for without a license. This tutorial is a tech demo that uses already existing technologies and pieces of software to provide an example of how to use Oakestra with a toy use case. We do not take any responsibility for what the users will do with the proposed example. 

## Step 1 - 🌳 Create Your Oakestra Cluster

Get Oakestra up and running with at least one cluster and one worker node. 

Check out the official [Wiki](https://www.oakestra.io/docs/getting-started/welcome-to-oakestra-docs/)

## Step 2 - 🖼️ Access the Dashboard 

Open the Oakestra dashboard at 
http://< Root IP >

Login with your custom credentials or use the default: ID: `Admin`, Password: `Admin`

![login](img/login.png)

## Step 3 - 👾 Create the Minecraft app

![app](img/newapp.png)

## Step 4 - 📁 Upload the SLA

![sla](img/sla.png)

## Step 5 - 📲 Deploy All

![apps](img/dashboard.png)

## Step 6 - 🖥️ Monitor your deplyment

Find the IP address of the client from the service details of the oakestra dashbaord:

![monitor](img/ip-page.png)

## Step 7 - 💻 Reach your client! 

Then reach your client node IP address at port 8080.
```
http://<Client NodeIP>:8080
```

![monitor](img/menu.png)

## Step 8 - ⚙️ Setup the server proxy! 

Find the IP address of the proxy service from the service details of the oakestra dashbaord. Then in the server selection menu of the minecraft client, click "EDIT" on the pre-existing server and change the IP address to the proxy service IP address.

![monitor](img/edit-page.png)

![monitor](img/proxy-ip-page.png)

Replace only the IP address of the proxy. The server IP is a LoadBalancer Semantic IP of Oakestra. The Proxy will load balance the traffic across all the instances of the servers available.

## Step 9 - 🎮 Enjoy the game!

Save the server configuration, click the server and enjoy! 

![monitor](img/oak-gif.gif)



