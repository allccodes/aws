#!/bin/bash

sudo su
yum update -y
amazon-linux-extras install nginx1 -y
systemctl enable nginx
systemctl start nginx
cd /usr/share/nginx/html && sudo index.html index.html.sample
echo "<h1>Hello World from $(hostname -f)</h1>" > /usr/share/nginx
