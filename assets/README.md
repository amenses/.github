# Assets

Organization visual assets for the GitHub profile and documentation.

| File | Description |
|------|-------------|
| `organization-logo.svg` | Amenses wordmark (vector, from ADS) |
| `architecture.svg` | High-level architecture diagram (placeholder) |

## PNG Versions

GitHub organization profiles work best with PNG images. To generate PNG versions:

```bash
# Using rsvg-convert (librsvg)
rsvg-convert -w 400 assets/organization-logo.svg -o assets/organization-logo.png

# Using ImageMagick
convert -background none -resize 400x assets/organization-logo.svg assets/organization-logo.png
```

Replace `architecture.svg` with your team's architecture diagram and export as `architecture.png` when ready.
