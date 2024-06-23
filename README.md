# Chat-Application
ChatApplication 
Overview:
This project implements a multi-client and server application using C programming language and Docker containerization. The system allows multiple clients to connect to a server and exchange messages in real-time.
Key Features:
•	Multi-threading for handling multiple clients simultaneously
•	Real-time message broadcasting
•	User name identification for each client
•	Containerized deployment using Docker
Commands used for containerization:
•	docker build -t chat-server -f Dockerfile.server .
•	docker build -t chat-client -f Dockerfile.client .
•	docker network create chat-network
•	docker run -d --name chat-server --network chat-network -p 4444:4444 chat-server
•	docker run -it --name chat-client1 --network chat-network chat-client ./client chat-server 4444
•	docker tag chat-server realayub/chat-server:latest
•	docker tag chat-client realayub/chat-server:latest
•	docker push realayub/chat-server:latest
•	docker push realayub/chat-client:latest
•	docker pull realayub/chat-server:latest
•	docker pull realayub/chat-client:latest
•	./client 192.168.1.2 4444
•	docker stop chat-server
•	docker logs chat-server
•	docker logs chat-client
•	docker ps

