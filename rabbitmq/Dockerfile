FROM rabbitmq:3.6-management

RUN  apt-get update \
	&& apt-get install -y wget \
	&& rm -rf /var/lib/apt/lists/*

RUN cd /usr/lib/rabbitmq/lib/rabbitmq_server-$RABBITMQ_VERSION/plugins/ \
	&& wget --quiet https://www.rabbitmq.com/community-plugins/v3.6.x/rabbitmq_auth_backend_ip_range-0.2.0.ez \
	&& rabbitmq-plugins enable --offline rabbitmq_auth_backend_ip_range
