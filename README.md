# tech-challenge
This repository contains the files required to execute a docker container that calls a ThousandEyes API.

To execute this project:

1)	Install on your Linux machine Docker version 20.10.24, build 297e128.

2)	Clone the Git repository to your working directory.

3)	Add your email address and ThousandEyes authToken to the config.py file located in the directory te_api_display/te_api_app/:
```
api_users_keys = {
'user_1':{'email':'<your-mail>','authToken':'<your-TE-authToken>'},
'user_2':{'email':'<your-mail>','authToken':'<your-TE-authToken>'}
}
NOTE: You can add as many users as you want.
```
4)	To build the Docker container run the following command in the directory te_api_display where the Dockerfile is located:
```docker build . -t te-api-display-v1.0```

5)	To run the container run the command:
```docker run -it -d --restart unless-stopped -p 8000:8000 te-api-display-v1.0```

6)	Very that the container is running with the command:
```docker ps```
