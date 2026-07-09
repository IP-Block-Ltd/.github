# IP Block Ltd

**[ip-block.com](https://www.ip-block.com/)** is an IP-screening service that protects websites and eCommerce stores from unwanted traffic. This organization hosts the **official platform extensions** that connect your site to the service.

Every extension does the same thing in its platform's native idiom: on each front-end request it asks the IP Block API whether the visitor should be allowed, and blocks the flagged ones — before your pages render.

> ⚠️ **All extensions are currently untested in production.** They are provided as-is under the **GNU GPLv3** — please feel free to fork, modify, improve, and open pull requests.

## The shared API contract

```
POST https://api.ip-block.com/v1/check
Content-Type: application/json
{ "api_key": "...", "site_id": "...", "ip": "<visitor>", "user_agent": "...", "referrer": "..." }
  ->  { "action": "allow" }   |   { "action": "block" }
```

The API key travels in the **body** (not a header) · **1-second** timeout · **fail-open** on any error · block only when `action == "block"`. Health check: `GET /v1/ping → {"status":"ok"}`.

---

## 🛒 eCommerce

| Platform | Version | Repository |
|----------|---------|------------|
| Magento (Adobe Commerce OS) | 2.4.9 | [ipblock-magento](https://github.com/IP-Block-Ltd/ipblock-magento) |
| WooCommerce | 10.9.4 | [ipblock-woocommerce](https://github.com/IP-Block-Ltd/ipblock-woocommerce) |
| PrestaShop | 9.1.4 | [ipblock-prestashop](https://github.com/IP-Block-Ltd/ipblock-prestashop) |
| OpenCart | 4.1.0.3 | [ipblock-opencart](https://github.com/IP-Block-Ltd/ipblock-opencart) |
| Shopware 6 | 6.7.11.1 | [ipblock-shopware](https://github.com/IP-Block-Ltd/ipblock-shopware) |
| CS-Cart | 4.20.1 | [ipblock-cs-cart](https://github.com/IP-Block-Ltd/ipblock-cs-cart) |
| X-Cart | 5.6.0 | [ipblock-x-cart](https://github.com/IP-Block-Ltd/ipblock-x-cart) |
| Zen Cart | 2.2.2 | [ipblock-zencart](https://github.com/IP-Block-Ltd/ipblock-zencart) |
| osCommerce (CE Phoenix) | 1.0.7.18 | [ipblock-oscommerce](https://github.com/IP-Block-Ltd/ipblock-oscommerce) |
| Craft Commerce | 5.10.10 | [ipblock-craft](https://github.com/IP-Block-Ltd/ipblock-craft) |

## 📝 CMS & forums

| Platform | Version | Repository |
|----------|---------|------------|
| WordPress | 7.0 | [ipblock-wordpress](https://github.com/IP-Block-Ltd/ipblock-wordpress) |
| Drupal (+ Commerce) | 11 | [ipblock-drupal](https://github.com/IP-Block-Ltd/ipblock-drupal) |
| Joomla | 5 | [ipblock-joomla](https://github.com/IP-Block-Ltd/ipblock-joomla) |
| phpBB | 3.3.17 | [ipblock-phpbb](https://github.com/IP-Block-Ltd/ipblock-phpbb) |
| XenForo | 2.3.11 | [ipblock-xenforo](https://github.com/IP-Block-Ltd/ipblock-xenforo) |
| MyBB | 1.8.40 | [ipblock-mybb](https://github.com/IP-Block-Ltd/ipblock-mybb) |
| MediaWiki | 1.43 LTS | [ipblock-mediawiki](https://github.com/IP-Block-Ltd/ipblock-mediawiki) |

## 🌐 Edge / reverse-proxy / WAF / CDN

Protect **any** site — including SaaS storefronts (Shopify, Wix) fronted by a CDN.

| Platform | Repository |
|----------|------------|
| Cloudflare Workers | [ipblock-cloudflare](https://github.com/IP-Block-Ltd/ipblock-cloudflare) |
| Fastly Compute | [ipblock-fastly](https://github.com/IP-Block-Ltd/ipblock-fastly) |
| AWS CloudFront (Lambda@Edge) | [ipblock-aws-cloudfront](https://github.com/IP-Block-Ltd/ipblock-aws-cloudfront) |
| Akamai EdgeWorkers | [ipblock-akamai](https://github.com/IP-Block-Ltd/ipblock-akamai) |
| NGINX / OpenResty | [ipblock-nginx](https://github.com/IP-Block-Ltd/ipblock-nginx) |
| Apache httpd | [ipblock-apache](https://github.com/IP-Block-Ltd/ipblock-apache) |
| Caddy | [ipblock-caddy](https://github.com/IP-Block-Ltd/ipblock-caddy) |
| HAProxy | [ipblock-haproxy](https://github.com/IP-Block-Ltd/ipblock-haproxy) |
| Traefik | [ipblock-traefik](https://github.com/IP-Block-Ltd/ipblock-traefik) |
| Kong Gateway | [ipblock-kong](https://github.com/IP-Block-Ltd/ipblock-kong) |
| Envoy (ext_authz) | [ipblock-envoy](https://github.com/IP-Block-Ltd/ipblock-envoy) |

## 🖥️ Hosting control panels

| Panel | Version | Repository |
|-------|---------|------------|
| cPanel / WHM | 136 | [ipblock-cpanel](https://github.com/IP-Block-Ltd/ipblock-cpanel) |
| Plesk Obsidian | 18.0.76 | [ipblock-plesk](https://github.com/IP-Block-Ltd/ipblock-plesk) |
| DirectAdmin | 1.705 | [ipblock-directadmin](https://github.com/IP-Block-Ltd/ipblock-directadmin) |

## 🧩 Application frameworks

| Framework | Repository |
|-----------|------------|
| Symfony | [ipblock-symfony](https://github.com/IP-Block-Ltd/ipblock-symfony) |
| Django | [ipblock-django](https://github.com/IP-Block-Ltd/ipblock-django) |
| Ruby on Rails | [ipblock-rails](https://github.com/IP-Block-Ltd/ipblock-rails) |
| ASP.NET Core | [ipblock-aspnet](https://github.com/IP-Block-Ltd/ipblock-aspnet) |
| Spring Boot | [ipblock-springboot](https://github.com/IP-Block-Ltd/ipblock-springboot) |
| Flask | [ipblock-flask](https://github.com/IP-Block-Ltd/ipblock-flask) |
| FastAPI | [ipblock-fastapi](https://github.com/IP-Block-Ltd/ipblock-fastapi) |
| Express (Node.js) | [ipblock-express](https://github.com/IP-Block-Ltd/ipblock-express) |
| Go (net/http) | [ipblock-go](https://github.com/IP-Block-Ltd/ipblock-go) |

---

Each repository contains full installation and configuration instructions in its own `README.md`. Contributions are welcome — see each repo's `CONTRIBUTING.md`.

© IP Block Ltd · Licensed under the [GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.html).
