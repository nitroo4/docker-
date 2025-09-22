FROM nginx
MAINTAINER mickael
LABEL maintainer="mickael.razaka@example.com"

RUN apt-get update && \
    apt-get install -y nano iputils-ping && apt install -y iproute2 && \
    apt-get install -y nodejs 

RUN useradd -ms /bin/bash mickael
USER mickael
WORKDIR /home/mickael

VOLUME ["/home/mickael/data"]

EXPOSE 3000

CMD ["bash"]
