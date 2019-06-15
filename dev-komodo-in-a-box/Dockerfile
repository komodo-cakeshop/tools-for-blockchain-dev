FROM komodocakeshop/dev-komodo-bins:0.4.0a
RUN apt-get update && \
    apt-get -y install \
    dialog \
    jq && \
    apt-get -y clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN git clone https://github.com/komodo-cakeshop/komodo-in-a-box.git
CMD ["/bin/bash"]
