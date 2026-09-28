# lumos-oauth-branding

The publicly reachable home page and privacy policy that Google requires before an OAuth
client can be published (Google calls this "App domain" / branding), for the OAuth client
behind **Lumos** — a private, self-hosted household assistant.

Why a separate repo: Google requires the home page and privacy policy to be publicly
accessible, on a domain whose ownership can be demonstrated, and both URLs have to keep
resolving for as long as the OAuth client exists. Keeping them here — plain static HTML,
no build step, no dependencies — means the consent screen's requirements are not coupled
to anything in the server's own release cycle.

| File | Purpose |
|---|---|
| `index.html` | Home page: what the app is, and why each Google API scope is requested |
| `privacy.html` | Privacy policy: what data is touched, where it is stored, retention, revocation |

Served by GitHub Pages at **https://jarvisqv333.github.io/lumos-oauth-branding/**.

Console values derived from this repo:

- App home page: `https://jarvisqv333.github.io/lumos-oauth-branding/`
- App privacy policy: `https://jarvisqv333.github.io/lumos-oauth-branding/privacy.html`
- Authorised domain: `jarvisqv333.github.io` (verified in Google Search Console)

If the requested scopes change, update the "Why each permission is requested" list in
`index.html` in the same change — reviewers compare that list against what the client
actually requests.
