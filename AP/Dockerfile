FROM ubuntu

RUN apt update
RUN apt install  -y git
RUN dpkg -l git

# この時点でdirが作成される
WORKDIR /work

RUN git clone https://github.com/iii-source/ci_heroku_cooperation.git /work

RUN pwd > ap.log
RUN ls >> ap.log

RUN sh install.sh

ENV PYTHONPATH /work/server
ENV PYTHONPATH $PYTHONPATH:/work
RUN echo $PYTHONPATH

RUN echo hi Comment ctermfg=DarkGreen >> ~/.vimrc

# TODO
# RUN python3 server/app.py & python3 -m pytest


