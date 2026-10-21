# Homepage assets

- `v1/*.svg`: the seven displayed Font Awesome Free 7.3.1 icons, from the tagged upstream repository (CC BY 4.0). Upstream attribution comments are retained.
- Upstream licenses and original font notices are in `licenses/`.

Fonts are **not committed**. The deployed site supplies `fonts/profile-heading.woff2`, `fonts/profile-body.woff2`, and `fonts/profile-mono.woff2` from its existing local `html/fonts/` directory. These are renamed, Latin-subset WOFF2 derivatives of the existing Bangers, Raleway, and Caskaydia Cove fonts. They include Latin/extended Latin, general punctuation, the euro/trademark signs, and ツ; unsupported characters use system fallbacks. Original TTF files remain untouched. Conversion used fonttools 4.67.0 with Brotli 1.2.0.

The homepage needs no JavaScript or CSS framework dependencies. Its small inline layout rules preserve the spacing and breakpoints previously provided by Bootstrap. Bootstrap's MIT license is retained to acknowledge those derived rules. The source-code ASCII drawing remains in its original script comment.

Deployment mounts this directory read-only at `/var/www/html/assets/`. Versioned assets are cached for a year: create a new version directory and update HTML references when changing them. Local optimized fonts are cached for one week; rename them and update HTML references for immediate cache busting when replacing them.
