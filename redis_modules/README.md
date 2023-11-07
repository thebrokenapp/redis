* Download Redis stack files from: https://redis.io/download/#redis-stack-downloads
* For CentOS9: https://packages.redis.io/redis-stack/redis-stack-server-7.2.0-v6.rhel9.x86_64.tar.gz
* wget https://packages.redis.io/redis-stack/redis-stack-server-7.2.0-v6.rhel9.x86_64.tar.gz
* Extract the file: tar -xvf redis-stack-server-7.2.0-v6.rhel9.x86_64.tar.gz
* Edit redis.conf files to add the module that we want to load:
  loadmodule /redis_installation/redis-modules/redis-stack-server-7.2.0-v6/lib/rejson.so
  loadmodule /redis_installation/redis-modules/redis-stack-server-7.2.0-v6/lib/redisearch.so
* Start Redis
* Observe the module loaded logs in the startup logs

