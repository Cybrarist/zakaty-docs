# Environments

## List of available environments and possible values.

## DB_CONNECTION
By Default the value is `sqlite` if you are planning to use `MySQL` then you need to pass the following
```dotenv
DB_CONNECTION=mysql
DB_HOST=host
DB_PORT=3306
DB_DATABASE=database
DB_USERNAME=username
DB_PASSWORD=password
```

# Notifications

## Email
you need an email setup (you can use google app passwords)

```dotenv
MAIL_MAILER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=465
MAIL_USERNAME="email@gmail.com"
MAIL_PASSWORD="app password"
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS="email@gmail.com"

```

## App and Asset url
you need to update those depending on your configuration and how the app is accessed
```dotenv
APP_URL="http://localhost:8080"
ASSET_URL="http://localhost:8080"
```

[//]: # (## Change the theme color)

[//]: # (by default it's `Stone`)

[//]: # (```dotenv)

[//]: # (THEME_COLOR="Stone")

[//]: # (```)

[//]: # (but here's a list of all available colors)

[//]: # ()
[//]: # (| {#remove_header} |        |        |         | )

[//]: # (|------------------|:------:|:------:|:-------:|)

[//]: # (| Slate            |  Gray  |  Zinc  | Neutral |)

[//]: # (| Stone            |  Red   | Orange |  Amber  |)

[//]: # (| Yellow           |  Lime  | Green  | Emerald |)

[//]: # (| Teal             |  Cyan  |  Sky   |  Blue   |)

[//]: # (| Indigo           | Violet | Purple | Fuchsia |)

[//]: # (| Pink             |  Rose  |        |         |)
