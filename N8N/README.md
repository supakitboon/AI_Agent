### How to set up Docker Desktop for n8n 
1.) Download Docker Desktop
2.) Go to image and terminal 
3.) Run command
'''
mkdir {folder_name} #to create a new folde for n8n project 
cd foldername
pwd #after you get path copy it to use in next command 
docker run -it --rm --name n8n -p 5678:5678 -v {folder_path}:/home/node/.n8n docker.n8n.io/n8nio/n8n
or 
docker volume create {volume_name}
docker run -it --rm --name n8n -p 5678:5678 -v {volume_name}:/home/node/.n8n docker.n8n.io/n8nio/n8n
'''
Note : you can read document about it via this link https://docs.n8n.io/hosting/installation/docker/
When we run all of this the n8n will be installed in our computer to the path that we set up

YOu might have a question why we need docker ? 


### How to set up Ngrok Desktop for n8n 
1.) Setup and installation 
2.) Select OS that you are using 
3.) Open terminal and run commands to install and setup 
'''
brew install ngrok
ngrok config add-authtoken #############################
'''
4.) Go to Deploy your app online & Click deploy your static domain
You would receive this 
ngrok http --url=pigeon-game-tiger.ngrok-free.app 80 # keep it we will use it in the next step 
5.) Click on domain an copy the link 

