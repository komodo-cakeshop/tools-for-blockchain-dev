FROM ubuntu:18.04
RUN apt-get update && \
    apt-get install -y wget
RUN wget https://raw.githubusercontent.com/KomodoPlatform/komodo/master/zcutil/fetch-params.sh
RUN mkdir $HOME/.zcash-params
RUN chmod +x fetch-params.sh
RUN ./fetch-params.sh
CMD ["/bin/bash"]
