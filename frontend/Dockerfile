FROM nginx:latest


COPY . /usr/share/nginx/html/

RUN rm -f /var/log/nginx/access.log /var/log/nginx/error.log

RUN  curl -L -O https://artifacts.elastic.co/downloads/beats/filebeat/filebeat-7.17.28-amd64.deb && \
        dpkg -i filebeat-7.17.28-amd64.deb 
     
COPY filebeat.yml /etc/filebeat/filebeat.yml
COPY entrypoint.sh /entrypoint.sh
RUN chmod go-w /etc/filebeat/filebeat.yml && chown root:root /etc/filebeat/filebeat.yml
RUN chmod +x /entrypoint.sh


EXPOSE 80

ENTRYPOINT [ "/entrypoint.sh" ]