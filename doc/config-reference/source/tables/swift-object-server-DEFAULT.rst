..
  Warning: Do not edit this file. It is automatically generated and your
  changes will be overwritten. The tool to do so lives in the
  openstack-doc-tools repository.

.. list-table:: Description of configuration options for ``[DEFAULT]`` in ``object-server.conf``
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - ``backlog`` = ``4096``
     - Maximum number of allowed pending TCP connections
   * - ``bind_ip`` = ``0.0.0.0``
     - IP Address for server to bind to
   * - ``bind_port`` = ``6000``
     - Port for server to bind to
   * - ``bind_timeout`` = ``30``
     - Seconds to attempt bind before giving up
   * - ``client_timeout`` = ``60``
     - Timeout to read one chunk from a client external services
   * - ``conn_timeout`` = ``0.5``
     - Connection timeout to external services
   * - ``container_update_timeout`` = ``1.0``
     - Time to wait while sending a container update on object update. object server. For most cases, this should be
   * - ``devices`` = ``/srv/node``
     - Parent directory of where devices are mounted
   * - ``disable_fallocate`` = ``false``
     - Disable "fast fail" fallocate checks if the underlying filesystem does not support it.
   * - ``disk_chunk_size`` = ``65536``
     - Size of chunks to read/write to disk
   * - ``eventlet_debug`` = ``false``
     - If true, turn on debug logging for eventlet
   * - ``expiring_objects_account_name`` = ``expiring_objects``
     - No help text available for this option.
   * - ``expiring_objects_container_divisor`` = ``86400``
     - No help text available for this option.
   * - ``fallocate_reserve`` = ``0``
     - You can set fallocate_reserve to the number of bytes you'd like fallocate to reserve, whether there is space for the given file size or not. This is useful for systems that behave badly when they completely run out of space; you can make the services pretend they're out of space early. server. For most cases, this should be
   * - ``log_address`` = ``/dev/log``
     - Location where syslog sends the logs to
   * - ``log_custom_handlers`` = `` ``
     - Comma-separated list of functions to call to setup custom log handlers.
   * - ``log_facility`` = ``LOG_LOCAL0``
     - Syslog log facility
   * - ``log_level`` = ``INFO``
     - Logging level
   * - ``log_max_line_length`` = ``0``
     - Caps the length of log lines to the value given; no limit if set to 0, the default.
   * - ``log_name`` = ``swift``
     - Label used when logging
   * - ``log_statsd_default_sample_rate`` = ``1.0``
     - Defines the probability of sending a sample for any given event or timing measurement.
   * - ``log_statsd_host`` = ``localhost``
     - If not set, the StatsD feature is disabled.
   * - ``log_statsd_metric_prefix`` = `` ``
     - Value will be prepended to every metric sent to the StatsD server.
   * - ``log_statsd_port`` = ``8125``
     - Port value for the StatsD server.
   * - ``log_statsd_sample_rate_factor`` = ``1.0``
     - Not recommended to set this to a value less than 1.0, if frequency of logging is too high, tune the log_statsd_default_sample_rate instead.
   * - ``log_udp_host`` = `` ``
     - If not set, the UDP receiver for syslog is disabled.
   * - ``log_udp_port`` = ``514``
     - Port value for UDP receiver, if enabled.
   * - ``max_clients`` = ``1024``
     - Maximum number of clients one worker can process simultaneously Lowering the number of clients handled per worker, and raising the number of workers can lessen the impact that a CPU intensive, or blocking, request can have on other requests served by the same worker. If the maximum number of clients is set to one, then a given worker will not perform another call while processing, allowing other workers a chance to process it.
   * - ``mount_check`` = ``true``
     - Whether or not check if the devices are mounted to prevent accidentally writing to the root device
   * - ``network_chunk_size`` = ``65536``
     - Size of chunks to read/write over the network
   * - ``node_timeout`` = ``3``
     - Request timeout to external services
   * - ``servers_per_port`` = ``0``
     - If each disk in each storage policy ring has unique port numbers for its "ip" value, you can use this setting to have each object-server worker only service requests for the single disk matching the port in the ring. The value of this setting determines how many worker processes run for each port (disk) in the
   * - ``swift_dir`` = ``/etc/swift``
     - Swift configuration directory
   * - ``user`` = ``swift``
     - User to run as
   * - ``workers`` = ``auto``
     - a much higher value, one can reduce the impact of slow file system operations in one request from negatively impacting other requests.
