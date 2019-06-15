FROM komodocakeshop/dev-komodo-bins
RUN apt-get update && \
    apt-get -y install \
    dialog \
    jq && \
    apt-get -y clean; \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN ln -sf /linux64/komodod /usr/local/bin
RUN ln -sf /linux64/komodo-cli /usr/local/bin
RUN git clone https://github.com/komodo-cakeshop/komodo-in-a-box.git
CMD ["/bin/bash"]
