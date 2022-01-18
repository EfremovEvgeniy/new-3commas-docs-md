---
title: API title v0.0.1
language_tabs:
  - ruby: Ruby
language_clients:
  - ruby: ""
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2

---

<!-- Generator: Widdershins v4.0.1 -->

<h1 id="api-title">API title v0.0.1</h1>

> Scroll down for code samples, example requests and responses. Select a language for code samples from the tabs above or the mobile navigation menu.

Base URLs:

* <a href="//api.3commas.io/public/api">//api.3commas.io/public/api</a>

<h1 id="api-title-bots">bots</h1>

Operations about bots

## getVer1BotsAccountTradeInfoSmartSell

<a id="opIdgetVer1BotsAccountTradeInfoSmartSell"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/bots/account_trade_info_smart_sell',
  params: {
  'account_id' => 'integer(int32)'
}

p JSON.parse(result)

```

`GET /ver1/bots/account_trade_info_smart_sell`

Smart Sell Account Table Info (Permission: NONE, Security: SIGNED)

<h3 id="getver1botsaccounttradeinfosmartsell-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|query|integer(int32)|true|none|

<h3 id="getver1botsaccounttradeinfosmartsell-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Smart Sell Account Table Info (Permission: NONE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1BotsAccountTradeInfo

<a id="opIdgetVer1BotsAccountTradeInfo"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/bots/account_trade_info',
  params: {
  'account_id' => 'integer(int32)'
}

p JSON.parse(result)

```

`GET /ver1/bots/account_trade_info`

Account Trade Info (Permission: NONE, Security: SIGNED)

<h3 id="getver1botsaccounttradeinfo-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|query|integer(int32)|true|none|

<h3 id="getver1botsaccounttradeinfo-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Account Trade Info (Permission: NONE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1BotsStrategyList

<a id="opIdgetVer1BotsStrategyList"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/bots/strategy_list',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/bots/strategy_list`

