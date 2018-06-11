# moon
python3, docker, 機械学習用

## Docker set up

```
$ cd /path/to/moon/
$ docker-compose build
$ docker-compose up -d
```

## Provisioning

- {environment}には対象環境名(localなど)を入れる

### exce rovisioning

```
$ cd /path/to/moon/
$ ansible-playbook -i ansible/inventories/{environment} site.yml
```

### docker exec web container

```
$ cd /path/to/moon/
$ docker exec -it moon_web /bin/bash --login
```
