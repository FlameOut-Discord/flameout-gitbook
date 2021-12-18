# Page 1

{% swagger method="get" path="/user/{id}/?token={token}" baseUrl="https://api.flameout.gq/api" summary="Профиль пользователя" %}
{% swagger-description %}
Получение профиля пользователя из БД
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="String" required="true" %}
Идентификатор пользователя из Discord
{% endswagger-parameter %}

{% swagger-parameter in="path" name="token" type="String" required="true" %}
Специальный токен
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Успешно" %}
```javascript
{
  "id": "747431086816100402",
  "xp": 27499,
  "coins": 50000,
  "hidden": true,
  "lvl": 50,
  "gifts": 0,
  "developer": false,
  "fish": 0,
  "wood": 0,
  "bankcoins": 0,
  "stoneresource": 0,
  "coalresource": 0,
  "ironresource": 0,
  "goldresource": 0,
  "diamondresource": 0,
  "netheriteresource": 0,
  "donaterubles": 0,
  "premium": true,
  "bitcoin": 0,
  "username": "FlameOut#2563",
  "event": false,
  "boxes": 0,
  "snus": 0,
  "snakescore": 0,
  "votes": 0,
  "badge_translator": false,
  "badge_donater": false,
  "scam": true,
  "badge_OLD": true,
  "badge_bughunter": false,
  "pension_month": 0,
  "ban": false, 
  "redstoneresource": 0,
  "lapisresource": 0,
  "copperresource": 0,
  "emeraldresource": 0,
  "quartzresource": 0,
  "background": 0,
  "badgeBirthday": true,
  "leafs": 0,
  "registrationdate": 1598281500,
  "pickaxelevel": 0,
  "stocks": 0,
  "badgeVoter": false,
  "titaniumresource": 0,
  "hiddeninleaders": true,
  "axelevel": 0,
  "badge_newyear2022": false,
  "reputation": 3,
  "timestampofreputation": 0,
  "bankcard": "0"
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Не указан идентификатор пользователя" %}
```javascript
{
  "message": "User id not found",
  "error": 403
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Идентификатор пользователя не является числом" %}
```javascript
{
    "message": "User id must be a number",
  "error": 403
}
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="Пользователь не найден" %}
```javascript
{
  "message": "User not found",
  "error": 404
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Неверный токен" %}
```javascript
{
  "message": "Incorrect token",
  "error": 403
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Не указан токен" %}
```javascript
{
  "message": "Token not defended",
  "error": 403
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/server/{id}/?token={token}" baseUrl="https://api.flameout.gq/api" summary="Профиль сервера" %}
{% swagger-description %}
Получение профиля сервера из БД
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="String" required="true" %}
Идентификатор сервера из Discord
{% endswagger-parameter %}

{% swagger-parameter in="path" name="token" type="String" required="true" %}
Специальный токен
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Успешно" %}
```javascript
{
  "id": "457858774099689479",
  "name": "Server of Nubovik :: FlameOut Support",
  "lang": "ru",
  "prefix": "f!",
  "levelupmessages": true
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Не указан идентификатор сервера" %}
```javascript
{
  "message": "Server id not found",
  "error": 403
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Идентификатор сервера не является числом" %}
```javascript
{
  "message": "Server id must be a number",
  "error": 403
}
```
{% endswagger-response %}

{% swagger-response status="404: Not Found" description="Сервер не найден" %}
```javascript
{
  "message": "Server not found",
  "error": 404
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Неверный токен" %}
```javascript
{
  "message": "Incorrect token",
  "error": 403
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Не указан токен" %}
```javascript
{
  "message": "Token not found",
  "error": 403
}
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/bot/stats/?token={token}" baseUrl="https://api.flameout.gq/api" summary="Получение статистики бота" %}
{% swagger-description %}
Получение статистика бота из кэша и БД. Вкратце: получение количества серверов и пользователей из БД, количества эмодзи и каналов из кэша, время ответа БД и количество использований команд (т.е. сколько раз командами бота воспользовались). 
{% endswagger-description %}

{% swagger-parameter in="path" name="token" type="String" required="true" %}
Специальный токен
{% endswagger-parameter %}

{% swagger-response status="403: Forbidden" description="Неверный токен" %}
```javascript
{
  "message": "Incorrect token",
  "error": 403
}
```
{% endswagger-response %}

{% swagger-response status="403: Forbidden" description="Не указан токен" %}
```javascript
{
  "message": "Token not found",
  "error": 403
}
```
{% endswagger-response %}
{% endswagger %}
