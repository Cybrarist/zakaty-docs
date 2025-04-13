# Linux / MAC / Windows Installation

## Requirements

- [Portainer](https://hub.docker.com/r/portainer/portainer-ce)
- [Docker](https://www.docker.com/)

## How To Install

### Method 1: Pull the image directly
you can pull the image directly in portainer

![Portainer add image](/public/images/portainer_add.png)

then you need to map the port

![Portainer add image](/public/images/portainer_port.png)

After that you can fill the environments with the values needed.

::: warning
Please refer to [Environments](/installation/environments) to get a list of available options.
:::

Finally, you can deploy and it should be running on port 8080 (per image)

### Method2: Use Docker Compose To Build Stack

Go to [Github](https://github.com/Cybrarist/Zakaty) and check [docker-compose](https://github.com/Cybrarist/Zakaty/blob/master/docker-compose.yaml) file.

Copy the content of docker-compose file

::: warning
you need to add the image name, and you can remove the volumes if not required.
:::

the updated docker compose file should look like the following
```yaml
services:
  zakaty:
    image: cybrarist/zakaty:latest
    #    build:
    #      context: .
    ports:
      - 8080:80
    environment:
      DB_CONNECTION: sqlite
      # DB_HOST=127.0.0.1
      # DB_PORT=3306
      # DB_DATABASE=zakah
      # DB_USERNAME=root
      # DB_PASSWORD=
      APP_TIMEZONE: Asia/Dubai
      APP_URL: "http://localhost:8080"
      ASSET_URL: "http://localhost:8080"
      MAIL_MAILER: smtp
      MAIL_HOST: smtp.gmail.com
      MAIL_PORT: 465
      MAIL_USERNAME: "email@gmail.com"
      MAIL_PASSWORD: "app password"
      MAIL_ENCRYPTION: tls
      MAIL_FROM_ADDRESS: "email@gmail.com"
      EXCHANGE_RATE_API_KEY: ""
      PRECIOUS_METAL_PRICE_API_KEY: ""


```

Choose "Web Editor" option and paste the content of the file

![Available Options](/public/images/web-editor.png)
![Available Options](/public/images/web-editor.png)

Change the values of the environment variable to anything you want.

::: warning
Please refer to [Environments](/installation/environments) to get a list of available options.
:::

Deploy the Stack.

Go To "Containers" and you should be able to find the following

![Available Options](/public/images/containers.png)

::: warning
you won't see mysql image if you choose sqlite
:::