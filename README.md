In this guide you will learn how to use Caddy web server to automatically generate an SSL certificate and run ImagineAPI using a domain/subdomain instead of an IP.

0. Make sure you point a domain to the IP where ImagineAPI is hosted.
1. `git clone git@github.com:imagineapi/ssl.git`
2. `cd ssl`
3. Add your email and domain to `Caddyfile`. For example I want my domain to be `demo.imagineapi.dev` and my Caddyfile looks like this:

```
  {
    email team@imagineapi.dev
  }
  
  demo.imagineapi.dev {
    reverse_proxy api:8055
  }
```

4. Launch the Caddy server with `docker compose up -d`
