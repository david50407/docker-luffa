Docker-Luffa
=====

Dockerize [Luffa](https://github.com/rschiang/luffa) that aimed to provide integration between multiple Slack domains.

Usage
=====

To run it:

```
$ docker run -d -p 80:80 -v /var/luffa.config.json:/config.json:ro david50407/luffa
```

Remember to provide your luffa config as data volume to let container read.

Usage-Compose
=====

docker-compose.yml:

```
luffa:
  image: david50407/luffa
  volumes:
    - "/var/luffa.config.json:/config.json:ro"
```

License
-------
Copyright (C) Davy <me@davy.tw> 2015, under MIT License.
