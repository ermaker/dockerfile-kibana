# Kibana

# Getting Started

```shell
docker run \
  -p 5601:5601 \
  ermaker/kibana
```

# Usage

```shell
CWD=$(pwd $(dirname $0))
CONF=${CWD}/kibana.conf.d

docker create \
  --name kibana \
  -p 5601:5601 \
  -v ${CONF}:/opt/kibana/config \
  --restart=on-failure:35 \
  ermaker/kibana
```
