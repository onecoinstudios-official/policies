# One Coin Studios policies

Public privacy policies served with GitHub Pages.

| Page | URL |
| --- | --- |
| Index | `https://onecoinstudios.github.io/policies/` |
| Bento Rush privacy policy | `https://onecoinstudios.github.io/policies/bento-rush.html` |

## Publishing

1. Create a **public** GitHub repository named `policies` under the
   `onecoinstudios` account/org.
2. Push this folder to the `main` branch.
3. In the repository: **Settings → Pages → Build and deployment**
   - Source: **Deploy from a branch**
   - Branch: **main**, folder: **/ (root)**
4. Wait for the Pages deployment to finish, then open
   `https://onecoinstudios.github.io/policies/bento-rush.html`.
5. Paste that URL into Play Console → **App content → Privacy policy**.

If the repository lives under a different account or organisation, the URL
prefix changes to `https://<account>.github.io/policies/`. Update
`store/privacy_policy.md` and the `rel="canonical"` link in
`bento-rush.html` to match.

The site is plain static HTML with inline CSS, so there is no build step.
`.nojekyll` keeps GitHub Pages from running Jekyll over the files.

## Editing the policy

Edit `bento-rush.html` **and** the source of truth at
`../games/bento_rush/store/privacy_policy.md`, then update the
"Last updated" date in both places.
