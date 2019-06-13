### Build Docker Image
docker build --tag=friendlyhello .

### List Docker Images
docker image ls

### Running Docker Image
docker run -p 4000:80 friendlyhello

### Testing the Container
You should see a message that Python is serving your app at http://0.0.0.0:80. But that message is coming from inside the container, which doesn’t know you mapped port 80 of that container to 4000, making the correct URL http://localhost:4000.

Go to that URL in a web browser to see the display content served up on a web pag

curl http://localhost:4000

### Connect to Continer in detached mode
docker run -d -p 4000:80 friendlyhello

### Stop Docker Container
docker container stop CONTAINERID