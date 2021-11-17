# Streamr
## Полезные команды

### Обновление ноды
```
docker stop streamr && docker rm streamr

docker pull streamr/broker-node:testnet

docker create --name streamr --restart=always -p 7170:7170 -p 7171:7171 -p 1883:1883 -v $(cd $HOME/.streamrDocker; pwd):/root/.streamr streamr/broker-node:testnet

docker start streamr

docker logs streamr -f --tail=50
```

### Посмотреть логи
```
docker restart streamr
```

### Проверить кошелек
```
streamr_wallet_info
```

### Официальный гайд
[Medium.com/streamrblog](https://medium.com/streamrblog/how-to-join-the-brubeck-testnet-c8b823c847f8)

