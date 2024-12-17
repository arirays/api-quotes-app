FROM ubuntu:latest

# Install MySQL client
RUN apt-get update && \
    DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-client bash && \
    apt-get clean

WORKDIR /opt

COPY mydatabase.sql /opt/
COPY import.sh /opt/

RUN chmod +x /opt/import.sh

CMD ["sh", "/opt/import.sh"]

