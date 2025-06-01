Analyze ZSATray logs using a Dockerized Elasticsearch cluster
- Copy the ZSATray logs to logs/
  - macOS: `~/Library/Application\ Support/com.zscaler.Zscaler/`
- Launch the Elasticsearch / Kibana containers: `docker compose up`
- Manually launch logstash against the logs, see further work in docker compose logstash service command
- Log into Kibana at http://localhost:5601 with username elastic and password elastic
  - Create a Data view against the zstray index, note that @timestamp will be parsed from the log entries
