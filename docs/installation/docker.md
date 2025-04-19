# Linux / MAC / Windows Installation

## Requirements

- [Docker](https://www.docker.com/)
- Free key from [Exchange Rate](https://www.exchangerate-api.com/)
- Free key from [Gold API](https://goldapi.io)

## How To Install
    
pull the image you want from docker repository [Zakaty](https://hub.docker.com/r/cybrarist/zakaty)

```
docker pull image_name
```

run the image with the env variables that are needed

```shell
docker run -d \
  -p 8080:80 \
  -v ./database:/app/database/sqlite \
  -e DB_CONNECTION=sqlite \
  -e EXCHANGE_RATE_API_KEY="" \
  -e PRECIOUS_METAL_PRICE_API_KEY="" \
  -e APP_TIMEZONE=UTC \
  -e APP_URL="http://localhost:8080" \
  -e ASSET_URL="http://localhost:8080" \
  cybrarist/zakaty:latest
```
::: warning
Please refer to [Environments](/installation/environments) to get a list of available options.
:::