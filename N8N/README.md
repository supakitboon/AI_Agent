### How to set up Docker Desktop for n8n 
1.) Download Docker Desktop
2.) Go to image and terminal 
3.) Run command
'''
mkdir {folder_name} #to create a new folde for n8n project 
or 
docker volume create {folder_name}
'''
4.) Run command
'''terminal
docker run -it --rm --name n8n -p 5678:5678 -v n8n_data:/home/node/.n8n docker.n8n.io/n8nio/n8n
'''

