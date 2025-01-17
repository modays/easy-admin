# easy-admin configure

```
settings:
  application:
    # dev test prod
    mode: dev
    # host IP ，default 0.0.0.0
    host: 0.0.0.0
    # application name
    name: easy-admin
    # application port
    port: 8000 
    readtimeout: 1
    writertimeout: 2
    # enable dp 
    enabledp: false
    # timezone 
    timezone: "Africa/Cairo"
    # local
    local: "en"
  ssl:
    # https domain
    domain: localhost:8000
    # https enable
    enable: false
    # ssl key
    key: keystring
    # ssl pem path
    pem: temp/pem.pem
  logger:
    # log save path
    path: temp/logs
    # file / default
    stdout: ''
    # trace, debug, info, warn, error, fatal
    level: trace
    # enable db log
    enableddb: false
  jwt:
    # token secret
    secret: easy-admin
    # token timeout (S)
    timeout: 3600
  database:
    # mysql，sqlite3， postgres
    driver: mysql
    source: user:password@tcp(127.0.0.1:3306)/dbname?charset=utf8&parseTime=True&loc=Local&timeout=1000ms
    # source: sqlite3.db
    # source: host=myhost port=myport user=gorm dbname=gorm password=mypassword
    registers:
      - sources:
          - user:password@tcp(127.0.0.1:3306)/dbname?charset=utf8&parseTime=True&loc=Local&timeout=1000ms
  gen:
    dbname: dbname
    frontpath: ../ui/src
  queue:
    memory:
      poolSize: 100
  extend: # ext config
    demo:
      name: data

```