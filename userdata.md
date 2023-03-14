#!/bin/bash

sudo yum update -y
sudo amazon-linux-extras install nginx1 -y
sudo systemctl enable nginx
sudo systemctl start nginx
sudo cd /usr/share/nginx/html && sudo cp index.html index.html.sample
sudo echo "<h1>Hello World from $(hostname -f)</h1>" > /usr/share/nginx
