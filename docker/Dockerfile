FROM phusion/baseimage:0.9.21
LABEL maintainer "chevdor@gmail.com"

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y erlang libncurses5-dev libssl-dev unixodbc-dev g++ git erlang-base-hipe wget rebar && \
	git clone https://github.com/aeternity/testnet.git && \
	cd testnet && \
	sh install.sh

EXPOSE 8040, 8041

WORKDIR /testnet
CMD ["/bin/sh", "start.sh"]