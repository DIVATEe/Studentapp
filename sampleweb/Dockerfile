FROM ubuntu:latest 

LABEL dev="anup"  

RUN apt-get update && \
    apt-get install nginx unzip -y  && \
    rm /var/www/html/index.html 

ADD https://templatemo.com/download/templatemo_562_space_dynamic   /var/www/html/templatemo_562_space_dynamic.zip 

WORKDIR /var/www/html  

RUN unzip templatemo_562_space_dynamic.zip && \
    mv templatemo_562_space_dynamic/* /var/www/html/


EXPOSE 80 


CMD ["nginx", "-g", "daemon off;"]