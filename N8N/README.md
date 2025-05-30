### How to set up Docker Desktop for n8n 
1.) Download Docker Desktop

2.) Go to the Image and terminal 

3.) Run the command ( Choose only one ) 
```
mkdir {folder_name} #to create a new folde for n8n project 
cd foldername
pwd #after you get the path, copy it to use in the next command 
docker run -it --rm --name n8n -p 5678:5678 -v {folder_path}:/home/node/.n8n docker.n8n.io/n8nio/n8n
or 
docker volume create {volume_name}
docker run -it --rm --name n8n -p 5678:5678 -v {volume_name}:/home/node/.n8n docker.n8n.io/n8nio/n8n
```

Note: you can read the document about it via this link https://docs.n8n.io/hosting/installation/docker/
When we run all of this, the n8n will be installed on our computer in the path that we set up

You might have a question about why we need Docker. 


### How to set up Ngrok for n8n 
1.) Setup and installation 

2.) Select the OS that you are using 

3.) Open the terminal and run commands to install and set up 
```
brew install ngrok
ngrok config add-authtoken #############################
```
4.) Go to Deploy your app online & click Deploy your static domain
You would receive this 
```
ngrok http-- url=pigeon-game-tiger.ngrok-free.app 80 # keep it, we will use it in the next step
```
5.) Click on the domain and copy the link 



