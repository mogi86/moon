# moon
python3, docker, 機械学習用

## Docker set up

```
$ cd /path/to/moon/
$ docker-compose build
$ docker-compose up -d
```

## Provisioning

### exce rovisioning

- ローカル

```
$ cd /path/to/moon/
$ ansible-playbook -i ansible/inventories/local site.yml
```

- AWS
prod環境のため、git上のホスト名はマスキングしている。

```
$ cd /path/to/moon/
$ ansible-playbook -i ansible/inventories/prod prod.yml
```

### docker exec web container

```
$ cd /path/to/moon/
$ docker exec -it moon_web /bin/bash --login
```
