# Changelog
## Major Changes:
### 3.0.0:
- __BREAKING:__ `FB_ROUTE_URL`'s new default is `/hubot/fb`, to reduce the chance of routing conflicts.
- __BREAKING:__ hubot-fb now automatically sets up webhooks! Manually specifying `FB_VERIFY_TOKEN` is no longer necessary, but you now need to specify `FB_PAGE_ID`, `FB_APP_ID`, `FB_APP_SECRET`, and `FB_WEBHOOK`. For simplicity's sake, this is required even if you previously have manually set up webhooks.
- New: Setting `FB_AUTOHEAR` to `true` allows hubot-fb to treat all direct messages (which is all the API currently supports) as messages that hubot will listen to. E.g., for a robot named "hubot", both "ping" and "@hubot ping" will be passed as "@hubot ping", when `FB_AUTOHEAR` is enabled.
- New: Emit [`fb_optin` and `fb_authentication`](https://developers.facebook.com/docs/messenger-platform/webhook-reference#auth) events. 