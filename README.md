# Telegram Bot using N8N 
A simple Telegram bot built using N8N and deployed locally using Docker and Ngrok

## N8N Workflow
<img width="1117" height="341" alt="image" src="https://github.com/user-attachments/assets/f4bc2458-a585-422e-bf1b-47712f55ea04" />

## Steps Involved
1. Create a Telegram Bot using BotFather in Telegram
2. Create an account in Ngrok
3. In Ngrok, in Setup and Installation, under Deploy your app online, select Static Domain to create a static url
   <img width="1195" height="375" alt="image" src="https://github.com/user-attachments/assets/e10bce82-1fb0-48ef-9b7f-590bdce06d70" />

4. Create a .env file replacing `DOMAIN_NAME` and `SUBDOMAIN` with the domain and sub-domain obtained from Ngrok (in step 3)
5. Go to a folder (n8n-project) where you want to store project files. Within that folder, create another folder called `local-files`
6. In the main folder, create a compose.yml file with the configuration from 3rd link in reference
7. Start Docker Compose using `docker compose up -d`
8. Start Ngrok server using Docker with the command from Ngrok site `docker run --net=host -it -e NGROK_AUTHTOKEN=<AUTH-TOKEN> ngrok/ngrok:latest http --url=your-url.ngrok-free.app 5678`
9. Open the Ngrok website in browser `your-url.ngrok-free.app`
10. Start new workflow
11. Add Telegram trigger. Use the credentials obtained from step 1
12. Add OpenAI message a model step
13. Add Telegram Send a Text Message step
14. Make the workflow active

 



## References
1. https://www.youtube.com/watch?v=azNX3bu0pwE
2. https://www.youtube.com/watch?v=_nMkQaguy3E
3. https://docs.n8n.io/hosting/installation/server-setups/docker-compose
