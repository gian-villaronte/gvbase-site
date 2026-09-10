# AutoVault OAuth branding site

These static files are the public homepage, privacy policy, and terms required before Google enables **Publish app** for an external production OAuth application.

## Required deployment

1. Publish this directory from the `main` branch of the public `gvbase-site` GitHub repository.
2. Register `gvbase.is-a.dev` with the four GitHub Pages `A` records, then add Google's TXT verification value when Search Console provides it.
3. Verify `gvbase.is-a.dev` as a **Domain property** in Google Search Console using the same Google account that owns or edits the Cloud project.
4. In Google Auth Platform → Branding, add `gvbase.is-a.dev` under Authorized domains first.
5. Set Application home page to `https://gvbase.is-a.dev/`, Privacy policy to `https://gvbase.is-a.dev/privacy.html`, and Terms of service to `https://gvbase.is-a.dev/terms.html`, then save.
6. In Audience, select **Publish app**. The configured `drive.file` scope is non-sensitive; do not add broader Drive scopes.
7. Re-run `deployment\Configure-GoogleDrive.ps1` once so the Windows Service receives a non-expiring production refresh token.

Do not publish the private Tailscale URL, OAuth client secret, token directory, server IP address, vehicle identifiers, or evidence files on this site.
