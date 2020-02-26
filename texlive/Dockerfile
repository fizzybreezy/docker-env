FROM debian:stretch-slim

RUN apt-get update -q && apt-get install -qy wget git make gnuplot && \ 
    apt-get --purge remove -y .\*-doc$ && \
    apt-get clean -y && \
    apt-get autoremove && \
    rm -rf /var/lib/apt/lists/* 

RUN wget http://mirror.ctan.org/systems/texlive/tlnet/install-tl-unx.tar.gz; \
	mkdir /install-tl-unx; \
	tar -xf install-tl-unx.tar.gz -C /install-tl-unx --strip-components=1; \
    echo "selected_scheme scheme-full" >> /install-tl-unx/texlive.profile; \
    echo "tlpdbopt_install_srcfiles 0" >> /install-tl/texlive.profile && \
    echo "tlpdbopt_install_docfiles 0" >> /install-tl/texlive.profile && \
	/install-tl-unx/install-tl -profile /install-tl-unx/texlive.profile; \
    rm -r /install-tl-unx; \
	rm install-tl-unx.tar.gz

ENV PATH="/usr/local/texlive/2019/bin/x86_64-linux:${PATH}"
