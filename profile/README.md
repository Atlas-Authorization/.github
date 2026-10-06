<div align="center">

# Atlas

### The open identity platform — authentication, authorization & user management for modern apps

A complete, developer-first alternative to Auth0 and Clerk: hosted & embeddable sign-in, organizations/B2B, SSO (SAML/OIDC), SCIM, passkeys & MFA, OAuth/OIDC provider, fine-grained authorization (FGA), machine identities, and a first-class SDK for every stack.

[Docs](https://atlasauth.net/docs) · [API reference](https://api.atlasauth.net/v1/openapi.json) · [Dashboard](https://atlasauth.net) · [Connectors](https://atlasauth.net/connectors)

</div>

---

## Quickstart

```bash
# Scaffold a full app (Next.js / React+Vite templates) wired to Atlas
npm create @atlasauth/atlas-app@latest

# or add the management CLI
npm i -g @atlasauth/cli   # → `atlas`
```

```ts
import { AtlasProvider, SignedIn, SignedOut, SignInButton, UserButton } from '@atlasauth/react';

<AtlasProvider publishableKey={pk}>
  <SignedOut><SignInButton /></SignedOut>
  <SignedIn><UserButton /></SignedIn>
</AtlasProvider>
```

---

## Packages

### Frontend (JavaScript / TypeScript) — on [npm `@atlasauth`](https://www.npmjs.com/org/atlasauth)
| Package | What |
|---|---|
| [`@atlasauth/js`](https://www.npmjs.com/package/@atlasauth/js) | Core browser client + flow machine |
| [`@atlasauth/react`](https://www.npmjs.com/package/@atlasauth/react) · [`vue`](https://www.npmjs.com/package/@atlasauth/vue) · [`angular`](https://www.npmjs.com/package/@atlasauth/angular) · [`svelte`](https://www.npmjs.com/package/@atlasauth/svelte) · [`solid`](https://www.npmjs.com/package/@atlasauth/solid) · [`qwik`](https://www.npmjs.com/package/@atlasauth/qwik) | Framework bindings — components & hooks |
| [`@atlasauth/nextjs`](https://www.npmjs.com/package/@atlasauth/nextjs) · [`nuxt`](https://www.npmjs.com/package/@atlasauth/nuxt) · [`astro`](https://www.npmjs.com/package/@atlasauth/astro) · [`react-router`](https://www.npmjs.com/package/@atlasauth/react-router) · [`tanstack-react-start`](https://www.npmjs.com/package/@atlasauth/tanstack-react-start) | Meta-framework integrations (SSR/middleware) |
| [`@atlasauth/elements`](https://www.npmjs.com/package/@atlasauth/elements) · [`@atlasauth/lock`](https://www.npmjs.com/package/@atlasauth/lock) · [`embed`](https://www.npmjs.com/package/@atlasauth/embed) | Headless primitives & the drop-in login widget → [atlas-lock](https://github.com/Atlas-Authorization/atlas-lock) |
| [`@atlasauth/themes`](https://www.npmjs.com/package/@atlasauth/themes) · [`localizations`](https://www.npmjs.com/package/@atlasauth/localizations) | Appearance presets & i18n catalogs |
| [`@atlasauth/chrome-extension`](https://www.npmjs.com/package/@atlasauth/chrome-extension) · [`electron`](https://www.npmjs.com/package/@atlasauth/electron) · `gatsby-plugin-atlasauth` | Extension / desktop / Gatsby |

### Backend & framework middleware
| Package | What |
|---|---|
| [`@atlasauth/backend`](https://www.npmjs.com/package/@atlasauth/backend) | Node management + token verification SDK |
| [`@atlasauth/express`](https://www.npmjs.com/package/@atlasauth/express) · [`fastify`](https://www.npmjs.com/package/@atlasauth/fastify) · [`hono`](https://www.npmjs.com/package/@atlasauth/hono) · [`nestjs`](https://www.npmjs.com/package/@atlasauth/nestjs) · [`passport`](https://www.npmjs.com/package/@atlasauth/passport) | Framework middleware → [atlas-passport](https://github.com/Atlas-Authorization/atlas-passport) |

### Server SDKs (every language)
| Language | Package | Registry |
|---|---|---|
| Go | [`atlas-go`](https://github.com/Atlas-Authorization/atlas-go) | `go get github.com/Atlas-Authorization/atlas-go` |
| Rust | [`atlasauth`](https://crates.io/crates/atlasauth) | `cargo add atlasauth` → [atlas-rust](https://github.com/Atlas-Authorization/atlas-rust) |
| Python | [`atlas-backend`](https://pypi.org/project/atlas-backend/) | `pip install atlas-backend` |
| Ruby | [`atlas-auth`](https://rubygems.org/gems/atlas-auth) | `gem install atlas-auth` |
| Java | [`net.atlasauth:atlas-java`](https://central.sonatype.com/artifact/net.atlasauth/atlas-java) | Maven Central → [atlas-java](https://github.com/Atlas-Authorization/atlas-java) |
| .NET | [`Atlas.Sdk`](https://www.nuget.org/packages/Atlas.Sdk) | `dotnet add package Atlas.Sdk` → [atlas-dotnet](https://github.com/Atlas-Authorization/atlas-dotnet) |
| PHP | [`atlas-auth/atlas-php`](https://packagist.org/packages/atlas-auth/atlas-php) | `composer require atlas-auth/atlas-php` → [atlas-php](https://github.com/Atlas-Authorization/atlas-php) |
| Elixir | `atlas_auth` (Hex) | → [atlas-elixir](https://github.com/Atlas-Authorization/atlas-elixir) |

### Mobile & native
[`atlas-swift`](https://github.com/Atlas-Authorization/atlas-swift) (SPM) · Android [`net.atlasauth:atlas-android`](https://central.sonatype.com/artifact/net.atlasauth/atlas-android) ([src](https://github.com/Atlas-Authorization/atlas-android)) · Kotlin/JVM [`net.atlasauth:atlas-kotlin`](https://central.sonatype.com/artifact/net.atlasauth/atlas-kotlin) ([src](https://github.com/Atlas-Authorization/atlas-kotlin)) · Flutter [`atlas_auth`](https://pub.dev/packages/atlas_auth) ([src](https://github.com/Atlas-Authorization/atlas-flutter)) · [`@atlasauth/react-native`](https://www.npmjs.com/package/@atlasauth/react-native) · [`expo`](https://www.npmjs.com/package/@atlasauth/expo) (+ `expo-passkeys` / `expo-biometrics` / `expo-google-signin`) · [`capacitor`](https://www.npmjs.com/package/@atlasauth/capacitor)

### Fine-grained authorization (FGA) — OpenFGA-compatible
Atlas speaks the OpenFGA wire protocol at `/v1/openfga`, so the stock OpenFGA SDKs/CLI work — plus native clients with Atlas defaults:
[`@atlasauth/fga-js`](https://www.npmjs.com/package/@atlasauth/fga-js) · [`atlas-fga-go`](https://github.com/Atlas-Authorization/atlas-fga-go) · [`atlas-fga`](https://pypi.org/project/atlas-fga/) (Python → [atlas-fga-python](https://github.com/Atlas-Authorization/atlas-fga-python))

### Infrastructure as code
[`terraform-provider-atlas`](https://github.com/Atlas-Authorization/terraform-provider-atlas) · [`pulumi-atlas`](https://github.com/Atlas-Authorization/pulumi-atlas) · config-as-code via `atlas config export/import` + the [`atlas-deploy`](https://github.com/Atlas-Authorization/terraform-provider-atlas) GitHub Action

### Tooling & DX
[`@atlasauth/cli`](https://www.npmjs.com/package/@atlasauth/cli) · [`create-atlas-app`](https://www.npmjs.com/package/@atlasauth/create-atlas-app) · [`@atlasauth/actions`](https://www.npmjs.com/package/@atlasauth/actions) (+ [atlas-actions](https://github.com/Atlas-Authorization/atlas-actions)) · [`agent-toolkit`](https://www.npmjs.com/package/@atlasauth/agent-toolkit) · [`mcp`](https://www.npmjs.com/package/@atlasauth/mcp) · [`msw`](https://www.npmjs.com/package/@atlasauth/msw) · [`testing`](https://www.npmjs.com/package/@atlasauth/testing) · [`eslint-plugin`](https://www.npmjs.com/package/@atlasauth/eslint-plugin) · [`upgrade`](https://www.npmjs.com/package/@atlasauth/upgrade) · [`jwt-decode`](https://www.npmjs.com/package/@atlasauth/jwt-decode) · [`cli-banner`](https://www.npmjs.com/package/@atlasauth/cli-banner)

**Try the API:** [Postman collection](https://github.com/Atlas-Authorization/atlas-postman) (generated from the spec, 643 ops) · [OIDC/JWT playground](https://github.com/Atlas-Authorization/atlas-playground) · [quickstarts for every stack](https://github.com/orgs/Atlas-Authorization/repositories?q=quickstart)

---

## Why Atlas

- **Full auth surface** — passwords, email/SMS codes & magic links, passkeys/WebAuthn, TOTP/SMS/push MFA, social & enterprise connections, step-up & adaptive MFA.
- **Standards-complete OAuth/OIDC provider** — PKCE, device flow, CIBA, PAR, RAR, DPoP & mTLS-bound tokens, `private_key_jwt`, JAR/JARM, token exchange, dynamic client registration.
- **B2B/Organizations** — org-scoped SSO with JIT provisioning, SCIM, roles & permissions, per-org branding & settings.
- **Fine-grained authorization** — ReBAC/FGA with an OpenFGA-compatible API.
- **Machine identities** — enrolment, per-machine keypairs, short-lived JWTs, scoped & proof-of-possession API keys.
- **Migrate in, not out** — lazy/custom-database migration drains your old user store on first login.

<div align="center">

**[Read the docs →](https://atlasauth.net/docs)**

</div>