Available strategy list for bot (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1botsstrategylist-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|query|integer(int32)|false|id from GET /ver1/accounts|
|type|query|string|false|none|
|strategy|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|simple|
|type|composite|
|strategy|long|
|strategy|short|

<h3 id="getver1botsstrategylist-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Available strategy list for bot (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1BotsPairsBlackList

<a id="opIdgetVer1BotsPairsBlackList"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/bots/pairs_black_list',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/bots/pairs_black_list`

Black List for bot pairs (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1botspairsblacklist-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Black List for bot pairs (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsUpdatePairsBlackList

<a id="opIdpostVer1BotsUpdatePairsBlackList"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/update_pairs_black_list',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/bots/update_pairs_black_list`

Create or Update pairs BlackList for bots (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
pairs:
  - string

```

<h3 id="postver1botsupdatepairsblacklist-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» pairs|body|[string]|true|none|

<h3 id="postver1botsupdatepairsblacklist-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create or Update pairs BlackList for bots (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsCreateBot

<a id="opIdpostVer1BotsCreateBot"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/create_bot',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/bots/create_bot`

Create bot (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: string
account_id: 0
pairs:
  - string
max_active_deals: 1
base_order_volume: 0
base_order_volume_type: quote_currency
take_profit: 0
safety_order_volume: 0
safety_order_volume_type: quote_currency
martingale_volume_coefficient: 1
martingale_step_coefficient: 1
max_safety_orders: 0
active_safety_orders_count: 0
stop_loss_percentage: 0
cooldown: 0
trailing_enabled: true
trailing_deviation: 0
btc_price_limit: 0
strategy: short
safety_order_step_percentage: 0
take_profit_type: base
strategy_list:
  - null
leverage_type: custom
leverage_custom_value: 0
min_price: 0
max_price: 0
stop_loss_timeout_enabled: true
stop_loss_timeout_in_seconds: 0
min_volume_btc_24h: 0
tsl_enabled: true
deal_start_delay_seconds: 0
profit_currency: quote_currency
start_order_type: limit
stop_loss_type: stop_loss
disable_after_deals_count: 0
allowed_deals_on_same_pair: 0
close_deals_timeout: 0

```

<h3 id="postver1botscreatebot-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» name|body|string|true|none|
|» account_id|body|integer(int32)|true|id from GET /ver1/accounts|
|» pairs|body|[string]|true|Pass single pair to create SingleBot or any other number of pairs to create MultiBot|
|» max_active_deals|body|integer(int32)|false|none|
|» base_order_volume|body|number(double)|true|Base order size|
|» base_order_volume_type|body|string|false|base order volume currency|
|» take_profit|body|number(double)|true|Target profit(percentage)|
|» safety_order_volume|body|number(double)|true|Safety trade size|
|» safety_order_volume_type|body|string|false|safety order volume currency|
|» martingale_volume_coefficient|body|number(double)|true|none|
|» martingale_step_coefficient|body|number(double)|true|none|
|» max_safety_orders|body|integer(int32)|true|Max safety trades count|
|» active_safety_orders_count|body|integer(int32)|true|Max active safety trades count|
|» stop_loss_percentage|body|number(double)|false|none|
|» cooldown|body|number(double)|false|none|
|» trailing_enabled|body|boolean|false|Enable trailing take profit. Binance only.|
|» trailing_deviation|body|number(double)|false|required if trailing_enabled|
|» btc_price_limit|body|number(double)|false|none|
|» strategy|body|string|false|none|
|» safety_order_step_percentage|body|number(double)|true|Price deviation to open safety trades(percentage)|
|» take_profit_type|body|string|true|Percentage: base – from base order, total – from total volume|
|» strategy_list|body|[json]|true|For manual signals: [{"strategy":"manual"}] or []<br>|
|» leverage_type|body|string|false|Used for Bitmex bots only|
|» leverage_custom_value|body|number(double)|false|required if leverage_type is isolated|
|» min_price|body|number(double)|false|minimum price to open deal|
|» max_price|body|number(double)|false|maximum price to open deal|
|» stop_loss_timeout_enabled|body|boolean|false|none|
|» stop_loss_timeout_in_seconds|body|integer(int32)|false|StopLoss timeout in seconds if StopLoss timeout enabled|
|» min_volume_btc_24h|body|number(double)|false|none|
|» tsl_enabled|body|boolean|false|Enable trailing stop loss. Bitmex only.|
|» deal_start_delay_seconds|body|integer(int32)|false|Deal start delay in seconds|
|» profit_currency|body|string|false|Take profit currency|
|» start_order_type|body|string|false|none|
|» stop_loss_type|body|string|false|none|
|» disable_after_deals_count|body|integer(int32)|false|Bot will be disabled after opening this number of deals|
|» allowed_deals_on_same_pair|body|integer(int32)|false|Allow specific number of deals on the same pair. Multibot only.|
|» close_deals_timeout|body|integer(int32)|false|Close bot deals after given number of seconds. Must be greater than 60.|

#### Detailed descriptions

**» strategy_list**: For manual signals: [{"strategy":"manual"}] or []<br>
                                                        For non-stop(1 pair only): [{"strategy":"nonstop"}]<br>
                                                        QFL: {"options": {"type": "original"}, {"percent": 3}, "strategy": "qfl"}] <br>
                                                        TradingView: [{"options": {"time": "5m", "type": "buy_or_strong_buy"}, "strategy": "trading_view"}

#### Enumerated Values

|Parameter|Value|
|---|---|
|» base_order_volume_type|quote_currency|
|» base_order_volume_type|base_currency|
|» base_order_volume_type|percent|
|» base_order_volume_type|xbt|
|» safety_order_volume_type|quote_currency|
|» safety_order_volume_type|base_currency|
|» safety_order_volume_type|percent|
|» safety_order_volume_type|xbt|
|» strategy|short|
|» strategy|long|
|» take_profit_type|base|
|» take_profit_type|total|
|» leverage_type|custom|
|» leverage_type|cross|
|» leverage_type|not_specified|
|» leverage_type|isolated|
|» profit_currency|quote_currency|
|» profit_currency|base_currency|
|» start_order_type|limit|
|» start_order_type|market|
|» stop_loss_type|stop_loss|
|» stop_loss_type|stop_loss_and_disable_bot|

<h3 id="postver1botscreatebot-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1Bots

<a id="opIdgetVer1Bots"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/bots',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/bots`

User bots (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1bots-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer(int32)|false|Limit records. Max: 100|
|offset|query|integer(int32)|false|Offset records|
|from|query|string|false|Param for a filter by created date|
|account_id|query|integer(int32)|false|Account to show bots on. Return all if not specified. Gather this from GET /ver1/accounts|
|scope|query|string|false|none|
|strategy|query|string|false|none|
|sort_by|query|string|false|none|
|sort_direction|query|string|false|none|
|quote|query|string|false|Quote currency|

#### Enumerated Values

|Parameter|Value|
|---|---|
|scope|enabled|
|scope|disabled|
|strategy|long|
|strategy|short|
|sort_by|profit|
|sort_by|created_at|
|sort_by|updated_at|
|sort_direction|asc|
|sort_direction|desc|

<h3 id="getver1bots-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User bots (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1BotsStats

<a id="opIdgetVer1BotsStats"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/bots/stats',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/bots/stats`

Get bot stats (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1botsstats-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|query|integer(int32)|false|Account to show on. Null - show for all. Gather this from GET /ver1/accounts|
|bot_id|query|integer(int32)|false|Bots to show on. Null - show for all|

<h3 id="getver1botsstats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get bot stats (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsBotIdCopyAndCreate

<a id="opIdpostVer1BotsBotIdCopyAndCreate"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/{bot_id}/copy_and_create',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/bots/{bot_id}/copy_and_create`

POST /bots/:id/copy_and_create. Permission: BOTS_WRITE, Security: SIGNED

> Body parameter

```yaml
name: string
secret: string
amount: 0

```

<h3 id="postver1botsbotidcopyandcreate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» name|body|string|true|none|
|» secret|body|string|true|none|
|» amount|body|number(double)|false|Max amount for bot usage (Based on current rate)|

<h3 id="postver1botsbotidcopyandcreate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|POST /bots/:id/copy_and_create. Permission: BOTS_WRITE, Security: SIGNED|None|

<aside class="success">
This operation does not require authentication
</aside>

## patchVer1BotsBotIdUpdate

<a id="opIdpatchVer1BotsBotIdUpdate"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.patch '/api.3commas.io/public/api/ver1/bots/{bot_id}/update',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /ver1/bots/{bot_id}/update`

Edit bot (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: string
pairs:
  - string
max_active_deals: 1
base_order_volume: 0
base_order_volume_type: quote_currency
take_profit: 0
safety_order_volume: 0
safety_order_volume_type: quote_currency
martingale_volume_coefficient: 1
martingale_step_coefficient: 1
max_safety_orders: 0
active_safety_orders_count: 0
stop_loss_percentage: 0
cooldown: 0
trailing_enabled: true
trailing_deviation: 0
btc_price_limit: 0
safety_order_step_percentage: 0
take_profit_type: total
strategy_list:
  - null
leverage_type: custom
leverage_custom_value: 0
min_price: 0
max_price: 0
stop_loss_timeout_enabled: true
stop_loss_timeout_in_seconds: 0
min_volume_btc_24h: 0
tsl_enabled: true
deal_start_delay_seconds: 0
profit_currency: quote_currency
start_order_type: limit
stop_loss_type: stop_loss
disable_after_deals_count: 0
allowed_deals_on_same_pair: 0
close_deals_timeout: 0

```

<h3 id="patchver1botsbotidupdate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» name|body|string|true|none|
|» pairs|body|[string]|true|none|
|» max_active_deals|body|integer(int32)|false|none|
|» base_order_volume|body|number(double)|true|Base order size|
|» base_order_volume_type|body|string|false|base order volume currency|
|» take_profit|body|number(double)|true|Target profit(percentage)|
|» safety_order_volume|body|number(double)|true|Safety trade size|
|» safety_order_volume_type|body|string|false|safety order volume currency|
|» martingale_volume_coefficient|body|number(double)|true|none|
|» martingale_step_coefficient|body|number(double)|true|none|
|» max_safety_orders|body|integer(int32)|true|Max safety trades count|
|» active_safety_orders_count|body|integer(int32)|true|Max active safety trades count|
|» stop_loss_percentage|body|number(double)|false|none|
|» cooldown|body|number(double)|false|none|
|» trailing_enabled|body|boolean|false|Enable trailing take profit. Binance only.|
|» trailing_deviation|body|number(double)|false|required if trailing_enabled|
|» btc_price_limit|body|number(double)|false|none|
|» safety_order_step_percentage|body|number(double)|true|Price deviation to open safety trades(percentage)|
|» take_profit_type|body|string|true|Percentage: base – from base order, total – from total volume|
|» strategy_list|body|[json]|true|For manual signals: [{"strategy":"manual"}] or []<br>|
|» leverage_type|body|string|false|Used for Bitmex bots only|
|» leverage_custom_value|body|number(double)|false|required if leverage_type is isolated|
|» min_price|body|number(double)|false|minimum price to open deal|
|» max_price|body|number(double)|false|maximum price to open deal|
|» stop_loss_timeout_enabled|body|boolean|false|none|
|» stop_loss_timeout_in_seconds|body|integer(int32)|false|StopLoss timeout in seconds if StopLoss timeout enabled|
|» min_volume_btc_24h|body|number(double)|false|none|
|» tsl_enabled|body|boolean|false|Enable trailing stop loss. Bitmex only.|
|» deal_start_delay_seconds|body|integer(int32)|false|Deal start delay in seconds|
|» profit_currency|body|string|false|Take profit currency|
|» start_order_type|body|string|false|none|
|» stop_loss_type|body|string|false|none|
|» disable_after_deals_count|body|integer(int32)|false|Bot will be disabled after opening this number of deals|
|» allowed_deals_on_same_pair|body|integer(int32)|false|Allow specific number of deals on the same pair. Multibot only.|
|» close_deals_timeout|body|integer(int32)|false|Close bot deals after given number of seconds. Must be greater than 60.|

#### Detailed descriptions

**» strategy_list**: For manual signals: [{"strategy":"manual"}] or []<br>
                                                        For non-stop(1 pair only): [{"strategy":"nonstop"}]<br>
                                                        QFL: {"options": {"type": "original"}, {"percent": 3}, "strategy": "qfl"}] <br>
                                                        TradingView: [{"options": {"time": "5m", "type": "buy_or_strong_buy", "strategy": "trading_view"}

#### Enumerated Values

|Parameter|Value|
|---|---|
|» base_order_volume_type|quote_currency|
|» base_order_volume_type|base_currency|
|» base_order_volume_type|percent|
|» base_order_volume_type|xbt|
|» safety_order_volume_type|quote_currency|
|» safety_order_volume_type|base_currency|
|» safety_order_volume_type|percent|
|» safety_order_volume_type|xbt|
|» take_profit_type|total|
|» take_profit_type|base|
|» leverage_type|custom|
|» leverage_type|cross|
|» leverage_type|not_specified|
|» leverage_type|isolated|
|» profit_currency|quote_currency|
|» profit_currency|base_currency|
|» start_order_type|limit|
|» start_order_type|market|
|» stop_loss_type|stop_loss|
|» stop_loss_type|stop_loss_and_disable_bot|

<h3 id="patchver1botsbotidupdate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Edit bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsBotIdDisable

<a id="opIdpostVer1BotsBotIdDisable"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/{bot_id}/disable',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/bots/{bot_id}/disable`

Disable bot (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1botsbotiddisable-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|

<h3 id="postver1botsbotiddisable-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Disable bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsBotIdEnable

<a id="opIdpostVer1BotsBotIdEnable"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/{bot_id}/enable',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/bots/{bot_id}/enable`

Enable bot (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1botsbotidenable-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|

<h3 id="postver1botsbotidenable-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Enable bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsBotIdStartNewDeal

<a id="opIdpostVer1BotsBotIdStartNewDeal"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/{bot_id}/start_new_deal',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/bots/{bot_id}/start_new_deal`

Start new deal asap (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
pair: string
skip_signal_checks: true
skip_open_deals_checks: true

```

<h3 id="postver1botsbotidstartnewdeal-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|
|body|body|object|false|none|
|» pair|body|string|false|Can be omited for simple bot|
|» skip_signal_checks|body|boolean|false|If false or not specified then all paramaters like signals or volume filters will be checked. If true - those checks will be skipped|
|» skip_open_deals_checks|body|boolean|false|If true then you will be allowed to open more then one deal per pair in composite bot|

<h3 id="postver1botsbotidstartnewdeal-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Start new deal asap (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsBotIdDelete

<a id="opIdpostVer1BotsBotIdDelete"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/{bot_id}/delete',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/bots/{bot_id}/delete`

Delete bot (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1botsbotiddelete-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|

<h3 id="postver1botsbotiddelete-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Delete bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsBotIdPanicSellAllDeals

<a id="opIdpostVer1BotsBotIdPanicSellAllDeals"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/{bot_id}/panic_sell_all_deals',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/bots/{bot_id}/panic_sell_all_deals`

Panic sell all bot deals (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1botsbotidpanicsellalldeals-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|

<h3 id="postver1botsbotidpanicsellalldeals-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Panic sell all bot deals (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1BotsBotIdCancelAllDeals

<a id="opIdpostVer1BotsBotIdCancelAllDeals"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/bots/{bot_id}/cancel_all_deals',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/bots/{bot_id}/cancel_all_deals`

Cancel all bot deals (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1botsbotidcancelalldeals-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|

<h3 id="postver1botsbotidcancelalldeals-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Cancel all bot deals (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1BotsBotIdDealsStats

<a id="opIdgetVer1BotsBotIdDealsStats"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/bots/{bot_id}/deals_stats',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/bots/{bot_id}/deals_stats`

Bot deals stats (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1botsbotiddealsstats-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|bot_id|path|integer(int32)|true|none|

<h3 id="getver1botsbotiddealsstats-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Bot deals stats (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1BotsBotIdShow

<a id="opIdgetVer1BotsBotIdShow"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/bots/{bot_id}/show',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/bots/{bot_id}/show`

Bot info (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1botsbotidshow-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|include_events|query|boolean|false|none|
|bot_id|path|integer(int32)|true|none|

<h3 id="getver1botsbotidshow-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Bot info (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-deals">deals</h1>

Operations about deals

## getVer1Deals

<a id="opIdgetVer1Deals"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/deals',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/deals`

User deals (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1deals-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer(int32)|false|Limit records. Max: 1_000|
|offset|query|integer(int32)|false|Offset records|
|from|query|string|false|Param for a filter by created date|
|account_id|query|integer(int32)|false|Account to show bots on. Return all if not specified. Gather this from GET /ver1/accounts|
|bot_id|query|integer(int32)|false|Bot show deals on. Return all if not specified|
|scope|query|string|false|active - active deals, finished - finished deals, completed - successfully completed, cancelled - cancelled deals, failed - failed deals, any other value or null (default) - all deals|
|order|query|string|false|none|
|order_direction|query|string|false|none|
|base|query|string|false|Base currency|
|quote|query|string|false|Quote currency|

#### Enumerated Values

|Parameter|Value|
|---|---|
|order|created_at|
|order|updated_at|
|order|closed_at|
|order|profit|
|order|profit_percentage|
|order_direction|asc|
|order_direction|desc|

<h3 id="getver1deals-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User deals (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1DealsDealIdConvertToSmartTrade

<a id="opIdpostVer1DealsDealIdConvertToSmartTrade"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/deals/{deal_id}/convert_to_smart_trade',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/deals/{deal_id}/convert_to_smart_trade`

Convert to smart trade (Permission: SMART_TRADE_WRITE, Security: SIGNED)

> Body parameter

```yaml
stop_bot: false

```

<h3 id="postver1dealsdealidconverttosmarttrade-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|
|body|body|object|false|none|
|» stop_bot|body|boolean|false|none|

<h3 id="postver1dealsdealidconverttosmarttrade-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Convert to smart trade (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1DealsDealIdUpdateMaxSafetyOrders

<a id="opIdpostVer1DealsDealIdUpdateMaxSafetyOrders"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/deals/{deal_id}/update_max_safety_orders',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/deals/{deal_id}/update_max_safety_orders`

Update max safety orders (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
max_safety_orders: 0

```

<h3 id="postver1dealsdealidupdatemaxsafetyorders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» max_safety_orders|body|integer(int32)|true|New maximum safety orders value|

<h3 id="postver1dealsdealidupdatemaxsafetyorders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Update max safety orders (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1DealsDealIdPanicSell

<a id="opIdpostVer1DealsDealIdPanicSell"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/deals/{deal_id}/panic_sell',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/deals/{deal_id}/panic_sell`

Panic sell deal (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1dealsdealidpanicsell-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|

<h3 id="postver1dealsdealidpanicsell-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Panic sell deal (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1DealsDealIdCancel

<a id="opIdpostVer1DealsDealIdCancel"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/deals/{deal_id}/cancel',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/deals/{deal_id}/cancel`

Cancel deal (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1dealsdealidcancel-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|

<h3 id="postver1dealsdealidcancel-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Cancel deal (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## patchVer1DealsDealIdUpdateDeal

<a id="opIdpatchVer1DealsDealIdUpdateDeal"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.patch '/api.3commas.io/public/api/ver1/deals/{deal_id}/update_deal',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /ver1/deals/{deal_id}/update_deal`

Update deal (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
take_profit: 0
profit_currency: quote_currency
take_profit_type: string
trailing_enabled: true
trailing_deviation: 0
stop_loss_percentage: 0
max_safety_orders: 0
active_safety_orders_count: 0
stop_loss_timeout_enabled: true
stop_loss_timeout_in_seconds: 0
tsl_enabled: true
stop_loss_type: stop_loss
close_timeout: 0

```

<h3 id="patchver1dealsdealidupdatedeal-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|
|body|body|object|false|none|
|» take_profit|body|number(double)|false|New take profit value|
|» profit_currency|body|string|false|none|
|» take_profit_type|body|string|false|base – from base order, total – from total volume|
|» trailing_enabled|body|boolean|false|none|
|» trailing_deviation|body|number(double)|false|New trailing deviation value|
|» stop_loss_percentage|body|number(double)|false|New stop loss percentage value|
|» max_safety_orders|body|integer(int32)|false|New max safety orders value|
|» active_safety_orders_count|body|integer(int32)|false|New active safety orders count value|
|» stop_loss_timeout_enabled|body|boolean|false|none|
|» stop_loss_timeout_in_seconds|body|integer(int32)|false|StopLoss timeout in seconds if StopLoss timeout enabled|
|» tsl_enabled|body|boolean|false|Trailing stop loss enabled|
|» stop_loss_type|body|string|false|none|
|» close_timeout|body|integer(int32)|false|Close deal after given number of seconds. Must be greater than 60.|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» profit_currency|quote_currency|
|» profit_currency|base_currency|
|» stop_loss_type|stop_loss|
|» stop_loss_type|stop_loss_and_disable_bot|

<h3 id="patchver1dealsdealidupdatedeal-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update deal (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1DealsDealIdUpdateTp

<a id="opIdpostVer1DealsDealIdUpdateTp"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/deals/{deal_id}/update_tp',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/deals/{deal_id}/update_tp`

DEPRECATED, Update take profit condition. Deal status should be bought (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
new_take_profit_percentage: 0

```

<h3 id="postver1dealsdealidupdatetp-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» new_take_profit_percentage|body|number(double)|true|New take profit value|

<h3 id="postver1dealsdealidupdatetp-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|DEPRECATED, Update take profit condition. Deal status should be bought (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1DealsDealIdShow

<a id="opIdgetVer1DealsDealIdShow"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/deals/{deal_id}/show',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/deals/{deal_id}/show`

Info about specific deal (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1dealsdealidshow-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|

<h3 id="getver1dealsdealidshow-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Info about specific deal (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1DealsDealIdCancelOrder

<a id="opIdpostVer1DealsDealIdCancelOrder"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/deals/{deal_id}/cancel_order',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/deals/{deal_id}/cancel_order`

Cancel manual safety orders (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
order_id: string

```

<h3 id="postver1dealsdealidcancelorder-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» order_id|body|string|true|manual safety order id|

<h3 id="postver1dealsdealidcancelorder-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Cancel manual safety orders (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1DealsDealIdMarketOrders

<a id="opIdgetVer1DealsDealIdMarketOrders"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/deals/{deal_id}/market_orders',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/deals/{deal_id}/market_orders`

Deal safety orders (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1dealsdealidmarketorders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|

<h3 id="getver1dealsdealidmarketorders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Deal safety orders (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1DealsDealIdAddFunds

<a id="opIdpostVer1DealsDealIdAddFunds"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/deals/{deal_id}/add_funds',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/deals/{deal_id}/add_funds`

Adding manual safety order (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
quantity: 0
is_market: true
response_type: empty
rate: 0

```

<h3 id="postver1dealsdealidaddfunds-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» quantity|body|number(double)|true|safety order quantity|
|» is_market|body|boolean|true|true - use MARKET order, false - use LIMIT order|
|» response_type|body|string|false|none|
|» rate|body|number(double)|true|safety order rate. Required if LIMIT order used|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» response_type|empty|
|» response_type|deal|
|» response_type|market_order|

<h3 id="postver1dealsdealidaddfunds-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Adding manual safety order (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1DealsDealIdDataForAddingFunds

<a id="opIdgetVer1DealsDealIdDataForAddingFunds"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/deals/{deal_id}/data_for_adding_funds',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/deals/{deal_id}/data_for_adding_funds`

Info required to add funds correctly: available amounts, exchange limitations etc  (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1dealsdealiddataforaddingfunds-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|deal_id|path|integer(int32)|true|none|

<h3 id="getver1dealsdealiddataforaddingfunds-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Info required to add funds correctly: available amounts, exchange limitations etc  (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-users">users</h1>

Operations about users

## getVer1UsersCurrentMode

<a id="opIdgetVer1UsersCurrentMode"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/users/current_mode',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/users/current_mode`

Current User Mode (Paper or Real) (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1userscurrentmode-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Current User Mode (Paper or Real) (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1UsersChangeMode

<a id="opIdpostVer1UsersChangeMode"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/users/change_mode',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/users/change_mode`

Change User Mode (Paper or Real) (Permission: ACCOUNTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
mode: paper

```

<h3 id="postver1userschangemode-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» mode|body|string|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» mode|paper|
|» mode|real|

<h3 id="postver1userschangemode-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Change User Mode (Paper or Real) (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-accounts">accounts</h1>

Operations about accounts

## postVer1AccountsTransfer

<a id="opIdpostVer1AccountsTransfer"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/transfer',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/accounts/transfer`

Transfer coins between accounts (Permission: ACCOUNTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
currency: string
amount: 0
to_account_id: 0
from_account_id: 0

```

<h3 id="postver1accountstransfer-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» currency|body|string|true|Currency code(example: USDT)|
|» amount|body|number(double)|true|none|
|» to_account_id|body|integer(int32)|true|Recipient account ID (possible values in /transfer_data)|
|» from_account_id|body|integer(int32)|true|Sender account ID (possible values in /transfer_data)|

<h3 id="postver1accountstransfer-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Transfer coins between accounts (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsTransferHistory

<a id="opIdgetVer1AccountsTransferHistory"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/transfer_history',
  params: {
  'account_id' => 'integer(int32)',
'currency' => 'string'
}

p JSON.parse(result)

```

`GET /ver1/accounts/transfer_history`

Transfers history (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1accountstransferhistory-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|query|integer(int32)|true|Sender or Recipient account ID (possible values in /transfer_data)|
|currency|query|string|true|Currency code(example: USDT)|
|page|query|integer(int32)|false|Page number|
|per_page|query|integer(int32)|false|Elements per page|

<h3 id="getver1accountstransferhistory-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Transfers history (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsTransferData

<a id="opIdgetVer1AccountsTransferData"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/transfer_data',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/accounts/transfer_data`

Data for transfer between accounts (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1accountstransferdata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Data for transfer between accounts (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsNew

<a id="opIdpostVer1AccountsNew"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/new',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/accounts/new`

Add exchange account  (Permission: ACCOUNTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
type: string
name: string
api_key: string
secret: string
address: string
customer_id: string
passphrase: string
subaccount_name: string
how_connect: mnemonic_phrase
keystore: null
wallet_password: string
mnemonic_phrase: string

```

<h3 id="postver1accountsnew-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» type|body|string|true|check market_code in market_list method|
|» name|body|string|true|Account name (any string)|
|» api_key|body|string|false|Requires unless type = binance_dex|
|» secret|body|string|false|Requires unless type = binance_dex|
|» address|body|string|false|Requires if type = ethereumwallet|
|» customer_id|body|string|false|For Bitstamp|
|» passphrase|body|string|false|For Coinbase Pro (GDAX)|
|» subaccount_name|body|string|false|For FTX|
|» how_connect|body|string|false|none|
|» keystore|body|json|false|keystore file content. Requires if type = binance_dex and how_connect = keystore|
|» wallet_password|body|string|false|Requires if type = binance_dex and how_connect = keystore|
|» mnemonic_phrase|body|string|false|Requires if type = binance_dex and how_connect = mnemonic_phrase|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» how_connect|mnemonic_phrase|
|» how_connect|keystore|

<h3 id="postver1accountsnew-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Add exchange account  (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsUpdate

<a id="opIdpostVer1AccountsUpdate"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/update',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/accounts/update`

Edit exchange account

> Body parameter

```yaml
account_id: 0
name: string
api_key: string
secret: string
customer_id: string
passphrase: string
subaccount_name: string
address: string
how_connect: mnemonic_phrase
keystore: null
wallet_password: string
mnemonic_phrase: string

```

<h3 id="postver1accountsupdate-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» account_id|body|integer(int32)|true|none|
|» name|body|string|false|Account name (any string)|
|» api_key|body|string|false|none|
|» secret|body|string|false|none|
|» customer_id|body|string|false|For Bitstamp|
|» passphrase|body|string|false|For Coinbase Pro (GDAX)|
|» subaccount_name|body|string|false|For FTX|
|» address|body|string|false|For accounts with type = ethereumwallet|
|» how_connect|body|string|false|none|
|» keystore|body|json|false|none|
|» wallet_password|body|string|false|none|
|» mnemonic_phrase|body|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» how_connect|mnemonic_phrase|
|» how_connect|keystore|

<h3 id="postver1accountsupdate-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Edit exchange account|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1Accounts

<a id="opIdgetVer1Accounts"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/accounts`

User connected exchanges(and EthereumWallet) list (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1accounts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|page|query|integer(int32)|false|none|
|per_page|query|integer(int32)|false|Page size, from 1 to 100|

<h3 id="getver1accounts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User connected exchanges(and EthereumWallet) list (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsMarketList

<a id="opIdgetVer1AccountsMarketList"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/market_list',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/accounts/market_list`

Supported markets list (Permission: NONE, Security: NONE)

<h3 id="getver1accountsmarketlist-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Supported markets list (Permission: NONE, Security: NONE)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsMarketPairs

<a id="opIdgetVer1AccountsMarketPairs"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/market_pairs',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/accounts/market_pairs`

All market pairs (Permission: NONE, Security: NONE)

<h3 id="getver1accountsmarketpairs-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|pretty_display_type|query|string|false|deprecated. mandatory use market_code instead|
|market_code|query|string|false|market_code from account model|

<h3 id="getver1accountsmarketpairs-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|All market pairs (Permission: NONE, Security: NONE)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsCurrencyRatesWithLeverageData

<a id="opIdgetVer1AccountsCurrencyRatesWithLeverageData"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/currency_rates_with_leverage_data',
  params: {
  'market_code' => 'string',
'pair' => 'string'
}

p JSON.parse(result)

```

`GET /ver1/accounts/currency_rates_with_leverage_data`

Currency rates and limits with leverage data (Permission: NONE, Security: NONE)

<h3 id="getver1accountscurrencyrateswithleveragedata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|market_code|query|string|true|market_code from account model|
|pair|query|string|true|Pair|

<h3 id="getver1accountscurrencyrateswithleveragedata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Currency rates and limits with leverage data (Permission: NONE, Security: NONE)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsCurrencyRates

<a id="opIdgetVer1AccountsCurrencyRates"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/currency_rates',
  params: {
  'pair' => 'string'
}

p JSON.parse(result)

```

`GET /ver1/accounts/currency_rates`

Currency rates and limits (Permission: NONE, Security: NONE)

<h3 id="getver1accountscurrencyrates-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit_type|query|string|false|Type of limits - bot or smart_trade|
|pretty_display_type|query|string|false|deprecated. use market_code instead|
|market_code|query|string|false|market_code from account model. If you are retrieving data for pairs, you must also include market_code|
|pair|query|string|true|Pair|

<h3 id="getver1accountscurrencyrates-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Currency rates and limits (Permission: NONE, Security: NONE)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsAccountIdDepositData

<a id="opIdgetVer1AccountsAccountIdDepositData"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/{account_id}/deposit_data',
  params: {
  'currency' => 'string',
'network' => 'string'
}

p JSON.parse(result)

```

`GET /ver1/accounts/{account_id}/deposit_data`

User Deposit Data (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1accountsaccountiddepositdata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|currency|query|string|true|none|
|network|query|string|true|none|
|account_id|path|integer(int32)|true|none|

<h3 id="getver1accountsaccountiddepositdata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|User Deposit Data (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsAccountIdNetworksInfo

<a id="opIdgetVer1AccountsAccountIdNetworksInfo"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/{account_id}/networks_info',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/accounts/{account_id}/networks_info`

Deposit/withdraw networks info (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1accountsaccountidnetworksinfo-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|purpose|query|string|false|Filter currencies with deposit/withdraw enabled|
|account_id|path|integer(int32)|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|purpose|deposit|
|purpose|withdraw|

<h3 id="getver1accountsaccountidnetworksinfo-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Deposit/withdraw networks info (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsAccountIdConvertDustToBnb

<a id="opIdpostVer1AccountsAccountIdConvertDustToBnb"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/{account_id}/convert_dust_to_bnb',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/accounts/{account_id}/convert_dust_to_bnb`

Convert dust coins to BNB (Permission: ACCOUNTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
codes:
  - string

```

<h3 id="postver1accountsaccountidconvertdusttobnb-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|
|body|body|object|false|none|
|» codes|body|[string]|false|Array of currency codes|

<h3 id="postver1accountsaccountidconvertdusttobnb-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Convert dust coins to BNB (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsAccountIdActiveTradingEntities

<a id="opIdgetVer1AccountsAccountIdActiveTradingEntities"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/{account_id}/active_trading_entities',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/accounts/{account_id}/active_trading_entities`

Active trade entities (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1accountsaccountidactivetradingentities-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|

<h3 id="getver1accountsaccountidactivetradingentities-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Active trade entities (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsAccountIdSellAllToUsd

<a id="opIdpostVer1AccountsAccountIdSellAllToUsd"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/{account_id}/sell_all_to_usd',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/accounts/{account_id}/sell_all_to_usd`

Sell all to USD  (Permission: ACCOUNTS_WRITE, Security: SIGNED)

<h3 id="postver1accountsaccountidsellalltousd-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|

<h3 id="postver1accountsaccountidsellalltousd-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Sell all to USD  (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsAccountIdSellAllToBtc

<a id="opIdpostVer1AccountsAccountIdSellAllToBtc"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/{account_id}/sell_all_to_btc',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/accounts/{account_id}/sell_all_to_btc`

Sell all to BTC  (Permission: ACCOUNTS_WRITE, Security: SIGNED)

<h3 id="postver1accountsaccountidsellalltobtc-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|

<h3 id="postver1accountsaccountidsellalltobtc-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Sell all to BTC  (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsAccountIdBalanceChartData

<a id="opIdgetVer1AccountsAccountIdBalanceChartData"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/{account_id}/balance_chart_data',
  params: {
  'date_from' => 'string(date-time)'
}

p JSON.parse(result)

```

`GET /ver1/accounts/{account_id}/balance_chart_data`

balance history data (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1accountsaccountidbalancechartdata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|date_from|query|string(date-time)|true|none|
|date_to|query|string(date-time)|false|none|
|account_id|path|integer(int32)|true|none|

<h3 id="getver1accountsaccountidbalancechartdata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|balance history data (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsAccountIdLoadBalances

<a id="opIdpostVer1AccountsAccountIdLoadBalances"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/{account_id}/load_balances',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/accounts/{account_id}/load_balances`

Load balances for specified exchange  (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="postver1accountsaccountidloadbalances-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|

<h3 id="postver1accountsaccountidloadbalances-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Load balances for specified exchange  (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsAccountIdRename

<a id="opIdpostVer1AccountsAccountIdRename"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/{account_id}/rename',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/accounts/{account_id}/rename`

Rename exchange connection  (Permission: ACCOUNTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: string

```

<h3 id="postver1accountsaccountidrename-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» name|body|string|true|none|

<h3 id="postver1accountsaccountidrename-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Rename exchange connection  (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsAccountIdPieChartData

<a id="opIdpostVer1AccountsAccountIdPieChartData"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/{account_id}/pie_chart_data',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/accounts/{account_id}/pie_chart_data`

Information about all user balances on specified exchange in pretty for pie chart format (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="postver1accountsaccountidpiechartdata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|

<h3 id="postver1accountsaccountidpiechartdata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Information about all user balances on specified exchange in pretty for pie chart format (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsAccountIdAccountTableData

<a id="opIdpostVer1AccountsAccountIdAccountTableData"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/{account_id}/account_table_data',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/accounts/{account_id}/account_table_data`

Information about all user balances on specified exchange  (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="postver1accountsaccountidaccounttabledata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|

<h3 id="postver1accountsaccountidaccounttabledata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Information about all user balances on specified exchange  (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1AccountsAccountIdRemove

<a id="opIdpostVer1AccountsAccountIdRemove"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/accounts/{account_id}/remove',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/accounts/{account_id}/remove`

Remove exchange connection  (Permission: ACCOUNTS_WRITE, Security: SIGNED)

<h3 id="postver1accountsaccountidremove-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|

<h3 id="postver1accountsaccountidremove-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Remove exchange connection  (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsAccountIdLeverageData

<a id="opIdgetVer1AccountsAccountIdLeverageData"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/{account_id}/leverage_data',
  params: {
  'pair' => 'string'
}

p JSON.parse(result)

```

`GET /ver1/accounts/{account_id}/leverage_data`

Information about account leverage (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1accountsaccountidleveragedata-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|pair|query|string|true|none|
|account_id|path|integer(int32)|true|none|

<h3 id="getver1accountsaccountidleveragedata-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Information about account leverage (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1AccountsAccountId

<a id="opIdgetVer1AccountsAccountId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/accounts/{account_id}',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/accounts/{account_id}`

Single Account Info (Permission: ACCOUNTS_READ, Security: SIGNED)
You can send 'summary' instead of {account_id} to get summary account info

<h3 id="getver1accountsaccountid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|

<h3 id="getver1accountsaccountid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Single Account Info (Permission: ACCOUNTS_READ, Security: SIGNED)
You can send 'summary' instead of {account_id} to get summary account info|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-marketplace">marketplace</h1>

Operations about marketplaces

## getVer1MarketplacePresets

<a id="opIdgetVer1MarketplacePresets"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded',
  'Accept' => 'application/json'
}

result = RestClient.get '/api.3commas.io/public/api/ver1/marketplace/presets',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /ver1/marketplace/presets`

Marketplace presets (Permission: NONE, Security: SIGNED)

> Body parameter

```yaml
account_types:
  - string
markets:
  - string
pairs:
  - string
deal_start_conditions:
  - string

```

<h3 id="getver1marketplacepresets-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|profit_per_day_from|query|number(double)|false|none|
|profit_per_day_to|query|number(double)|false|none|
|profit_per_month_from|query|number(double)|false|none|
|profit_per_month_to|query|number(double)|false|none|
|with_all_market_pairs|query|boolean|false|none|
|days_running_from|query|integer(int32)|false|none|
|days_running_to|query|integer(int32)|false|none|
|bot_type|query|string|false|none|
|bot_strategy|query|string|false|none|
|cmc|query|string|false|none|
|sort_by|query|string|false|none|
|sort_direction|query|string|false|none|
|page|query|integer(int32)|false|none|
|per_page|query|integer(int32)|false|none|
|body|body|object|false|none|
|» account_types|body|[string]|false|none|
|» markets|body|[string]|false|none|
|» pairs|body|[string]|false|none|
|» deal_start_conditions|body|[string]|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|sort_direction|asc|
|sort_direction|desc|

> Example responses

> 200 Response

```json
{
  "bots": [
    {
      "id": 0,
      "type": "string",
      "name": "string",
      "strategy": "string",
      "secret": "string",
      "marketplace_item": {
        "id": 0,
        "name": "string",
        "icon_url": "string"
      },
      "profit": {
        "period": "string",
        "amount": 0,
        "chart_data": [
          0
        ]
      },
      "currencies": [
        "string"
      ],
      "copies": 0,
      "is_favorite": true
    }
  ],
  "total": 0,
  "page": 0
}
```

<h3 id="getver1marketplacepresets-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Marketplace presets (Permission: NONE, Security: SIGNED)|[MarketplacePresets_IndexEntity](#schemamarketplacepresets_indexentity)|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1MarketplaceItems

<a id="opIdgetVer1MarketplaceItems"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/marketplace/items',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/marketplace/items`

All marketplace items (Permission: NONE, Security: NONE)

<h3 id="getver1marketplaceitems-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer(int32)|false|Limit records. Max: 1_000|
|offset|query|integer(int32)|false|Offset records|
|scope|query|string|false|paid - show only paid signal providers. free - show only free signal providers|
|order|query|string|false|none|
|locale|query|string|false|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|scope|all|
|scope|paid|
|scope|free|
|order|subscribers|
|order|name|
|order|newest|
|locale|en|
|locale|ru|
|locale|zh|
|locale|zh-CN|
|locale|es|
|locale|pt|
|locale|ko|
|locale|fr|
|locale|cs|
|locale|tr|
|locale|de|

<h3 id="getver1marketplaceitems-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|All marketplace items (Permission: NONE, Security: NONE)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1MarketplaceItemIdSignals

<a id="opIdgetVer1MarketplaceItemIdSignals"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/marketplace/{item_id}/signals',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/marketplace/{item_id}/signals`

Marketplace Item Signals (Permission: NONE, Security: NONE)

<h3 id="getver1marketplaceitemidsignals-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|limit|query|integer(int32)|false|Limit records. Max: 1_000|
|offset|query|integer(int32)|false|Offset records|
|order|query|string|false|none|
|order_direction|query|string|false|none|
|locale|query|string|false|none|
|item_id|path|integer(int32)|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|order|pair|
|order|exchange|
|order|signal_type|
|order|date|
|order_direction|asc|
|order_direction|desc|
|locale|en|
|locale|ru|
|locale|zh|
|locale|zh-CN|
|locale|es|
|locale|pt|
|locale|ko|
|locale|fr|
|locale|cs|
|locale|tr|
|locale|de|

<h3 id="getver1marketplaceitemidsignals-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Marketplace Item Signals (Permission: NONE, Security: NONE)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-grid_bots">grid_bots</h1>

Operations about grid_bots

## postVer1GridBotsAi

<a id="opIdpostVer1GridBotsAi"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/grid_bots/ai',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/grid_bots/ai`

Create AI Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: GridBot
account_id: 0
pair: string
total_quantity: 0
leverage_type: custom
leverage_custom_value: 0

```

<h3 id="postver1gridbotsai-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» name|body|string|false|Grid Bot's name|
|» account_id|body|integer(int32)|true|id from GET /ver1/accounts|
|» pair|body|string|true|none|
|» total_quantity|body|number(double)|true|none|
|» leverage_type|body|string|false|Leverage type for futures accounts|
|» leverage_custom_value|body|number(double)|false|Required if leverage_type = 'isolated'|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» leverage_type|custom|
|» leverage_type|cross|
|» leverage_type|not_specified|
|» leverage_type|isolated|

<h3 id="postver1gridbotsai-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create AI Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1GridBotsManual

<a id="opIdpostVer1GridBotsManual"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/grid_bots/manual',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/grid_bots/manual`

Create Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: GridBot
account_id: 0
pair: string
upper_price: 0
lower_price: 0
quantity_per_grid: 0
grids_quantity: 0
upper_stop_loss_price: 0
upper_stop_loss_enabled: false
upper_stop_loss_action: stop_bot
lower_stop_loss_price: 0
lower_stop_loss_enabled: false
lower_stop_loss_action: stop_bot
leverage_type: custom
leverage_custom_value: 0
is_enabled: true

```

<h3 id="postver1gridbotsmanual-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|false|none|
|» name|body|string|false|Grid Bot's name|
|» account_id|body|integer(int32)|true|id from GET /ver1/accounts|
|» pair|body|string|true|none|
|» upper_price|body|number(double)|true|none|
|» lower_price|body|number(double)|true|none|
|» quantity_per_grid|body|number(double)|true|none|
|» grids_quantity|body|number(double)|true|none|
|» upper_stop_loss_price|body|number(double)|false|none|
|» upper_stop_loss_enabled|body|boolean|false|none|
|» upper_stop_loss_action|body|string|false|none|
|» lower_stop_loss_price|body|number(double)|false|none|
|» lower_stop_loss_enabled|body|boolean|false|none|
|» lower_stop_loss_action|body|string|false|none|
|» leverage_type|body|string|false|Leverage type for futures accounts|
|» leverage_custom_value|body|number(double)|false|Required if leverage_type = 'isolated'|
|» is_enabled|body|boolean|false|Turn on or off grid_bot after creation|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» upper_stop_loss_action|stop_bot|
|» upper_stop_loss_action|stop_bot_and_buy|
|» upper_stop_loss_action|stop_bot_and_sell|
|» upper_stop_loss_action|stop_bot_and_close_position|
|» lower_stop_loss_action|stop_bot|
|» lower_stop_loss_action|stop_bot_and_buy|
|» lower_stop_loss_action|stop_bot_and_sell|
|» lower_stop_loss_action|stop_bot_and_close_position|
|» leverage_type|custom|
|» leverage_type|cross|
|» leverage_type|not_specified|
|» leverage_type|isolated|

<h3 id="postver1gridbotsmanual-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1GridBotsAiSettings

<a id="opIdgetVer1GridBotsAiSettings"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/grid_bots/ai_settings',
  params: {
  'pair' => 'string',
'market_code' => 'string'
}

p JSON.parse(result)

```

`GET /ver1/grid_bots/ai_settings`

Get AI settings (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1gridbotsaisettings-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|pair|query|string|true|none|
|market_code|query|string|true|Market code from /accounts/market_list|

<h3 id="getver1gridbotsaisettings-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get AI settings (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1GridBots

<a id="opIdgetVer1GridBots"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.get '/api.3commas.io/public/api/ver1/grid_bots',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /ver1/grid_bots`

Grid bots list (Permission: BOTS_READ, Security: SIGNED)

> Body parameter

```yaml
account_ids:
  - 0
account_types:
  - string

```

<h3 id="getver1gridbots-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|state|query|string|false|Filter by bot state|
|sort_by|query|string|false|Sort column|
|sort_direction|query|string|false|Sort direction|
|limit|query|integer(int32)|false|none|
|offset|query|integer(int32)|false|none|
|from|query|string|false|Param for a filter by created date|
|base|query|string|false|Base currency|
|quote|query|string|false|Quote currency|
|body|body|object|false|none|
|» account_ids|body|[integer]|false|Filter by account id|
|» account_types|body|[string]|false|Filter by account type|

#### Enumerated Values

|Parameter|Value|
|---|---|
|state|enabled|
|state|disabled|
|sort_by|current_profit|
|sort_by|profit|
|sort_by|bot_id|
|sort_by|pair|
|sort_by|created_at|
|sort_by|updated_at|
|sort_direction|desc|
|sort_direction|asc|

<h3 id="getver1gridbots-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Grid bots list (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1GridBotsIdMarketOrders

<a id="opIdgetVer1GridBotsIdMarketOrders"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/grid_bots/{id}/market_orders',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/grid_bots/{id}/market_orders`

Grid Bot Market Orders (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1gridbotsidmarketorders-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="getver1gridbotsidmarketorders-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Grid Bot Market Orders (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1GridBotsIdProfits

<a id="opIdgetVer1GridBotsIdProfits"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api.3commas.io/public/api/ver1/grid_bots/{id}/profits',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /ver1/grid_bots/{id}/profits`

Grid Bot Profits (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1gridbotsidprofits-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

> Example responses

> 200 Response

```json
{
  "grid_line_id": "'8000'",
  "profit": "'0.01'",
  "usd_profit": "'100'",
  "created_at": "2018-08-08 08:08:08",
  "grid_line": {
    "id": 21,
    "price": "'8000'",
    "side": "'SELL'",
    "order_placed": true
  }
}
```

<h3 id="getver1gridbotsidprofits-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Grid Bot Profits (Permission: BOTS_READ, Security: SIGNED)|[GridBotProfitsEntity](#schemagridbotprofitsentity)|

<aside class="success">
This operation does not require authentication
</aside>

## patchVer1GridBotsIdAi

<a id="opIdpatchVer1GridBotsIdAi"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.patch '/api.3commas.io/public/api/ver1/grid_bots/{id}/ai',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /ver1/grid_bots/{id}/ai`

Edit Grid Bot (AI) (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: GridBot
pair: string
total_quantity: 0
leverage_type: custom
leverage_custom_value: 0

```

<h3 id="patchver1gridbotsidai-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|
|body|body|object|false|none|
|» name|body|string|false|Grid Bot's name|
|» pair|body|string|true|none|
|» total_quantity|body|number(double)|true|none|
|» leverage_type|body|string|false|Leverage type for futures accounts|
|» leverage_custom_value|body|number(double)|false|Required if leverage_type = 'isolated'|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» leverage_type|custom|
|» leverage_type|cross|
|» leverage_type|not_specified|
|» leverage_type|isolated|

<h3 id="patchver1gridbotsidai-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Edit Grid Bot (AI) (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## patchVer1GridBotsIdManual

<a id="opIdpatchVer1GridBotsIdManual"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.patch '/api.3commas.io/public/api/ver1/grid_bots/{id}/manual',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /ver1/grid_bots/{id}/manual`

Edit Grid Bot (Manual) (Permission: BOTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: GridBot
pair: string
upper_price: 0
lower_price: 0
quantity_per_grid: 0
grids_quantity: 0
upper_stop_loss_price: 0
upper_stop_loss_enabled: true
upper_stop_loss_action: stop_bot
lower_stop_loss_price: 0
lower_stop_loss_enabled: true
lower_stop_loss_action: stop_bot
leverage_type: custom
leverage_custom_value: 0

```

<h3 id="patchver1gridbotsidmanual-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|
|body|body|object|false|none|
|» name|body|string|false|Grid Bot's name|
|» pair|body|string|true|none|
|» upper_price|body|number(double)|true|none|
|» lower_price|body|number(double)|true|none|
|» quantity_per_grid|body|number(double)|true|none|
|» grids_quantity|body|number(double)|true|none|
|» upper_stop_loss_price|body|number(double)|false|none|
|» upper_stop_loss_enabled|body|boolean|false|none|
|» upper_stop_loss_action|body|string|false|none|
|» lower_stop_loss_price|body|number(double)|false|none|
|» lower_stop_loss_enabled|body|boolean|false|none|
|» lower_stop_loss_action|body|string|false|none|
|» leverage_type|body|string|false|Leverage type for futures accounts|
|» leverage_custom_value|body|number(double)|false|Required if leverage_type = 'isolated'|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» upper_stop_loss_action|stop_bot|
|» upper_stop_loss_action|stop_bot_and_buy|
|» upper_stop_loss_action|stop_bot_and_sell|
|» upper_stop_loss_action|stop_bot_and_close_position|
|» lower_stop_loss_action|stop_bot|
|» lower_stop_loss_action|stop_bot_and_buy|
|» lower_stop_loss_action|stop_bot_and_sell|
|» lower_stop_loss_action|stop_bot_and_close_position|
|» leverage_type|custom|
|» leverage_type|cross|
|» leverage_type|not_specified|
|» leverage_type|isolated|

<h3 id="patchver1gridbotsidmanual-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Edit Grid Bot (Manual) (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1GridBotsId

<a id="opIdgetVer1GridBotsId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/grid_bots/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/grid_bots/{id}`

Show Grid Bot (Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1gridbotsid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="getver1gridbotsid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Show Grid Bot (Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteVer1GridBotsId

<a id="opIddeleteVer1GridBotsId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete '/api.3commas.io/public/api/ver1/grid_bots/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /ver1/grid_bots/{id}`

Delete Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="deletever1gridbotsid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="deletever1gridbotsid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Delete Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1GridBotsIdDisable

<a id="opIdpostVer1GridBotsIdDisable"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/grid_bots/{id}/disable',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/grid_bots/{id}/disable`

Disable Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1gridbotsiddisable-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="postver1gridbotsiddisable-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Disable Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1GridBotsIdEnable

<a id="opIdpostVer1GridBotsIdEnable"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/ver1/grid_bots/{id}/enable',
  params: {
  }

p JSON.parse(result)

```

`POST /ver1/grid_bots/{id}/enable`

Enable Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)

<h3 id="postver1gridbotsidenable-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="postver1gridbotsidenable-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Enable Grid Bot (Permission: BOTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1GridBotsIdRequiredBalances

<a id="opIdgetVer1GridBotsIdRequiredBalances"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/grid_bots/{id}/required_balances',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/grid_bots/{id}/required_balances`

Get required balances to start bot(Permission: BOTS_READ, Security: SIGNED)

<h3 id="getver1gridbotsidrequiredbalances-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="getver1gridbotsidrequiredbalances-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get required balances to start bot(Permission: BOTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-loose_accounts">loose_accounts</h1>

Operations about loose_accounts

## postVer1LooseAccounts

<a id="opIdpostVer1LooseAccounts"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/loose_accounts',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/loose_accounts`

Create Loose Account (Permission: ACCOUNTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: string
"tokens[code]":
  - string
"tokens[amount]":
  - 0

```

<h3 id="postver1looseaccounts-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» name|body|string|true|none|
|» tokens[code]|body|[string]|true|none|
|» tokens[amount]|body|[number]|true|none|

<h3 id="postver1looseaccounts-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create Loose Account (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getVer1LooseAccountsAvailableCurrencies

<a id="opIdgetVer1LooseAccountsAvailableCurrencies"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/loose_accounts/available_currencies',
  params: {
  }

p JSON.parse(result)

```

`GET /ver1/loose_accounts/available_currencies`

Available currencies (Permission: ACCOUNTS_READ, Security: SIGNED)

<h3 id="getver1looseaccountsavailablecurrencies-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|contains|query|string|false|none|
|limit|query|integer(int32)|false|none|
|offset|query|integer(int32)|false|none|

<h3 id="getver1looseaccountsavailablecurrencies-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Available currencies (Permission: ACCOUNTS_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## putVer1LooseAccountsAccountId

<a id="opIdputVer1LooseAccountsAccountId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.put '/api.3commas.io/public/api/ver1/loose_accounts/{account_id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PUT /ver1/loose_accounts/{account_id}`

Update Loose Account (Permission: ACCOUNTS_WRITE, Security: SIGNED)

> Body parameter

```yaml
name: string
"tokens[code]":
  - string
"tokens[amount]":
  - 0

```

<h3 id="putver1looseaccountsaccountid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|path|integer(int32)|true|none|
|body|body|object|false|none|
|» name|body|string|false|none|
|» tokens[code]|body|[string]|true|none|
|» tokens[amount]|body|[number]|true|none|

<h3 id="putver1looseaccountsaccountid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update Loose Account (Permission: ACCOUNTS_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-mini_apps">mini_apps</h1>

Operations about mini_apps

## getVer1MiniAppsStorage

<a id="opIdgetVer1MiniAppsStorage"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/ver1/mini_apps/storage',
  params: {
  'key' => 'string'
}

p JSON.parse(result)

```

`GET /ver1/mini_apps/storage`

Fetch data from storage (Security: SIGNED)

<h3 id="getver1miniappsstorage-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|key|query|string|true|none|

<h3 id="getver1miniappsstorage-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Fetch data from storage (Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postVer1MiniAppsStorage

<a id="opIdpostVer1MiniAppsStorage"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/ver1/mini_apps/storage',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /ver1/mini_apps/storage`

Write data into storage (Security: SIGNED)

> Body parameter

```yaml
key: string
data: null

```

<h3 id="postver1miniappsstorage-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» key|body|string|true|none|
|» data|body|json|true|none|

<h3 id="postver1miniappsstorage-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Write data into storage (Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-ping">ping</h1>

Operations about pings

## getVer1Ping

<a id="opIdgetVer1Ping"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api.3commas.io/public/api/ver1/ping',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /ver1/ping`

Test connectivity to the Rest API (Permission: NONE, Security: NONE)

> Example responses

> 200 Response

```json
{
  "pong": "'pong'"
}
```

<h3 id="getver1ping-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Test connectivity to the Rest API (Permission: NONE, Security: NONE)|[PongEntity](#schemapongentity)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-time">time</h1>

Operations about times

## getVer1Time

<a id="opIdgetVer1Time"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Accept' => 'application/json'
}

result = RestClient.get '/api.3commas.io/public/api/ver1/time',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`GET /ver1/time`

Test connectivity to the Rest API and get the current server time (Permission: NONE, Security: NONE)

> Example responses

> 200 Response

```json
{
  "server_time": "1592769067"
}
```

<h3 id="getver1time-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Test connectivity to the Rest API and get the current server time (Permission: NONE, Security: NONE)|[TimeEntity](#schematimeentity)|

<aside class="success">
This operation does not require authentication
</aside>

<h1 id="api-title-smart_trades_v2">smart_trades_v2</h1>

Operations about smart_trades_v2s

## getV2SmartTrades

<a id="opIdgetV2SmartTrades"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/v2/smart_trades',
  params: {
  }

p JSON.parse(result)

```

`GET /v2/smart_trades`

Get smart trade history (Permission: SMART_TRADE_READ, Security: SIGNED)

<h3 id="getv2smarttrades-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|account_id|query|integer(int32)|false|none|
|pair|query|string|false|none|
|type|query|string|false|none|
|page|query|integer(int32)|false|none|
|per_page|query|integer(int32)|false|none|
|status|query|string|false|none|
|order_by|query|string|false|none|
|order_direction|query|string|false|none|
|from|query|string|false|Param for a filter by created date|
|base|query|string|false|Base currency|
|quote|query|string|false|Quote currency|

#### Enumerated Values

|Parameter|Value|
|---|---|
|type|simple_buy|
|type|simple_sell|
|type|smart_sell|
|type|smart_trade|
|type|smart_cover|
|type|smart_buy|
|status|all|
|status|active|
|status|finished|
|status|successfully_finished|
|status|cancelled|
|status|failed|
|order_by|created_at|
|order_by|updated_at|
|order_by|closed_at|
|order_by|status|
|order_by|profit|
|order_by|profit_percentage|
|order_direction|asc|
|order_direction|desc|

<h3 id="getv2smarttrades-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get smart trade history (Permission: SMART_TRADE_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2SmartTrades

<a id="opIdpostV2SmartTrades"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/v2/smart_trades',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /v2/smart_trades`

Create smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

> Body parameter

```yaml
account_id: 0
pair: string
instant: false
skip_enter_step: false
note: string
"leverage[enabled]": false
"leverage[type]": custom
"leverage[value]": 0
"position[type]": buy
"position[order_type]": market
"position[units][value]": 0
"position[price][value]": 0
"position[conditional][price][value]": 0
"position[conditional][price][type]": bid
"position[conditional][order_type]": market
"position[conditional][trailing][enabled]": false
"position[conditional][trailing][percent]": 0
"take_profit[enabled]": false
"take_profit[steps][][order_type]":
  - market
"take_profit[steps][][volume]":
  - 0
"take_profit[steps][][price][type]":
  - bid
"take_profit[steps][][price][value]":
  - 0
"take_profit[steps][][price][percent]":
  - 0
"take_profit[steps][][trailing][enabled]": false
"take_profit[steps][][trailing][percent]":
  - 0
"stop_loss[enabled]": false
"stop_loss[breakeven]": false
"stop_loss[order_type]": market
"stop_loss[price][value]": 0
"stop_loss[conditional][price][type]": bid
"stop_loss[conditional][price][value]": 0
"stop_loss[conditional][price][percent]": 0
"stop_loss[conditional][trailing][enabled]": false
"stop_loss[timeout][enabled]": false
"stop_loss[timeout][value]": 0

```

<h3 id="postv2smarttrades-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|body|body|object|true|none|
|» account_id|body|integer(int32)|true|id from GET /ver1/accounts|
|» pair|body|string|true|none|
|» instant|body|boolean|false|true for Simple Buy and Simple Sell|
|» skip_enter_step|body|boolean|false|true only for Smart Sell|
|» note|body|string|false|none|
|» leverage[enabled]|body|boolean|true|none|
|» leverage[type]|body|string|false|none|
|» leverage[value]|body|integer(int32)|false|Cross leverage value|
|» position[type]|body|string|true|none|
|» position[order_type]|body|string|true|none|
|» position[units][value]|body|number(double)|true|Amount of units to buy|
|» position[price][value]|body|number(double)|true|Price for limit order|
|» position[conditional][price][value]|body|number(double)|true|Conditional trigger price|
|» position[conditional][price][type]|body|string|false|By default ask for long, bid for short|
|» position[conditional][order_type]|body|string|true|none|
|» position[conditional][trailing][enabled]|body|boolean|true|none|
|» position[conditional][trailing][percent]|body|number(float)|true|Should be 100% in the sum of all steps|
|» take_profit[enabled]|body|boolean|true|none|
|» take_profit[steps][][order_type]|body|[string]|true|market, limit|
|» take_profit[steps][][volume]|body|[number]|true|none|
|» take_profit[steps][][price][type]|body|[string]|true|bid, ask, last|
|» take_profit[steps][][price][value]|body|[number]|false|only if position has no trailing or position trailing is finished|
|» take_profit[steps][][price][percent]|body|[number]|false|only if position has trailing and position trailing is not finished|
|» take_profit[steps][][trailing][enabled]|body|[boolean]|true|none|
|» take_profit[steps][][trailing][percent]|body|[number]|true|none|
|» stop_loss[enabled]|body|boolean|true|none|
|» stop_loss[breakeven]|body|boolean|false|none|
|» stop_loss[order_type]|body|string|true|none|
|» stop_loss[price][value]|body|number(double)|true|Price for limit order|
|» stop_loss[conditional][price][type]|body|string|true|none|
|» stop_loss[conditional][price][value]|body|number(double)|false|if position has no trailing or position trailing is finished|
|» stop_loss[conditional][price][percent]|body|number(float)|false|only if position has trailing and position trailing is not finished|
|» stop_loss[conditional][trailing][enabled]|body|boolean|true|none|
|» stop_loss[timeout][enabled]|body|boolean|true|none|
|» stop_loss[timeout][value]|body|integer(int32)|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» leverage[type]|custom|
|» leverage[type]|cross|
|» leverage[type]|isolated|
|» position[type]|buy|
|» position[type]|sell|
|» position[order_type]|market|
|» position[order_type]|limit|
|» position[order_type]|conditional|
|» position[conditional][price][type]|bid|
|» position[conditional][price][type]|ask|
|» position[conditional][price][type]|last|
|» position[conditional][order_type]|market|
|» position[conditional][order_type]|limit|
|» take_profit[steps][][order_type]|market|
|» take_profit[steps][][order_type]|limit|
|» take_profit[steps][][price][type]|bid|
|» take_profit[steps][][price][type]|ask|
|» take_profit[steps][][price][type]|last|
|» stop_loss[order_type]|market|
|» stop_loss[order_type]|limit|
|» stop_loss[conditional][price][type]|bid|
|» stop_loss[conditional][price][type]|ask|
|» stop_loss[conditional][price][type]|last|

<h3 id="postv2smarttrades-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Create smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2SmartTradesId

<a id="opIdgetV2SmartTradesId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/v2/smart_trades/{id}',
  params: {
  }

p JSON.parse(result)

```

`GET /v2/smart_trades/{id}`

Get smart trade v2 by id (Permission: SMART_TRADE_READ, Security: SIGNED)

<h3 id="getv2smarttradesid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="getv2smarttradesid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get smart trade v2 by id (Permission: SMART_TRADE_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteV2SmartTradesId

<a id="opIddeleteV2SmartTradesId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete '/api.3commas.io/public/api/v2/smart_trades/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /v2/smart_trades/{id}`

Cancel smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

<h3 id="deletev2smarttradesid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="deletev2smarttradesid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Cancel smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## patchV2SmartTradesId

<a id="opIdpatchV2SmartTradesId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.patch '/api.3commas.io/public/api/v2/smart_trades/{id}',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`PATCH /v2/smart_trades/{id}`

Update smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

> Body parameter

```yaml
"leverage[enabled]": false
"leverage[type]": custom
"leverage[value]": 0
"position[units][value]": 0
"position[price][value]": 0
"position[conditional][price][value]": 0
"position[conditional][price][type]": bid
"position[conditional][order_type]": market
"position[conditional][trailing][enabled]": false
"position[conditional][trailing][percent]": 0
"take_profit[enabled]": false
"take_profit[steps][][order_type]":
  - market
"take_profit[steps][][volume]":
  - 0
"take_profit[steps][][price][type]":
  - bid
"take_profit[steps][][price][value]":
  - 0
"take_profit[steps][][price][percent]":
  - 0
"take_profit[steps][][trailing][enabled]": false
"take_profit[steps][][trailing][percent]":
  - 0
"stop_loss[enabled]": false
"stop_loss[breakeven]": false
"stop_loss[order_type]": market
"stop_loss[price][value]": 0
"stop_loss[conditional][price][type]": bid
"stop_loss[conditional][price][value]": 0
"stop_loss[conditional][price][percent]": 0
"stop_loss[conditional][trailing][enabled]": false
"stop_loss[timeout][enabled]": false
"stop_loss[timeout][value]": 0

```

<h3 id="patchv2smarttradesid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» leverage[enabled]|body|boolean|true|none|
|» leverage[type]|body|string|false|none|
|» leverage[value]|body|integer(int32)|false|Cross leverage value|
|» position[units][value]|body|number(double)|true|Amount of units to buy|
|» position[price][value]|body|number(double)|true|Price for limit order|
|» position[conditional][price][value]|body|number(double)|true|Conditional trigger price|
|» position[conditional][price][type]|body|string|false|By default ask for long, bid for short|
|» position[conditional][order_type]|body|string|true|none|
|» position[conditional][trailing][enabled]|body|boolean|true|none|
|» position[conditional][trailing][percent]|body|number(float)|true|none|
|» take_profit[enabled]|body|boolean|true|none|
|» take_profit[steps][][order_type]|body|[string]|true|none|
|» take_profit[steps][][volume]|body|[number]|true|none|
|» take_profit[steps][][price][type]|body|[string]|true|none|
|» take_profit[steps][][price][value]|body|[number]|false|none|
|» take_profit[steps][][price][percent]|body|[number]|false|none|
|» take_profit[steps][][trailing][enabled]|body|[boolean]|true|none|
|» take_profit[steps][][trailing][percent]|body|[number]|true|none|
|» stop_loss[enabled]|body|boolean|true|none|
|» stop_loss[breakeven]|body|boolean|false|none|
|» stop_loss[order_type]|body|string|true|none|
|» stop_loss[price][value]|body|number(double)|true|Price for limit order|
|» stop_loss[conditional][price][type]|body|string|true|none|
|» stop_loss[conditional][price][value]|body|number(double)|false|Trigger price|
|» stop_loss[conditional][price][percent]|body|number(float)|false|none|
|» stop_loss[conditional][trailing][enabled]|body|boolean|true|none|
|» stop_loss[timeout][enabled]|body|boolean|true|none|
|» stop_loss[timeout][value]|body|integer(int32)|true|none|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» leverage[type]|custom|
|» leverage[type]|cross|
|» leverage[type]|isolated|
|» position[conditional][price][type]|bid|
|» position[conditional][price][type]|ask|
|» position[conditional][price][type]|last|
|» position[conditional][order_type]|market|
|» position[conditional][order_type]|limit|
|» take_profit[steps][][order_type]|market|
|» take_profit[steps][][order_type]|limit|
|» take_profit[steps][][price][type]|bid|
|» take_profit[steps][][price][type]|ask|
|» take_profit[steps][][price][type]|last|
|» stop_loss[order_type]|market|
|» stop_loss[order_type]|limit|
|» stop_loss[conditional][price][type]|bid|
|» stop_loss[conditional][price][type]|ask|
|» stop_loss[conditional][price][type]|last|

<h3 id="patchv2smarttradesid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2SmartTradesIdReduceFunds

<a id="opIdpostV2SmartTradesIdReduceFunds"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/v2/smart_trades/{id}/reduce_funds',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /v2/smart_trades/{id}/reduce_funds`

Reduce funds for smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

> Body parameter

```yaml
order_type: market
"units[value]": 0
"price[value]": 0

```

<h3 id="postv2smarttradesidreducefunds-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» order_type|body|string|true|none|
|» units[value]|body|number(double)|true|Amount of units to buy|
|» price[value]|body|number(double)|true|Price for limit order|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» order_type|market|
|» order_type|limit|

<h3 id="postv2smarttradesidreducefunds-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Reduce funds for smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2SmartTradesIdAddFunds

<a id="opIdpostV2SmartTradesIdAddFunds"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/v2/smart_trades/{id}/add_funds',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /v2/smart_trades/{id}/add_funds`

Average for smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

> Body parameter

```yaml
order_type: market
"units[value]": 0
"price[value]": 0

```

<h3 id="postv2smarttradesidaddfunds-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» order_type|body|string|true|none|
|» units[value]|body|number(double)|true|Amount of units to buy|
|» price[value]|body|number(double)|true|Price for limit order|

#### Enumerated Values

|Parameter|Value|
|---|---|
|» order_type|market|
|» order_type|limit|

<h3 id="postv2smarttradesidaddfunds-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Average for smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2SmartTradesIdCloseByMarket

<a id="opIdpostV2SmartTradesIdCloseByMarket"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/v2/smart_trades/{id}/close_by_market',
  params: {
  }

p JSON.parse(result)

```

`POST /v2/smart_trades/{id}/close_by_market`

Close by market smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

<h3 id="postv2smarttradesidclosebymarket-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="postv2smarttradesidclosebymarket-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Close by market smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2SmartTradesIdForceStart

<a id="opIdpostV2SmartTradesIdForceStart"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/v2/smart_trades/{id}/force_start',
  params: {
  }

p JSON.parse(result)

```

`POST /v2/smart_trades/{id}/force_start`

Force start smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

<h3 id="postv2smarttradesidforcestart-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="postv2smarttradesidforcestart-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Force start smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2SmartTradesIdForceProcess

<a id="opIdpostV2SmartTradesIdForceProcess"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/v2/smart_trades/{id}/force_process',
  params: {
  }

p JSON.parse(result)

```

`POST /v2/smart_trades/{id}/force_process`

Process smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

<h3 id="postv2smarttradesidforceprocess-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|

<h3 id="postv2smarttradesidforceprocess-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Process smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2SmartTradesIdSetNote

<a id="opIdpostV2SmartTradesIdSetNote"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

headers = {
  'Content-Type' => 'application/x-www-form-urlencoded'
}

result = RestClient.post '/api.3commas.io/public/api/v2/smart_trades/{id}/set_note',
  params: {
  }, headers: headers

p JSON.parse(result)

```

`POST /v2/smart_trades/{id}/set_note`

Set note to smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)

> Body parameter

```yaml
note: string

```

<h3 id="postv2smarttradesidsetnote-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|id|path|integer(int32)|true|none|
|body|body|object|true|none|
|» note|body|string|true|none|

<h3 id="postv2smarttradesidsetnote-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Set note to smart trade v2 (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## getV2SmartTradesSmartTradeIdTrades

<a id="opIdgetV2SmartTradesSmartTradeIdTrades"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.get '/api.3commas.io/public/api/v2/smart_trades/{smart_trade_id}/trades',
  params: {
  }

p JSON.parse(result)

```

`GET /v2/smart_trades/{smart_trade_id}/trades`

Get smart trade v2 trades (Permission: SMART_TRADE_READ, Security: SIGNED)

<h3 id="getv2smarttradessmarttradeidtrades-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|smart_trade_id|path|integer(int32)|true|none|

<h3 id="getv2smarttradessmarttradeidtrades-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Get smart trade v2 trades (Permission: SMART_TRADE_READ, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## postV2SmartTradesSmartTradeIdTradesIdCloseByMarket

<a id="opIdpostV2SmartTradesSmartTradeIdTradesIdCloseByMarket"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.post '/api.3commas.io/public/api/v2/smart_trades/{smart_trade_id}/trades/{id}/close_by_market',
  params: {
  }

p JSON.parse(result)

```

`POST /v2/smart_trades/{smart_trade_id}/trades/{id}/close_by_market`

Panic close trade by market (Permission: SMART_TRADE_WRITE, Security: SIGNED)

<h3 id="postv2smarttradessmarttradeidtradesidclosebymarket-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|smart_trade_id|path|integer(int32)|true|none|
|id|path|integer(int32)|true|none|

<h3 id="postv2smarttradessmarttradeidtradesidclosebymarket-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Panic close trade by market (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

## deleteV2SmartTradesSmartTradeIdTradesId

<a id="opIddeleteV2SmartTradesSmartTradeIdTradesId"></a>

> Code samples

```ruby
require 'rest-client'
require 'json'

result = RestClient.delete '/api.3commas.io/public/api/v2/smart_trades/{smart_trade_id}/trades/{id}',
  params: {
  }

p JSON.parse(result)

```

`DELETE /v2/smart_trades/{smart_trade_id}/trades/{id}`

Cancel trade (Permission: SMART_TRADE_WRITE, Security: SIGNED)

<h3 id="deletev2smarttradessmarttradeidtradesid-parameters">Parameters</h3>

|Name|In|Type|Required|Description|
|---|---|---|---|---|
|smart_trade_id|path|integer(int32)|true|none|
|id|path|integer(int32)|true|none|

<h3 id="deletev2smarttradessmarttradeidtradesid-responses">Responses</h3>

|Status|Meaning|Description|Schema|
|---|---|---|---|
|204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Cancel trade (Permission: SMART_TRADE_WRITE, Security: SIGNED)|None|

<aside class="success">
This operation does not require authentication
</aside>

# Schemas

<h2 id="tocS_BotEntity">BotEntity</h2>
<!-- backwards compatibility -->
<a id="schemabotentity"></a>
<a id="schema_BotEntity"></a>
<a id="tocSbotentity"></a>
<a id="tocsbotentity"></a>

```json
{
  "id": 5,
  "account_id": 10,
  "is_enabled": true,
  "max_safety_orders": 5,
  "active_safety_orders_count": 2,
  "pairs": "['BTC_LTC', 'BTC_ETH', 'BTC_ADA']",
  "strategy_list": "[{'options'=>{'time'=>'5m', 'type'=>'buy_or_strong_buy'}, 'strategy'=>'trading_view'}, ...]",
  "max_active_deals": 2,
  "active_deals_count": 2,
  "deletable?": true,
  "created_at": "2018-08-08 08:08:08",
  "updated_at": "2018-08-10 10:10:10",
  "trailing_enabled": true,
  "tsl_enabled": true,
  "deal_start_delay_seconds": 60,
  "stop_loss_timeout_enabled": true,
  "stop_loss_timeout_in_seconds": 2,
  "disable_after_deals_count": 2,
  "deals_counter": 2,
  "allowed_deals_on_same_pair": 2,
  "easy_form_supported": true,
  "close_deals_timeout": 70,
  "url_secret": "string",
  "name": "'Test Bot'",
  "take_profit": "'1.5'",
  "base_order_volume": "'0.002'",
  "safety_order_volume": "'0.0015'",
  "safety_order_step_percentage": "'1.1'",
  "take_profit_type": "'base'",
  "type": "'Bot::SingleBot'",
  "martingale_volume_coefficient": "'1.3'",
  "martingale_step_coefficient": "'0.9'",
  "stop_loss_percentage": "'5.5'",
  "cooldown": "'200'",
  "btc_price_limit": "'30.15'",
  "strategy": "'long'",
  "min_volume_btc_24h": "'500.5'",
  "profit_currency": "'quote_currency'",
  "min_price": "'0.0245'",
  "max_price": "'0.0123'",
  "stop_loss_type": "'stop_loss'",
  "safety_order_volume_type": "'base_currency'",
  "base_order_volume_type": "'percent'",
  "account_name": "'My account'",
  "trailing_deviation": "0.14",
  "finished_deals_profit_usd": "12.14",
  "finished_deals_count": "252.1",
  "leverage_type": "'not_specified'",
  "leverage_custom_value": "'1'",
  "start_order_type": "'limit'",
  "active_deals_usd_profit": "200.21"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|account_id|integer(int32)|false|none|none|
|is_enabled|boolean|false|none|none|
|max_safety_orders|integer(int32)|false|none|none|
|active_safety_orders_count|integer(int32)|false|none|none|
|pairs|string|false|none|Format: [QUOTE_BASE, ...]|
|strategy_list|string|false|none|none|
|max_active_deals|integer(int32)|false|none|none|
|active_deals_count|integer(int32)|false|none|none|
|deletable?|boolean|false|none|none|
|created_at|string|false|none|none|
|updated_at|string|false|none|none|
|trailing_enabled|boolean|false|none|none|
|tsl_enabled|boolean|false|none|none|
|deal_start_delay_seconds|integer(int32)|false|none|Deal start delay in seconds|
|stop_loss_timeout_enabled|boolean|false|none|none|
|stop_loss_timeout_in_seconds|integer(int32)|false|none|none|
|disable_after_deals_count|integer(int32)|false|none|none|
|deals_counter|integer(int32)|false|none|none|
|allowed_deals_on_same_pair|integer(int32)|false|none|none|
|easy_form_supported|boolean|false|none|none|
|close_deals_timeout|integer(int32)|false|none|Close bot deals after given number of seconds|
|url_secret|string|false|none|none|
|name|string|false|none|none|
|take_profit|string|false|none|'Percentage'|
|base_order_volume|string|false|none|none|
|safety_order_volume|string|false|none|none|
|safety_order_step_percentage|string|false|none|none|
|take_profit_type|string|false|none|Values: base, total|
|type|string|false|none|Values: ["Bot::MultiBot", "Bot::SingleBot", "Bot::SwitchBot"]|
|martingale_volume_coefficient|string|false|none|none|
|martingale_step_coefficient|string|false|none|none|
|stop_loss_percentage|string|false|none|none|
|cooldown|string|false|none|none|
|btc_price_limit|string|false|none|none|
|strategy|string|false|none|Values: long, short|
|min_volume_btc_24h|string|false|none|none|
|profit_currency|string|false|none|Values: quote_currency, base_currency|
|min_price|string|false|none|none|
|max_price|string|false|none|none|
|stop_loss_type|string|false|none|Values: stop_loss, stop_loss_and_disable_bot|
|safety_order_volume_type|string|false|none|Values: quote_currency, base_currency, percent, xbt|
|base_order_volume_type|string|false|none|Values: quote_currency, base_currency, percent, xbt|
|account_name|string|false|none|none|
|trailing_deviation|string|false|none|none|
|finished_deals_profit_usd|string|false|none|none|
|finished_deals_count|string|false|none|none|
|leverage_type|string|false|none|Values: cross, not_specified, isolated|
|leverage_custom_value|string|false|none|none|
|start_order_type|string|false|none|Values: limit, market|
|active_deals_usd_profit|string|false|none|Sum of active deals profits|

<h2 id="tocS_AccountEntity">AccountEntity</h2>
<!-- backwards compatibility -->
<a id="schemaaccountentity"></a>
<a id="schema_AccountEntity"></a>
<a id="tocSaccountentity"></a>
<a id="tocsaccountentity"></a>

```json
{
  "id": 12,
  "auto_balance_period": 12,
  "auto_balance_portfolio_id": 452,
  "auto_balance_portfolio": {
    "name": "string",
    "id": "string",
    "created_at": "string",
    "portfolio_entries": {
      "target_percentage": "string",
      "currency_code": "string"
    }
  },
  "auto_balance_currency_change_limit": 5,
  "autobalance_enabled": true,
  "hedge_mode_available": true,
  "hedge_mode_enabled": true,
  "is_locked": true,
  "smart_trading_supported": true,
  "smart_selling_supported": true,
  "available_for_trading": true,
  "stats_supported": true,
  "trading_supported": true,
  "market_buy_supported": true,
  "market_sell_supported": true,
  "conditional_buy_supported": true,
  "bots_allowed": "false",
  "bots_ttp_allowed": "false",
  "bots_tsl_allowed": "false",
  "gordon_bots_available": "false",
  "multi_bots_allowed": "false",
  "created_at": "2018-08-08 08:08:08",
  "updated_at": "2018-08-22 02:25:08",
  "last_auto_balance": "2018-08-21 08:08:08",
  "fast_convert_available": true,
  "grid_bots_allowed": true,
  "api_key_invalid": true,
  "deposit_enabled": "false",
  "supported_market_types": "string",
  "api_key": "''",
  "name": "'Binance 2 '",
  "auto_balance_method": "'time'",
  "auto_balance_error": "'Failed to autobalance'",
  "customer_id": "string",
  "subaccount_name": "string",
  "lock_reason": "'API key is invalid'",
  "btc_amount": "'0.01134219'",
  "usd_amount": "'70.93146245'",
  "day_profit_btc": "'-0.00006'",
  "day_profit_usd": "'-0.02147'",
  "day_profit_btc_percentage": "'-0.26'",
  "day_profit_usd_percentage": "'-1.23'",
  "btc_profit": "'0.0001625'",
  "usd_profit": "'5.05764787'",
  "usd_profit_percentage": "'6.25'",
  "btc_profit_percentage": "'2.36'",
  "total_btc_profit": "'0.0012456'",
  "total_usd_profit": "'6.123181'",
  "pretty_display_type": "'BittrexAccount'",
  "exchange_name": "'Binance Futures'",
  "market_code": "'deribit_testnet'",
  "address": "'0xe00000dded00bbb08725d77777777ff070aa7aa7'"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|auto_balance_period|integer(int32)|false|none|none|
|auto_balance_portfolio_id|integer(int32)|false|none|none|
|auto_balance_portfolio|[PortfolioEntity](#schemaportfolioentity)|false|none|none|
|auto_balance_currency_change_limit|integer(int32)|false|none|none|
|autobalance_enabled|boolean|false|none|none|
|hedge_mode_available|boolean|false|none|none|
|hedge_mode_enabled|boolean|false|none|none|
|is_locked|boolean|false|none|none|
|smart_trading_supported|boolean|false|none|none|
|smart_selling_supported|boolean|false|none|DEPRECATED. use smart_trading_supported instead|
|available_for_trading|boolean|false|none|none|
|stats_supported|boolean|false|none|none|
|trading_supported|boolean|false|none|none|
|market_buy_supported|boolean|false|none|none|
|market_sell_supported|boolean|false|none|none|
|conditional_buy_supported|boolean|false|none|none|
|bots_allowed|boolean|false|none|none|
|bots_ttp_allowed|boolean|false|none|none|
|bots_tsl_allowed|boolean|false|none|none|
|gordon_bots_available|boolean|false|none|none|
|multi_bots_allowed|boolean|false|none|none|
|created_at|string|false|none|none|
|updated_at|string|false|none|none|
|last_auto_balance|string|false|none|none|
|fast_convert_available|boolean|false|none|Sell all to USD/BTC possibility|
|grid_bots_allowed|boolean|false|none|none|
|api_key_invalid|boolean|false|none|none|
|deposit_enabled|boolean|false|none|none|
|supported_market_types|string|false|none|none|
|api_key|string|false|none|none|
|name|string|false|none|none|
|auto_balance_method|integer(int32)|false|none|Values: time, currency_change|
|auto_balance_error|string|false|none|none|
|customer_id|string|false|none|none|
|subaccount_name|string|false|none|none|
|lock_reason|string|false|none|none|
|btc_amount|string|false|none|none|
|usd_amount|string|false|none|none|
|day_profit_btc|string|false|none|none|
|day_profit_usd|string|false|none|none|
|day_profit_btc_percentage|string|false|none|none|
|day_profit_usd_percentage|string|false|none|none|
|btc_profit|string|false|none|Month period|
|usd_profit|string|false|none|Month period|
|usd_profit_percentage|string|false|none|Month period|
|btc_profit_percentage|string|false|none|Month period|
|total_btc_profit|string|false|none|none|
|total_usd_profit|string|false|none|none|
|pretty_display_type|string|false|none|none|
|exchange_name|string|false|none|none|
|market_code|string|false|none|none|
|address|string|false|none|none|

<h2 id="tocS_PortfolioEntity">PortfolioEntity</h2>
<!-- backwards compatibility -->
<a id="schemaportfolioentity"></a>
<a id="schema_PortfolioEntity"></a>
<a id="tocSportfolioentity"></a>
<a id="tocsportfolioentity"></a>

```json
{
  "name": "string",
  "id": "string",
  "created_at": "string",
  "portfolio_entries": {
    "target_percentage": "string",
    "currency_code": "string"
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|name|string|false|none|none|
|id|string|false|none|none|
|created_at|string|false|none|none|
|portfolio_entries|[PortfolioEntryEntity](#schemaportfolioentryentity)|false|none|none|

<h2 id="tocS_PortfolioEntryEntity">PortfolioEntryEntity</h2>
<!-- backwards compatibility -->
<a id="schemaportfolioentryentity"></a>
<a id="schema_PortfolioEntryEntity"></a>
<a id="tocSportfolioentryentity"></a>
<a id="tocsportfolioentryentity"></a>

```json
{
  "target_percentage": "string",
  "currency_code": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|target_percentage|string|false|none|none|
|currency_code|string|false|none|none|

<h2 id="tocS_GridBotEntity">GridBotEntity</h2>
<!-- backwards compatibility -->
<a id="schemagridbotentity"></a>
<a id="schema_GridBotEntity"></a>
<a id="tocSgridbotentity"></a>
<a id="tocsgridbotentity"></a>

```json
{
  "id": 5,
  "account_id": 10,
  "account_name": "'My account'",
  "is_enabled": true,
  "grids_quantity": "'20'",
  "created_at": "2018-08-08 08:08:08",
  "updated_at": "2018-08-10 10:10:10",
  "strategy_type": "'manual'",
  "upper_stop_loss_enabled": true,
  "lower_stop_loss_enabled": true,
  "lower_price": "'8000'",
  "lower_stop_loss_price": "'7500'",
  "lower_stop_loss_action": "'stop_bot'",
  "upper_price": "'10000'",
  "upper_stop_loss_price": "'12000'",
  "upper_stop_loss_action": "'stop_bot'",
  "quantity_per_grid": "'100'",
  "leverage_type": "'isolated'",
  "leverage_custom_value": "'20.1'",
  "name": "'GridBot1'",
  "pair": "'BTC_ETH'",
  "start_price": "'9000'",
  "grid_price_step": "'100'",
  "current_profit": "100",
  "current_profit_usd": "1000",
  "total_profits_count": "10",
  "bought_volume": "1000",
  "sold_volume": "1000",
  "profit_percentage": "0.1",
  "current_price": "100.1",
  "investment_base_currency": "100",
  "investment_quote_currency": "100",
  "grid_lines": {
    "id": 21,
    "price": "'8000'",
    "side": "'SELL'",
    "order_placed": true
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|account_id|integer(int32)|false|none|none|
|account_name|string|false|none|none|
|is_enabled|boolean|false|none|none|
|grids_quantity|string|false|none|none|
|created_at|string|false|none|none|
|updated_at|string|false|none|none|
|strategy_type|string|false|none|none|
|upper_stop_loss_enabled|boolean|false|none|none|
|lower_stop_loss_enabled|boolean|false|none|none|
|lower_price|string|false|none|none|
|lower_stop_loss_price|string|false|none|none|
|lower_stop_loss_action|string|false|none|none|
|upper_price|string|false|none|none|
|upper_stop_loss_price|string|false|none|none|
|upper_stop_loss_action|string|false|none|none|
|quantity_per_grid|string|false|none|none|
|leverage_type|string|false|none|none|
|leverage_custom_value|string|false|none|none|
|name|string|false|none|none|
|pair|string|false|none|none|
|start_price|string|false|none|none|
|grid_price_step|string|false|none|none|
|current_profit|string|false|none|none|
|current_profit_usd|string|false|none|none|
|total_profits_count|string|false|none|none|
|bought_volume|string|false|none|none|
|sold_volume|string|false|none|none|
|profit_percentage|string|false|none|none|
|current_price|string|false|none|none|
|investment_base_currency|string|false|none|none|
|investment_quote_currency|string|false|none|none|
|grid_lines|[GridLineEntity](#schemagridlineentity)|false|none|none|

<h2 id="tocS_GridLineEntity">GridLineEntity</h2>
<!-- backwards compatibility -->
<a id="schemagridlineentity"></a>
<a id="schema_GridLineEntity"></a>
<a id="tocSgridlineentity"></a>
<a id="tocsgridlineentity"></a>

```json
{
  "id": 21,
  "price": "'8000'",
  "side": "'SELL'",
  "order_placed": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|Uniq id|
|price|string|false|none|none|
|side|string|false|none|none|
|order_placed|boolean|false|none|none|

<h2 id="tocS_GridBotProfitsEntity">GridBotProfitsEntity</h2>
<!-- backwards compatibility -->
<a id="schemagridbotprofitsentity"></a>
<a id="schema_GridBotProfitsEntity"></a>
<a id="tocSgridbotprofitsentity"></a>
<a id="tocsgridbotprofitsentity"></a>

```json
{
  "grid_line_id": "'8000'",
  "profit": "'0.01'",
  "usd_profit": "'100'",
  "created_at": "2018-08-08 08:08:08",
  "grid_line": {
    "id": 21,
    "price": "'8000'",
    "side": "'SELL'",
    "order_placed": true
  }
}

```

GridBotProfitsEntity model

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|grid_line_id|integer(int32)|false|none|none|
|profit|string|false|none|none|
|usd_profit|string|false|none|none|
|created_at|string|false|none|none|
|grid_line|[GridLineEntity](#schemagridlineentity)|false|none|none|

<h2 id="tocS_MarketplacePresets_IndexEntity">MarketplacePresets_IndexEntity</h2>
<!-- backwards compatibility -->
<a id="schemamarketplacepresets_indexentity"></a>
<a id="schema_MarketplacePresets_IndexEntity"></a>
<a id="tocSmarketplacepresets_indexentity"></a>
<a id="tocsmarketplacepresets_indexentity"></a>

```json
{
  "bots": [
    {
      "id": 0,
      "type": "string",
      "name": "string",
      "strategy": "string",
      "secret": "string",
      "marketplace_item": {
        "id": 0,
        "name": "string",
        "icon_url": "string"
      },
      "profit": {
        "period": "string",
        "amount": 0,
        "chart_data": [
          0
        ]
      },
      "currencies": [
        "string"
      ],
      "copies": 0,
      "is_favorite": true
    }
  ],
  "total": 0,
  "page": 0
}

```

MarketplacePresets_IndexEntity model

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|bots|[[MarketplacePresets_IndexEntity_MarketplaceBotEntity](#schemamarketplacepresets_indexentity_marketplacebotentity)]|false|none|none|
|total|integer(int32)|false|none|none|
|page|integer(int32)|false|none|none|

<h2 id="tocS_MarketplacePresets_IndexEntity_MarketplaceBotEntity">MarketplacePresets_IndexEntity_MarketplaceBotEntity</h2>
<!-- backwards compatibility -->
<a id="schemamarketplacepresets_indexentity_marketplacebotentity"></a>
<a id="schema_MarketplacePresets_IndexEntity_MarketplaceBotEntity"></a>
<a id="tocSmarketplacepresets_indexentity_marketplacebotentity"></a>
<a id="tocsmarketplacepresets_indexentity_marketplacebotentity"></a>

```json
{
  "id": 0,
  "type": "string",
  "name": "string",
  "strategy": "string",
  "secret": "string",
  "marketplace_item": {
    "id": 0,
    "name": "string",
    "icon_url": "string"
  },
  "profit": {
    "period": "string",
    "amount": 0,
    "chart_data": [
      0
    ]
  },
  "currencies": [
    "string"
  ],
  "copies": 0,
  "is_favorite": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|type|string|false|none|none|
|name|string|false|none|none|
|strategy|string|false|none|none|
|secret|string|false|none|none|
|marketplace_item|[MarketplacePresets_IndexEntity_MarketplaceBotEntity_MarketplaceItem](#schemamarketplacepresets_indexentity_marketplacebotentity_marketplaceitem)|false|none|none|
|profit|[MarketplacePresets_IndexEntity_MarketplaceBotEntity_Profit](#schemamarketplacepresets_indexentity_marketplacebotentity_profit)|false|none|none|
|currencies|[string]|false|none|none|
|copies|integer(int32)|false|none|Bot's copies count|
|is_favorite|boolean|false|none|none|

<h2 id="tocS_MarketplacePresets_IndexEntity_MarketplaceBotEntity_MarketplaceItem">MarketplacePresets_IndexEntity_MarketplaceBotEntity_MarketplaceItem</h2>
<!-- backwards compatibility -->
<a id="schemamarketplacepresets_indexentity_marketplacebotentity_marketplaceitem"></a>
<a id="schema_MarketplacePresets_IndexEntity_MarketplaceBotEntity_MarketplaceItem"></a>
<a id="tocSmarketplacepresets_indexentity_marketplacebotentity_marketplaceitem"></a>
<a id="tocsmarketplacepresets_indexentity_marketplacebotentity_marketplaceitem"></a>

```json
{
  "id": 0,
  "name": "string",
  "icon_url": "string"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer(int32)|false|none|none|
|name|string|false|none|none|
|icon_url|string|false|none|none|

<h2 id="tocS_MarketplacePresets_IndexEntity_MarketplaceBotEntity_Profit">MarketplacePresets_IndexEntity_MarketplaceBotEntity_Profit</h2>
<!-- backwards compatibility -->
<a id="schemamarketplacepresets_indexentity_marketplacebotentity_profit"></a>
<a id="schema_MarketplacePresets_IndexEntity_MarketplaceBotEntity_Profit"></a>
<a id="tocSmarketplacepresets_indexentity_marketplacebotentity_profit"></a>
<a id="tocsmarketplacepresets_indexentity_marketplacebotentity_profit"></a>

```json
{
  "period": "string",
  "amount": 0,
  "chart_data": [
    0
  ]
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|period|string|false|none|none|
|amount|number(double)|false|none|none|
|chart_data|[number]|false|none|none|

<h2 id="tocS_PongEntity">PongEntity</h2>
<!-- backwards compatibility -->
<a id="schemapongentity"></a>
<a id="schema_PongEntity"></a>
<a id="tocSpongentity"></a>
<a id="tocspongentity"></a>

```json
{
  "pong": "'pong'"
}

```

PongEntity model

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|pong|string|false|none|none|

<h2 id="tocS_TimeEntity">TimeEntity</h2>
<!-- backwards compatibility -->
<a id="schematimeentity"></a>
<a id="schema_TimeEntity"></a>
<a id="tocStimeentity"></a>
<a id="tocstimeentity"></a>

```json
{
  "server_time": "1592769067"
}

```

TimeEntity model

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|server_time|integer(int32)|false|none|UNIX timestamp|

<h2 id="tocS_DealEntity">DealEntity</h2>
<!-- backwards compatibility -->
<a id="schemadealentity"></a>
<a id="schema_DealEntity"></a>
<a id="tocSdealentity"></a>
<a id="tocsdealentity"></a>

```json
{
  "id": 1,
  "type": "Deal::ShortDeal",
  "bot_id": 111,
  "max_safety_orders": 2,
  "deal_has_error": true,
  "from_currency_id": 5,
  "to_currency_id": 10,
  "account_id": 121,
  "active_safety_orders_count": 1,
  "created_at": "2018-08-08 08:08:08",
  "updated_at": "2018-09-09 09:09:09",
  "closed_at": "2018-10-10 10:10:10",
  "finished?": true,
  "current_active_safety_orders_count": 1,
  "current_active_safety_orders": 1,
  "completed_safety_orders_count": 2,
  "completed_manual_safety_orders_count": 2,
  "cancellable?": true,
  "panic_sellable?": true,
  "trailing_enabled": true,
  "tsl_enabled": true,
  "stop_loss_timeout_enabled": true,
  "stop_loss_timeout_in_seconds": 2,
  "active_manual_safety_orders": 2,
  "pair": "'BTC_ADA'",
  "status": "'failed'",
  "localized_status": "string",
  "take_profit": "'1.23'",
  "base_order_volume": "'0.001'",
  "safety_order_volume": "'0.0015'",
  "safety_order_step_percentage": "'1.11'",
  "leverage_type": "'isolated'",
  "leverage_custom_value": "'20.1'",
  "bought_amount": "'1.5'",
  "bought_volume": "'150'",
  "bought_average_price": "'100'",
  "base_order_average_price": "'100'",
  "sold_amount": "'1.5'",
  "sold_volume": "'150'",
  "sold_average_price": "'100'",
  "take_profit_type": "'base'",
  "final_profit": "'-0.00051'",
  "martingale_coefficient": "'1.2'",
  "martingale_volume_coefficient": "'1.0'",
  "martingale_step_coefficient": "'1.0'",
  "stop_loss_percentage": "'3.6'",
  "error_message": "'Error placing base order'",
  "profit_currency": "'quote_currency'",
  "stop_loss_type": "'stop_loss'",
  "safety_order_volume_type": "'quote_currency'",
  "base_order_volume_type": "'base_currency,'",
  "from_currency": "'BTC'",
  "to_currency": "'ADA'",
  "current_price": "'102'",
  "take_profit_price": "'105'",
  "stop_loss_price": "'95.3'",
  "final_profit_percentage": "'4.2'",
  "actual_profit_percentage": "'3.4'",
  "bot_name": "My bot",
  "account_name": "My Account",
  "usd_final_profit": "'3.3523452'",
  "actual_profit": "'0.0023'",
  "actual_usd_profit": "'0.0023'",
  "failed_message": "Failed",
  "reserved_base_coin": "1.3423523",
  "reserved_second_coin": "0.1412454",
  "trailing_deviation": "0.14",
  "trailing_max_price": "0.1412454",
  "tsl_max_price": "0.1412454",
  "strategy": "'short'",
  "reserved_quote_funds": 0,
  "reserved_base_funds": 0
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|none|
|type|string¦null|false|none|none|
|bot_id|integer|false|none|none|
|max_safety_orders|integer|false|none|none|
|deal_has_error|boolean|false|none|none|
|from_currency_id|integer|false|none|DEPRECATED|
|to_currency_id|integer|false|none|DEPRECATED|
|account_id|integer|false|none|none|
|active_safety_orders_count|integer|false|none|none|
|created_at|string|false|none|none|
|updated_at|string|false|none|none|
|closed_at|string¦null|false|none|none|
|finished?|boolean|false|none|none|
|current_active_safety_orders_count|integer|false|none|none|
|current_active_safety_orders|integer|false|none|DEPRECATED|
|completed_safety_orders_count|integer|false|none|completed safeties (not including manual)|
|completed_manual_safety_orders_count|integer|false|none|completed manual safeties|
|cancellable?|boolean|false|none|none|
|panic_sellable?|boolean|false|none|none|
|trailing_enabled|boolean¦null|false|none|none|
|tsl_enabled|boolean|false|none|none|
|stop_loss_timeout_enabled|boolean|false|none|none|
|stop_loss_timeout_in_seconds|integer|false|none|none|
|active_manual_safety_orders|integer|false|none|none|
|pair|string|false|none|Format: QUOTE_BASE|
|status|string|false|none|Values: created, base_order_placed, bought, cancelled, completed, failed, panic_sell_pending, panic_sell_order_placed, panic_sold, cancel_pending, stop_loss_pending, stop_loss_finished, stop_loss_order_placed, switched, switched_take_profit, ttp_activated, ttp_order_placed, liquidated, bought_safety_pending, bought_take_profit_pending, settled|
|localized_status|string|false|none|none|
|take_profit|string¦null|false|none|Percentage|
|base_order_volume|string¦null|false|none|none|
|safety_order_volume|string¦null|false|none|none|
|safety_order_step_percentage|string|false|none|none|
|leverage_type|string|false|none|none|
|leverage_custom_value|string¦null|false|none|none|
|bought_amount|string¦null|false|none|none|
|bought_volume|string¦null|false|none|none|
|bought_average_price|string|false|none|none|
|base_order_average_price|string¦null|false|none|none|
|sold_amount|string¦null|false|none|none|
|sold_volume|string¦null|false|none|none|
|sold_average_price|string¦null|false|none|none|
|take_profit_type|string|false|none|Values: base, total|
|final_profit|string|false|none|none|
|martingale_coefficient|string|false|none|Percentage|
|martingale_volume_coefficient|string|false|none|Percentage|
|martingale_step_coefficient|string|false|none|Percentage|
|stop_loss_percentage|string¦null|false|none|none|
|error_message|string¦null|false|none|none|
|profit_currency|string|false|none|Values: quote_currency, base_currency|
|stop_loss_type|string|false|none|Values: stop_loss, stop_loss_and_disable_bot|
|safety_order_volume_type|string|false|none|Values: quote_currency, base_currency, percent, xbt|
|base_order_volume_type|string|false|none|Values: quote_currency, base_currency, percent, xbt|
|from_currency|string|false|none|none|
|to_currency|string|false|none|none|
|current_price|string|false|none|none|
|take_profit_price|string|false|none|none|
|stop_loss_price|string¦null|false|none|none|
|final_profit_percentage|string|false|none|none|
|actual_profit_percentage|string|false|none|none|
|bot_name|string|false|none|none|
|account_name|string|false|none|none|
|usd_final_profit|string|false|none|none|
|actual_profit|string|false|none|none|
|actual_usd_profit|string|false|none|none|
|failed_message|string¦null|false|none|none|
|reserved_base_coin|string|false|none|none|
|reserved_second_coin|string|false|none|none|
|trailing_deviation|string¦null|false|none|none|
|trailing_max_price|string¦null|false|none|Highest price met in case of long deal, lowest price otherwise|
|tsl_max_price|string¦null|false|none|Highest price met in TSL in case of long deal, lowest price otherwise|
|strategy|string|false|none|short or long|
|reserved_quote_funds|number¦null|false|none|Sum of reserved in active deals funds in QUOTE|
|reserved_base_funds|number¦null|false|none|Sum of reserved in active deals funds in BASE|

<h2 id="tocS_SmartTradeV2Entity">SmartTradeV2Entity</h2>
<!-- backwards compatibility -->
<a id="schemasmarttradev2entity"></a>
<a id="schema_SmartTradeV2Entity"></a>
<a id="tocSsmarttradev2entity"></a>
<a id="tocssmarttradev2entity"></a>

```json
{
  "id": 0,
  "version": 0,
  "account": {
    "id": 0,
    "type": "string",
    "name": "string",
    "market": "string",
    "link": "string"
  },
  "pair": "string",
  "instant": true,
  "status": {
    "type": "string",
    "title": "string"
  },
  "leverage": {
    "enabled": true,
    "type": "string",
    "value": 0
  },
  "position": {
    "type": "string",
    "editable": true,
    "units": {
      "value": 1231.11,
      "editable": true
    },
    "price": {
      "value": 1223.32,
      "value_without_commission": 500.2,
      "editable": true
    },
    "total": {
      "value": 100.2
    },
    "order_type": "string",
    "status": {
      "type": "string",
      "title": "string"
    }
  },
  "take_profit": {
    "enabled": true,
    "steps": [
      {
        "id": 0,
        "version": 0,
        "account": {
          "id": 0,
          "type": "string",
          "name": "string",
          "market": "string",
          "link": "string"
        },
        "pair": "string",
        "instant": true,
        "status": {
          "type": "string",
          "title": "string"
        },
        "leverage": {
          "enabled": true,
          "type": "string",
          "value": 0
        },
        "position": {
          "type": "string",
          "editable": true,
          "units": {
            "value": 1231.11,
            "editable": true
          },
          "price": {
            "value": 1223.32,
            "value_without_commission": 500.2,
            "editable": true
          },
          "total": {
            "value": 100.2
          },
          "order_type": "string",
          "status": {
            "type": "string",
            "title": "string"
          }
        },
        "take_profit": {
          "enabled": true,
          "steps": [
            {}
          ]
        },
        "stop_loss": {
          "enabled": true
        },
        "note": "string",
        "skip_enter_step": true,
        "data": {
          "editable": true,
          "current_price": {
            "quote_volume": "string",
            "last": "string"
          },
          "target_price_type": "string",
          "base_order_finished": true,
          "missing_funds_to_close": 0,
          "liquidation_price": 1000.22,
          "average_enter_price": 60.2,
          "average_close_price": 60.2,
          "average_enter_price_without_commission": 100.3,
          "average_close_price_without_commission": 40.2,
          "panic_sell_available": true,
          "add_funds_available": true,
          "force_start_available": true,
          "force_process_available": true,
          "cancel_available": true,
          "finished": true,
          "base_position_step_finished": true,
          "created_at": "2018-08-08 08:08:08",
          "updated_at": "2018-08-08 08:08:08",
          "closed_at": "2018-08-08 08:08:08",
          "type": "smart_sell"
        },
        "profit": {
          "volume": 14,
          "usd": 12.22,
          "percent": 12,
          "roe": 0
        },
        "margin": {
          "amount": 100.2,
          "total": 700.2
        },
        "is_position_not_filled": true
      }
    ]
  },
  "stop_loss": {
    "enabled": true
  },
  "reduce_funds": {
    "steps": [
      {
        "id": 0,
        "type": "string",
        "status": {
          "type": "string",
          "title": "string",
          "basic_type": "string"
        },
        "units": {
          "value": "string"
        },
        "price": {
          "value": "string",
          "value_without_commission": "string"
        },
        "total": {
          "value": "string"
        },
        "filled": {
          "units": "string",
          "total": "string",
          "price": "string",
          "value": "string"
        },
        "data": {
          "cancelable": true,
          "panic_sell_available": true
        }
      }
    ]
  },
  "market_close": {
    "id": 0,
    "type": "string",
    "status": {
      "type": "string",
      "title": "string",
      "basic_type": "string"
    },
    "units": {
      "value": "string"
    },
    "price": {
      "value": "string",
      "value_without_commission": "string"
    },
    "total": {
      "value": "string"
    },
    "filled": {
      "units": "string",
      "total": "string",
      "price": "string",
      "value": "string"
    }
  },
  "note": "string",
  "note_raw": "string",
  "skip_enter_step": true,
  "data": {
    "editable": true,
    "current_price": {
      "quote_volume": "string",
      "last": "string"
    },
    "target_price_type": "string",
    "base_order_finished": true,
    "missing_funds_to_close": 0,
    "liquidation_price": 1000.22,
    "average_enter_price": 60.2,
    "average_close_price": 60.2,
    "average_enter_price_without_commission": 100.3,
    "average_close_price_without_commission": 40.2,
    "panic_sell_available": true,
    "add_funds_available": true,
    "force_start_available": true,
    "force_process_available": true,
    "cancel_available": true,
    "finished": true,
    "base_position_step_finished": true,
    "created_at": "2018-08-08 08:08:08",
    "updated_at": "2018-08-08 08:08:08",
    "closed_at": "2018-08-08 08:08:08",
    "type": "smart_sell"
  },
  "profit": {
    "volume": 14,
    "usd": 12.22,
    "percent": 12,
    "roe": 0
  },
  "margin": {
    "amount": 100.2,
    "total": 700.2
  },
  "is_position_not_filled": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|none|
|version|integer|false|none|none|
|account|object|false|none|none|
|» id|integer|false|none|none|
|» type|string|false|none|none|
|» name|string|false|none|none|
|» market|string|false|none|none|
|» link|string|false|none|none|
|pair|string|false|none|none|
|instant|boolean|false|none|none|
|status|object|false|none|none|
|» type|string|false|none|none|
|» title|string|false|none|none|
|leverage|object|false|none|none|
|» enabled|boolean|false|none|none|
|» type|string|false|none|none|
|» value|integer|false|none|none|
|position|object|false|none|none|
|» type|string|false|none|none|
|» editable|boolean|false|none|none|
|» units|object|false|none|none|
|»» value|string¦null|false|none|none|
|»» editable|boolean|false|none|none|
|» price|object|false|none|none|
|»» value|number¦null|false|none|none|
|»» value_without_commission|number¦null|false|none|none|
|»» editable|boolean|false|none|none|
|» total|object|false|none|none|
|»» value|number¦null|false|none|none|
|» order_type|string|false|none|none|
|» status|object|false|none|none|
|»» type|string|false|none|none|
|»» title|string|false|none|none|
|take_profit|object|false|none|none|
|» enabled|boolean|false|none|none|
|» steps|[[TakeProfitStep](#schematakeprofitstep)]|false|none|none|
|stop_loss|object|false|none|none|
|» enabled|boolean|false|none|none|
|reduce_funds|object|false|none|none|
|» steps|[[ReduceFundsStep](#schemareducefundsstep)]|false|none|none|
|market_close|object|false|none|none|
|» id|integer|false|none|none|
|» type|string|false|none|none|
|» status|object|false|none|none|
|»» type|string|false|none|none|
|»» title|string|false|none|none|
|»» basic_type|string|false|none|none|
|» units|object|false|none|none|
|»» value|string|false|none|none|
|» price|object|false|none|none|
|»» value|string|false|none|none|
|»» value_without_commission|string|false|none|none|
|» total|object|false|none|none|
|»» value|string|false|none|none|
|» filled|object|false|none|none|
|»» units|string|false|none|none|
|»» total|string|false|none|none|
|»» price|string|false|none|none|
|»» value|string|false|none|none|
|note|string|false|none|none|
|note_raw|string¦null|false|none|none|
|skip_enter_step|boolean|false|none|none|
|data|object|false|none|none|
|» editable|boolean|false|none|none|
|» current_price|object|false|none|none|
|»» quote_volume|string|false|none|none|
|»» last|string|false|none|none|
|» target_price_type|string|false|none|none|
|» base_order_finished|boolean|false|none|none|
|» missing_funds_to_close|number|false|none|none|
|» liquidation_price|number¦null|false|none|none|
|» average_enter_price|number¦null|false|none|none|
|» average_close_price|number¦null|false|none|none|
|» average_enter_price_without_commission|number¦null|false|none|none|
|» average_close_price_without_commission|number¦null|false|none|none|
|» panic_sell_available|boolean|false|none|none|
|» add_funds_available|boolean|false|none|none|
|» force_start_available|boolean|false|none|none|
|» force_process_available|boolean|false|none|none|
|» cancel_available|boolean|false|none|none|
|» finished|boolean|false|none|none|
|» base_position_step_finished|boolean|false|none|none|
|» created_at|string|false|none|none|
|» updated_at|string|false|none|none|
|» closed_at|string|false|none|none|
|» type|string|false|none|none|
|profit|object|false|none|none|
|» volume|number¦null|false|none|none|
|» usd|number¦null|false|none|none|
|» percent|number|false|none|none|
|» roe|number¦null|false|none|none|
|margin|object|false|none|none|
|» amount|number¦null|false|none|none|
|» total|number¦null|false|none|none|
|is_position_not_filled|boolean|false|none|none|

<h2 id="tocS_TakeProfitStep">TakeProfitStep</h2>
<!-- backwards compatibility -->
<a id="schematakeprofitstep"></a>
<a id="schema_TakeProfitStep"></a>
<a id="tocStakeprofitstep"></a>
<a id="tocstakeprofitstep"></a>

```json
{
  "id": 0,
  "version": 0,
  "account": {
    "id": 0,
    "type": "string",
    "name": "string",
    "market": "string",
    "link": "string"
  },
  "pair": "string",
  "instant": true,
  "status": {
    "type": "string",
    "title": "string"
  },
  "leverage": {
    "enabled": true,
    "type": "string",
    "value": 0
  },
  "position": {
    "type": "string",
    "editable": true,
    "units": {
      "value": 1231.11,
      "editable": true
    },
    "price": {
      "value": 1223.32,
      "value_without_commission": 500.2,
      "editable": true
    },
    "total": {
      "value": 100.2
    },
    "order_type": "string",
    "status": {
      "type": "string",
      "title": "string"
    }
  },
  "take_profit": {
    "enabled": true,
    "steps": [
      {
        "id": 0,
        "version": 0,
        "account": {
          "id": 0,
          "type": "string",
          "name": "string",
          "market": "string",
          "link": "string"
        },
        "pair": "string",
        "instant": true,
        "status": {
          "type": "string",
          "title": "string"
        },
        "leverage": {
          "enabled": true,
          "type": "string",
          "value": 0
        },
        "position": {
          "type": "string",
          "editable": true,
          "units": {
            "value": 1231.11,
            "editable": true
          },
          "price": {
            "value": 1223.32,
            "value_without_commission": 500.2,
            "editable": true
          },
          "total": {
            "value": 100.2
          },
          "order_type": "string",
          "status": {
            "type": "string",
            "title": "string"
          }
        },
        "take_profit": {},
        "stop_loss": {
          "enabled": true
        },
        "note": "string",
        "skip_enter_step": true,
        "data": {
          "editable": true,
          "current_price": {
            "quote_volume": "string",
            "last": "string"
          },
          "target_price_type": "string",
          "base_order_finished": true,
          "missing_funds_to_close": 0,
          "liquidation_price": 1000.22,
          "average_enter_price": 60.2,
          "average_close_price": 60.2,
          "average_enter_price_without_commission": 100.3,
          "average_close_price_without_commission": 40.2,
          "panic_sell_available": true,
          "add_funds_available": true,
          "force_start_available": true,
          "force_process_available": true,
          "cancel_available": true,
          "finished": true,
          "base_position_step_finished": true,
          "created_at": "2018-08-08 08:08:08",
          "updated_at": "2018-08-08 08:08:08",
          "closed_at": "2018-08-08 08:08:08",
          "type": "smart_sell"
        },
        "profit": {
          "volume": 14,
          "usd": 12.22,
          "percent": 12,
          "roe": 0
        },
        "margin": {
          "amount": 100.2,
          "total": 700.2
        },
        "is_position_not_filled": true
      }
    ]
  },
  "stop_loss": {
    "enabled": true
  },
  "note": "string",
  "skip_enter_step": true,
  "data": {
    "editable": true,
    "current_price": {
      "quote_volume": "string",
      "last": "string"
    },
    "target_price_type": "string",
    "base_order_finished": true,
    "missing_funds_to_close": 0,
    "liquidation_price": 1000.22,
    "average_enter_price": 60.2,
    "average_close_price": 60.2,
    "average_enter_price_without_commission": 100.3,
    "average_close_price_without_commission": 40.2,
    "panic_sell_available": true,
    "add_funds_available": true,
    "force_start_available": true,
    "force_process_available": true,
    "cancel_available": true,
    "finished": true,
    "base_position_step_finished": true,
    "created_at": "2018-08-08 08:08:08",
    "updated_at": "2018-08-08 08:08:08",
    "closed_at": "2018-08-08 08:08:08",
    "type": "smart_sell"
  },
  "profit": {
    "volume": 14,
    "usd": 12.22,
    "percent": 12,
    "roe": 0
  },
  "margin": {
    "amount": 100.2,
    "total": 700.2
  },
  "is_position_not_filled": true
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|none|
|version|integer|false|none|none|
|account|object|false|none|none|
|» id|integer|false|none|none|
|» type|string|false|none|none|
|» name|string|false|none|none|
|» market|string|false|none|none|
|» link|string|false|none|none|
|pair|string|false|none|none|
|instant|boolean|false|none|none|
|status|object|false|none|none|
|» type|string|false|none|none|
|» title|string|false|none|none|
|leverage|object|false|none|none|
|» enabled|boolean|false|none|none|
|» type|string|false|none|none|
|» value|integer|false|none|none|
|position|object|false|none|none|
|» type|string|false|none|none|
|» editable|boolean|false|none|none|
|» units|object|false|none|none|
|»» value|string¦null|false|none|none|
|»» editable|boolean|false|none|none|
|» price|object|false|none|none|
|»» value|number¦null|false|none|none|
|»» value_without_commission|number¦null|false|none|none|
|»» editable|boolean|false|none|none|
|» total|object|false|none|none|
|»» value|number¦null|false|none|none|
|» order_type|string|false|none|none|
|» status|object|false|none|none|
|»» type|string|false|none|none|
|»» title|string|false|none|none|
|take_profit|object|false|none|none|
|» enabled|boolean|false|none|none|
|» steps|[[TakeProfitStep](#schematakeprofitstep)]|false|none|none|
|stop_loss|object|false|none|none|
|» enabled|boolean|false|none|none|
|note|string|false|none|none|
|skip_enter_step|boolean|false|none|none|
|data|object|false|none|none|
|» editable|boolean|false|none|none|
|» current_price|object|false|none|none|
|»» quote_volume|string|false|none|none|
|»» last|string|false|none|none|
|» target_price_type|string|false|none|none|
|» base_order_finished|boolean|false|none|none|
|» missing_funds_to_close|number|false|none|none|
|» liquidation_price|number¦null|false|none|none|
|» average_enter_price|number¦null|false|none|none|
|» average_close_price|number¦null|false|none|none|
|» average_enter_price_without_commission|number¦null|false|none|none|
|» average_close_price_without_commission|number¦null|false|none|none|
|» panic_sell_available|boolean|false|none|none|
|» add_funds_available|boolean|false|none|none|
|» force_start_available|boolean|false|none|none|
|» force_process_available|boolean|false|none|none|
|» cancel_available|boolean|false|none|none|
|» finished|boolean|false|none|none|
|» base_position_step_finished|boolean|false|none|none|
|» created_at|string|false|none|none|
|» updated_at|string|false|none|none|
|» closed_at|string|false|none|none|
|» type|string|false|none|none|
|profit|object|false|none|none|
|» volume|number¦null|false|none|none|
|» usd|number¦null|false|none|none|
|» percent|number|false|none|none|
|» roe|number¦null|false|none|none|
|margin|object|false|none|none|
|» amount|number¦null|false|none|none|
|» total|number¦null|false|none|none|
|is_position_not_filled|boolean|false|none|none|

<h2 id="tocS_BotDealsStatsEntity">BotDealsStatsEntity</h2>
<!-- backwards compatibility -->
<a id="schemabotdealsstatsentity"></a>
<a id="schema_BotDealsStatsEntity"></a>
<a id="tocSbotdealsstatsentity"></a>
<a id="tocsbotdealsstatsentity"></a>

```json
{
  "completed": 0,
  "panic_sold": 0,
  "active": 0,
  "completed_deals_usd_profit": "5000.0",
  "from_currency_is_dollars": false,
  "completed_deals_btc_profit": "0.5",
  "funds_locked_in_active_deals": "0.0",
  "btc_funds_locked_in_active_deals": "0.0",
  "active_deals_usd_profit": "0.0",
  "active_deals_btc_profit": "0.0"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|completed|integer|false|none|none|
|panic_sold|integer|false|none|none|
|active|integer|false|none|none|
|completed_deals_usd_profit|string|false|none|none|
|from_currency_is_dollars|boolean|false|none|none|
|completed_deals_btc_profit|string|false|none|none|
|funds_locked_in_active_deals|string|false|none|none|
|btc_funds_locked_in_active_deals|string|false|none|none|
|active_deals_usd_profit|string|false|none|none|
|active_deals_btc_profit|string|false|none|none|

<h2 id="tocS_LooseAccountEntity">LooseAccountEntity</h2>
<!-- backwards compatibility -->
<a id="schemalooseaccountentity"></a>
<a id="schema_LooseAccountEntity"></a>
<a id="tocSlooseaccountentity"></a>
<a id="tocslooseaccountentity"></a>

```json
{
  "id": 1,
  "name": "New Loose Account",
  "created_at": "2021-07-08 08:08:08",
  "updated_at": "2021-08-09 09:09:09",
  "type": "Accounts::LooseAccount",
  "is_deleted": false,
  "is_locked": false
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|none|
|name|string|false|none|none|
|created_at|string|false|none|none|
|updated_at|string|false|none|none|
|type|string|false|none|none|
|is_deleted|boolean|false|none|none|
|is_locked|boolean|false|none|none|

<h2 id="tocS_ReduceFundsStep">ReduceFundsStep</h2>
<!-- backwards compatibility -->
<a id="schemareducefundsstep"></a>
<a id="schema_ReduceFundsStep"></a>
<a id="tocSreducefundsstep"></a>
<a id="tocsreducefundsstep"></a>

```json
{
  "id": 0,
  "type": "string",
  "status": {
    "type": "string",
    "title": "string",
    "basic_type": "string"
  },
  "units": {
    "value": "string"
  },
  "price": {
    "value": "string",
    "value_without_commission": "string"
  },
  "total": {
    "value": "string"
  },
  "filled": {
    "units": "string",
    "total": "string",
    "price": "string",
    "value": "string"
  },
  "data": {
    "cancelable": true,
    "panic_sell_available": true
  }
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|id|integer|false|none|none|
|type|string|false|none|none|
|status|object|false|none|none|
|» type|string|false|none|none|
|» title|string|false|none|none|
|» basic_type|string|false|none|none|
|units|object|false|none|none|
|» value|string|false|none|none|
|price|object|false|none|none|
|» value|string|false|none|none|
|» value_without_commission|string|false|none|none|
|total|object|false|none|none|
|» value|string|false|none|none|
|filled|object|false|none|none|
|» units|string|false|none|none|
|» total|string|false|none|none|
|» price|string|false|none|none|
|» value|string|false|none|none|
|data|object|false|none|none|
|» cancelable|boolean|false|none|none|
|» panic_sell_available|boolean|false|none|none|

