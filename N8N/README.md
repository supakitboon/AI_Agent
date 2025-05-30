## There are 2 ways to create a n8n project

1.)Use Docker + ngrok if you want…
- A zero-cost playground for personal or small-team automations.
- Full control over packages, custom code, and data residency.
- To integrate tightly with your local/dev environment or internal services.

2.)Use n8n Cloud if you need…
- A fully managed, always-on service with automatic SSL.
- Built-in team collaboration features and enterprise support.
- To avoid any DevOps overhead or maintenance work.

🗒️Note: If you choose the first option, please follow below


## Tutorial: set up n8n on local host 
Note: You don't have to do this if you use n8n.cloud

### Step 1: Set up Docker Desktop for n8n 
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

🗒️Note: you can read the document about it via this link [https://docs.n8n.io/hosting/installation/docker/]
When we run all of this, the n8n will be installed on our computer in the path that we set up

You might have a question about why we need Docker. 


**Step 2: Install and configure ngrok**
### Step 2: Set up Ngrok for n8n 

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

### Step 3: Run the image file on Docker
1.) Click the image on the left panel

2.) Run our image 

3.) Setup Optional Setting 
Fill in this info 
```
- Container name: Myn8n #any name 
- Ports: 5555#any number
- Volumes: Host path: path to your folder created in Step 1
- Container path: /home/node.n8n
N8N_COMMUNITY_PACKAGES_ALLOW_TOOL_USAGE Value: TRUE
Variable : N8N_EDITOR_BASE_URL Value : [NGROK_PUBLIC_URL]
Variable : WEBHOOK_URL Value : [NGROK_PUBLIC_URL]
Variable: N8N_DEFAULT_BINARY_DATA_MODE Value: filesystem
```

4.) After running the image, use the command from Step 2 and change the port to run on the terminal 
```
ngrok http-- url=pigeon-game-tiger.ngrok-free.app 5555#Change to your port number
```
Finally, you would receive a public URL. Create an account and access it to build your n8n project hehe.













