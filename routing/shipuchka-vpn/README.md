# Shipuchka VPN Routing

Custom routing profile for Happ and INCY based on the RoscomVPN DEFAULT routing rules, rebranded as `Shipuchka VPN`.

## Files

- `HAPP/DEFAULT.JSON` - Happ routing JSON profile.
- `HAPP/DEFAULT.DEEPLINK` - Happ one-tap routing deeplink.
- `INCY/DEFAULT.JSON` - INCY routing JSON profile.
- `INCY/DEFAULT.DEEPLINK` - INCY one-tap routing deeplink.

## Routing Logic

Route order: `block-proxy-direct`.

Direct:

- Russian/Belarusian and whitelist resources.
- Microsoft and Apple services.
- Epic Games, Riot Games, Escape from Tarkov, Steam, Twitch, Pinterest, Faceit.

Proxy:

- Google Play.
- GitHub.
- Twitch ads.
- YouTube.
- Telegram.

Block:

- Windows telemetry.
- Torrent/DHT lists.
- Ads category.

DNS:

- Remote DNS: `8.8.8.8` over DoH.
- Domestic DNS: `77.88.8.8` over DoH.

Geo databases:

- RoscomVPN GeoIP.
- RoscomVPN Geosite.

## Sources

- https://github.com/hydraponique/roscomvpn-routing
- https://github.com/hydraponique/roscomvpn-geoip
- https://github.com/hydraponique/roscomvpn-geosite
- https://www.happ.su/main/ru/dev-docs/routing

## Validation

The deeplink payloads were decoded back to JSON and checked before publishing:

- `Name`: `Shipuchka VPN`
- `RouteOrder`: `block-proxy-direct`
- `DirectSites`: 12
- `ProxySites`: 5
- `BlockSites`: 3
