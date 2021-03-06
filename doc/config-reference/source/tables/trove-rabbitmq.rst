..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _trove-rabbitmq:

.. list-table:: Description of RabbitMQ configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[oslo_messaging_rabbit]**
     -
   * - ``amqp_auto_delete`` = ``False``
     - (Boolean) Auto-delete queues in AMQP.
   * - ``amqp_durable_queues`` = ``False``
     - (Boolean) Use durable queues in AMQP.
   * - ``channel_max`` = ``None``
     - (Integer) Maximum number of channels to allow
   * - ``default_notification_exchange`` = ``${control_exchange}_notification``
     - (String) Exchange name for for sending notifications
   * - ``default_notification_retry_attempts`` = ``-1``
     - (Integer) Reconnecting retry count in case of connectivity problem during sending notification, -1 means infinite retry.
   * - ``default_rpc_exchange`` = ``${control_exchange}_rpc``
     - (String) Exchange name for sending RPC messages
   * - ``default_rpc_retry_attempts`` = ``-1``
     - (Integer) Reconnecting retry count in case of connectivity problem during sending RPC message, -1 means infinite retry. If actual retry attempts in not 0 the rpc request could be processed more then one time
   * - ``fake_rabbit`` = ``False``
     - (Boolean) Deprecated, use rpc_backend=kombu+memory or rpc_backend=fake
   * - ``frame_max`` = ``None``
     - (Integer) The maximum byte size for an AMQP frame
   * - ``heartbeat_interval`` = ``1``
     - (Integer) How often to send heartbeats for consumer's connections
   * - ``heartbeat_rate`` = ``2``
     - (Integer) How often times during the heartbeat_timeout_threshold we check the heartbeat.
   * - ``heartbeat_timeout_threshold`` = ``60``
     - (Integer) Number of seconds after which the Rabbit broker is considered down if heartbeat's keep-alive fails (0 disable the heartbeat). EXPERIMENTAL
   * - ``host_connection_reconnect_delay`` = ``0.25``
     - (Floating point) Set delay for reconnection to some host which has connection error
   * - ``kombu_compression`` = ``None``
     - (String) EXPERIMENTAL: Possible values are: gzip, bz2. If not set compression will not be used. This option may notbe available in future versions.
   * - ``kombu_failover_strategy`` = ``round-robin``
     - (String) Determines how the next RabbitMQ node is chosen in case the one we are currently connected to becomes unavailable. Takes effect only if more than one RabbitMQ node is provided in config.
   * - ``kombu_missing_consumer_retry_timeout`` = ``60``
     - (Integer) How long to wait a missing client beforce abandoning to send it its replies. This value should not be longer than rpc_response_timeout.
   * - ``kombu_reconnect_delay`` = ``1.0``
     - (Floating point) How long to wait before reconnecting in response to an AMQP consumer cancel notification.
   * - ``kombu_ssl_ca_certs`` =
     - (String) SSL certification authority file (valid only if SSL enabled).
   * - ``kombu_ssl_certfile`` =
     - (String) SSL cert file (valid only if SSL enabled).
   * - ``kombu_ssl_keyfile`` =
     - (String) SSL key file (valid only if SSL enabled).
   * - ``kombu_ssl_version`` =
     - (String) SSL version to use (valid only if SSL enabled). Valid values are TLSv1 and SSLv23. SSLv2, SSLv3, TLSv1_1, and TLSv1_2 may be available on some distributions.
   * - ``notification_listener_prefetch_count`` = ``100``
     - (Integer) Max number of not acknowledged message which RabbitMQ can send to notification listener.
   * - ``notification_persistence`` = ``False``
     - (Boolean) Persist notification messages.
   * - ``notification_retry_delay`` = ``0.25``
     - (Floating point) Reconnecting retry delay in case of connectivity problem during sending notification message
   * - ``pool_max_overflow`` = ``0``
     - (Integer) Maximum number of connections to create above `pool_max_size`.
   * - ``pool_max_size`` = ``10``
     - (Integer) Maximum number of connections to keep queued.
   * - ``pool_recycle`` = ``600``
     - (Integer) Lifetime of a connection (since creation) in seconds or None for no recycling. Expired connections are closed on acquire.
   * - ``pool_stale`` = ``60``
     - (Integer) Threshold at which inactive (since release) connections are considered stale in seconds or None for no staleness. Stale connections are closed on acquire.
   * - ``pool_timeout`` = ``30``
     - (Integer) Default number of seconds to wait for a connections to available
   * - ``rabbit_ha_queues`` = ``False``
     - (Boolean) Try to use HA queues in RabbitMQ (x-ha-policy: all). If you change this option, you must wipe the RabbitMQ database. In RabbitMQ 3.0, queue mirroring is no longer controlled by the x-ha-policy argument when declaring a queue. If you just want to make sure that all queues (except those with auto-generated names) are mirrored across all nodes, run: "rabbitmqctl set_policy HA '^(?!amq\.).*' '{"ha-mode": "all"}' "
   * - ``rabbit_host`` = ``localhost``
     - (String) The RabbitMQ broker address where a single node is used.
   * - ``rabbit_hosts`` = ``$rabbit_host:$rabbit_port``
     - (List) RabbitMQ HA cluster host:port pairs.
   * - ``rabbit_interval_max`` = ``30``
     - (Integer) Maximum interval of RabbitMQ connection retries. Default is 30 seconds.
   * - ``rabbit_login_method`` = ``AMQPLAIN``
     - (String) The RabbitMQ login method.
   * - ``rabbit_max_retries`` = ``0``
     - (Integer) Maximum number of RabbitMQ connection retries. Default is 0 (infinite retry count).
   * - ``rabbit_password`` = ``guest``
     - (String) The RabbitMQ password.
   * - ``rabbit_port`` = ``5672``
     - (Unknown) The RabbitMQ broker port where a single node is used.
   * - ``rabbit_qos_prefetch_count`` = ``0``
     - (Integer) Specifies the number of messages to prefetch. Setting to zero allows unlimited messages.
   * - ``rabbit_retry_backoff`` = ``2``
     - (Integer) How long to backoff for between retries when connecting to RabbitMQ.
   * - ``rabbit_retry_interval`` = ``1``
     - (Integer) How frequently to retry connecting with RabbitMQ.
   * - ``rabbit_transient_queues_ttl`` = ``1800``
     - (Integer) Positive integer representing duration in seconds for queue TTL (x-expires). Queues which are unused for the duration of the TTL are automatically deleted. The parameter affects only reply and fanout queues.
   * - ``rabbit_use_ssl`` = ``False``
     - (Boolean) Connect over SSL for RabbitMQ.
   * - ``rabbit_userid`` = ``guest``
     - (String) The RabbitMQ userid.
   * - ``rabbit_virtual_host`` = ``/``
     - (String) The RabbitMQ virtual host.
   * - ``rpc_listener_prefetch_count`` = ``100``
     - (Integer) Max number of not acknowledged message which RabbitMQ can send to rpc listener.
   * - ``rpc_queue_expiration`` = ``60``
     - (Integer) Time to live for rpc queues without consumers in seconds.
   * - ``rpc_reply_exchange`` = ``${control_exchange}_rpc_reply``
     - (String) Exchange name for receiving RPC replies
   * - ``rpc_reply_listener_prefetch_count`` = ``100``
     - (Integer) Max number of not acknowledged message which RabbitMQ can send to rpc reply listener.
   * - ``rpc_reply_retry_attempts`` = ``-1``
     - (Integer) Reconnecting retry count in case of connectivity problem during sending reply. -1 means infinite retry during rpc_timeout
   * - ``rpc_reply_retry_delay`` = ``0.25``
     - (Floating point) Reconnecting retry delay in case of connectivity problem during sending reply.
   * - ``rpc_retry_delay`` = ``0.25``
     - (Floating point) Reconnecting retry delay in case of connectivity problem during sending RPC message
   * - ``socket_timeout`` = ``0.25``
     - (Floating point) Set socket timeout in seconds for connection's socket
   * - ``ssl`` = ``None``
     - (Boolean) Enable SSL
   * - ``ssl_options`` = ``None``
     - (Dict) Arguments passed to ssl.wrap_socket
   * - ``tcp_user_timeout`` = ``0.25``
     - (Floating point) Set TCP_USER_TIMEOUT in seconds for connection's socket
