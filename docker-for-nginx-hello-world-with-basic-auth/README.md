1. Generate .htpasswd with your desired username and password using let's say apache2-utils as passowrd generator utility.
# sudo htpasswd -c .htpasswd <user-name>
When prompted provide the password.

2. Build the docker image
sudo docker build -t nginx-hello-world-with-basic-auth .

3. Run the image
sudo docker run -p 8080:80 -d nginx-hello-world-with-basic-auth

4. Test it
curl -u <user:pwd> localhost:8080/HelloWorld.html 
