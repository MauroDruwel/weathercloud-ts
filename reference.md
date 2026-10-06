# Reference
## Auth
<details><summary><code>client.auth.<a href="/src/api/resources/auth/client/Client.ts">login</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Authenticates a user session to allow viewing private indoor sensors (`tempin`, `humin`, `heatin`) for the user's station.
This endpoint expects form urlencoded data and returns a `302 Found` redirect on successful login.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.auth.login({
    "LoginForm[entity]": "LoginForm[entity]",
    "LoginForm[password]": "LoginForm[password]"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.LoginAuthRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AuthClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## DeviceLive
<details><summary><code>client.deviceLive.<a href="/src/api/resources/deviceLive/client/Client.ts">getValues</a>({ ...params }) -> Weathercloud.DeviceValues</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns the latest sensor values for a device. **No CSRF token needed.**
This is the primary endpoint for a Home Assistant sensor integration.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deviceLive.getValues({
    deviceId: "5726468552"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetValuesDeviceLiveRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceLiveClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deviceLive.<a href="/src/api/resources/deviceLive/client/Client.ts">getStats</a>({ ...params }) -> Weathercloud.DeviceStats</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns current values plus day/month/year min and max for all sensors.
Each value is a `[unix_timestamp, value]` tuple.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deviceLive.getStats({
    code: "5726468552"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetStatsDeviceLiveRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceLiveClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deviceLive.<a href="/src/api/resources/deviceLive/client/Client.ts">getInfo</a>({ ...params }) -> Weathercloud.DeviceInfo</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Station name, location, elevation, equipment info.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deviceLive.getInfo({
    deviceId: "5726468552"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetInfoDeviceLiveRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceLiveClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deviceLive.<a href="/src/api/resources/deviceLive/client/Client.ts">getWindRose</a>({ ...params }) -> Weathercloud.WindData</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Wind direction distribution data for the wind rose chart.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deviceLive.getWindRose({
    code: "5726468552"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetWindRoseDeviceLiveRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceLiveClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deviceLive.<a href="/src/api/resources/deviceLive/client/Client.ts">getUpdateStatus</a>({ ...params }) -> Weathercloud.GetUpdateStatusDeviceLiveResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns seconds since last update and device online status.

> ⚠️ **Requires `X-Requested-With: XMLHttpRequest`** header — without it the server returns an empty 200.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deviceLive.getUpdateStatus({
    d: "5726468552"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetUpdateStatusDeviceLiveRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceLiveClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.deviceLive.<a href="/src/api/resources/deviceLive/client/Client.ts">getOwnerProfile</a>({ ...params }) -> Weathercloud.DeviceProfile</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns observer name, follower count, and device brand/model.

> ⚠️ **Requires `X-Requested-With: XMLHttpRequest`** header — without it the server returns an empty 200.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deviceLive.getOwnerProfile({
    d: "5726468552"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetOwnerProfileDeviceLiveRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceLiveClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## DeviceHistory
<details><summary><code>client.deviceHistory.<a href="/src/api/resources/deviceHistory/client/Client.ts">getEvolution</a>({ ...params }) -> Weathercloud.EvolutionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns hourly aggregated history for a given variable and period.

> ⚠️ **Requires `X-Requested-With: XMLHttpRequest`** header — without it the server returns an empty 200.

**Variable codes:**
| Code | Sensor |
|------|--------|
| 101  | Temperature (°C) |
| 201  | Humidity (%) |
| 541  | Dew point (°C) |
| 641  | Barometric pressure (hPa) |
| 701  | Wind speed (m/s) |
| 6001 | Wind direction (°) |
| 6501 | Wind gust / high speed (m/s) |
| 801  | Rain (mm) |
| 811  | Rain rate (mm/h) |
| 1001 | Solar radiation (W/m²) |
| 1101 | UV index |

**Period values:** `day`, `week`, `month`, `year`
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.deviceHistory.getEvolution({
    device: "5726468552",
    variable: 101,
    period: "day"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetEvolutionDeviceHistoryRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `DeviceHistoryClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Forecast
<details><summary><code>client.forecast.<a href="/src/api/resources/forecast/client/Client.ts">getDaily</a>({ ...params }) -> Weathercloud.ForecastResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.forecast.getDaily({
    id: "5726468552"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetDailyForecastRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ForecastClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Map
<details><summary><code>client.map.<a href="/src/api/resources/map/client/Client.ts">getDevices</a>({ ...params }) -> Weathercloud.MapDevicesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns stations visible on the map for a given location bounding box.

> ⚠️ **Requires `X-Requested-With: XMLHttpRequest`** header — without it the server returns an empty 200.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.map.getDevices();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetDevicesMapRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MapClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.map.<a href="/src/api/resources/map/client/Client.ts">getBackgroundDevices</a>({ ...params }) -> Weathercloud.MapDevicesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.map.getBackgroundDevices();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetBackgroundDevicesMapRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MapClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.map.<a href="/src/api/resources/map/client/Client.ts">getMetars</a>({ ...params }) -> Weathercloud.GetMetarsMapResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.map.getMetars({
    "key": "value"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Record<string, unknown>` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MapClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Stations
<details><summary><code>client.stations.<a href="/src/api/resources/stations/client/Client.ts">getNearby</a>({ ...params }) -> Weathercloud.PageDevicesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Returns nearby stations as JSON (despite `text/html` content-type header).
All `page/*` endpoints return `PageDevice` objects that include the **station name**.
Values are scaled integers — divide by 10 (e.g. `temp: 281` = 28.1°C).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stations.getNearby({
    lat: 1.1,
    lon: 1.1,
    km: 1
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetNearbyStationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stations.<a href="/src/api/resources/stations/client/Client.ts">getPopular</a>({ ...params }) -> Weathercloud.PageDevicesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stations.getPopular({
    country: "BE",
    period: "day"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetPopularStationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stations.<a href="/src/api/resources/stations/client/Client.ts">getNewest</a>({ ...params }) -> Weathercloud.PageDevicesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stations.getNewest({
    country: "BE"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetNewestStationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stations.<a href="/src/api/resources/stations/client/Client.ts">getMostFollowed</a>({ ...params }) -> Weathercloud.PageDevicesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stations.getMostFollowed({
    country: "BE"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetMostFollowedStationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stations.<a href="/src/api/resources/stations/client/Client.ts">getLastViews</a>() -> Weathercloud.PageDevicesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stations.getLastViews();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stations.<a href="/src/api/resources/stations/client/Client.ts">getOwn</a>() -> Weathercloud.PageDevicesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stations.getOwn();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**requestOptions:** `StationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.stations.<a href="/src/api/resources/stations/client/Client.ts">getStationPage</a>({ ...params }) -> string</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

The station **name** is not available from any JSON API endpoint.
The easiest way to get it is to fetch the station's HTML page and extract
the name from the `<title>` or `og:title` meta tag.

**Example response title:**
```
WeatherStation Skyline - Weathercloud | Global network of weather stations
```

Strip everything from ` - Weathercloud` onward to get the clean station name.

> This is a plain HTML page, not a JSON API. Use it for scraping only.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.stations.getStationPage({
    deviceId: "deviceId"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetStationPageStationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `StationsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Metar
<details><summary><code>client.metar.<a href="/src/api/resources/metar/client/Client.ts">getValues</a>({ ...params }) -> Weathercloud.DeviceValues</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Most `device/*` routes work identically for METAR (airport) stations by replacing the `device` prefix with `metar`.

METAR station IDs are **ICAO codes** (4 letters), e.g. `EBBR` for Brussels Airport.

**Supported `metar/*` routes (same request/response as their `device/*` counterparts):**
- `GET /metar/values/{icao}` — current readings
- `GET /metar/stats?code={icao}` — statistics
- `GET /metar/wind?code={icao}` — wind rose
- `GET /metar/info/{icao}` — station metadata
- `POST /metar/ajaxupdatedate` — last update time
- `POST /metar/ajaxprofile` — station profile
- `POST /metar/evolution` — time-series history

> **Not supported for METAR:** `/device/ajaxdevicestats`
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.metar.getValues({
    deviceId: "EBBR"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `Weathercloud.GetValuesMetarRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MetarClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

