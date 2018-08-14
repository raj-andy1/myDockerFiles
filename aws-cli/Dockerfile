FROM   ubuntu:xenial

RUN apt-get -y upgrade && apt-get -y update

RUN apt-get -y install curl python-pip vim jq \
&& pip install awscli --upgrade --user

RUN sed -i '$ a export PATH=~/.local/bin:$PATH' ~/.profile \
&& mkdir /root/.aws

COPY /credentials /accounts /config /root/.aws/

RUN curl https://raw.githubusercontent.com/coinbase/assume-role/master/install-assume-role -O \
&& bash ./install-assume-role