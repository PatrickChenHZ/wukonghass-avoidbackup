FROM wzpan/wukong-robot-arm:latest
MAINTAINER wzpan
ENV LANG C.UTF-8
WORKDIR /root/wukong-robot
RUN git pull -f
RUN pip3 install -r requirements.txt
WORKDIR /root/.wukong/contrib
RUN git pull -f
RUN pip3 install -r requirements.txt
WORKDIR /root/wukong-robot
EXPOSE 5000
COPY run.sh /
COPY config.yml /.wukong

RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
