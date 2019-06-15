FROM komodocakeshop/dev-komodo-builders
RUN wget https://github.com/KomodoPlatform/komodo/releases/download/dev-multios-0.4.0a-alpha/linux_0.4.0a.gz
RUN tar zxvf linux_0.4.0a.gz
RUN ln -sf /linux64/komodod /usr/local/bin
RUN ln -sf /linux64/komodo-cli /usr/local/bin
CMD ["/bin/bash"]
