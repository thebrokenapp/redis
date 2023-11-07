Step1: Download Redis stack files from: https://redis.io/download/#redis-stack-downloads
Step2: For CentOS9: https://packages.redis.io/redis-stack/redis-stack-server-7.2.0-v6.rhel9.x86_64.tar.gz
Step3: wget https://packages.redis.io/redis-stack/redis-stack-server-7.2.0-v6.rhel9.x86_64.tar.gz
Step4: Extract the file: tar -xvf redis-stack-server-7.2.0-v6.rhel9.x86_64.tar.gz
Step5: Edit redis.conf files to add the module that we want to load:
  loadmodule /redis_installation/redis-modules/redis-stack-server-7.2.0-v6/lib/rejson.so
  loadmodule /redis_installation/redis-modules/redis-stack-server-7.2.0-v6/lib/redisearch.so
Step6: Start Redis
Step7: Observe the module loaded logs in the startup logs

