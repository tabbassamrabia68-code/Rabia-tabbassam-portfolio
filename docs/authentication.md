# Authentication and credential handling

## Current portfolio implementation

This repository currently contains a static, client-side portfolio website. It does **not** implement user accounts, sign-in, sign-up, password storage, sessions, access tokens, refresh tokens, or protected API routes.

### Components

- `index.html` renders the portfolio content and navigation.
- `styles.css` provides the responsive visual design.
- `script.js` handles the mobile navigation, current year, and scroll-reveal effects.
- There is no authentication backend or identity provider configured in this repository.

### Request and data flow

1. A visitor opens the deployed static website.
2. The hosting platform serves the HTML, CSS, JavaScript, and SVG assets.
3. The browser runs the local JavaScript for presentation interactions.
4. Links to GitHub and LinkedIn navigate to those external services, which manage their own authentication.

There is no login request from this website and no credential or token exchange initiated by this code.

### Credentials and tokens

- The site does not ask visitors for passwords or personal account credentials.
- No access token, refresh token, API key, or session cookie is created or stored by the portfolio code.
- Do not add secrets to HTML, CSS, JavaScript, or any other public repository file.
- If a future feature needs a private API or authenticated user accounts, implement it through a backend or trusted identity provider. Keep secrets in the hosting provider's server-side environment variables, use HTTPS, validate authorization on the server, and never rely on hiding a frontend control as access protection.

## Important distinction

This document describes the code currently present in this portfolio repository. It is not a claim that the separate AutoLedger project uses this same authentication design. To document AutoLedger's actual authentication accurately, its backend authentication routes, dependencies, configuration, and token implementation must be inspected in the AutoLedger repository.

## Deployment notes

This is a static site and can be deployed on Vercel without a build command. Use the repository root as the project root and leave the output directory empty/default. No environment variables are required for the current portfolio version.
