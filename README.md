<img src="https://i.ibb.co/h1dW0gW2/x.jpg">
 Hi, I’m Stardust-Community .
 I’m interested in Coding .
 I’m currently learning python , c , c++ , java .
 I’m looking to collaborate on nothing
 Reach me at telegram id : @kaoru_tono .
 Fun fact: i dont exiist .

FROM python:3.8-slim-buster

RUN apt update && apt upgrade -y
RUN apt install git -y
COPY requirements.txt /requirements.txt

RUN cd /
RUN pip3 install -U pip && pip3 install -U -r requirements.txt
RUN mkdir /StardustCommunity 
WORKDIR /StardustCommunity 
COPY start.sh /start.sh
CMD ["/bin/bash", "/start.sh"]
