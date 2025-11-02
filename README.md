# OMT Logos

This repository contains the official logos for Open Media Transport (OMT) in vector format.

## Available Logos

- `O-Logo-Vector.svg` - The "O" logo symbol
- `OMTLogo-Vector.svg` - The main OMT logo
- `OMTLogo-Horizontal-Vector.svg` - The horizontal layout OMT logo

## Automated Logo Conversion

This repository includes a GitHub Actions workflow that automatically converts SVG logos to PNG and JPG formats with different backgrounds.

### Logo Conversion Workflow

The workflow (`convert-logos-advanced.yml`) runs automatically when:
- SVG files are pushed to any branch
- Pull requests modify SVG files
- A release is published
- Manually triggered via the Actions tab

**Features:**
- Customizable output resolution (default: 512x512)
- Adjustable JPG quality (default: 95)
- PNG with white background (`*-Light.png`)
- PNG with black background (`*-Dark.png`)
- PNG with alpha transparency (`*-Alpha.png`)
- JPG with white background (`*-Light.jpg`)
- JPG with black background (`*-Dark.jpg`)
- Thumbnail generation (128x128)
- File optimization (PNG and JPG compression)
- Organized folder structure
- Detailed file manifest
- **Automatic release asset creation** when releases are published

**Triggers:**
- SVG files pushed to any branch
- Pull requests modifying SVG files
- Release publications (automatically attaches assets)
- Manual execution with custom settings

**Manual execution with custom settings:**
1. Go to the "Actions" tab in GitHub
2. Select "Advanced Logo Conversion"
3. Click "Run workflow"
4. Optionally specify resolution (e.g., "1024x1024") and JPG quality (1-100)

### Downloading Converted Files

After the workflow completes, converted files are available as downloadable artifacts:

**Workflow Artifacts:**
- `logos-png-light` - PNG files with white background
- `logos-png-dark` - PNG files with black background  
- `logos-png-alpha` - PNG files with transparency
- `logos-jpg-light` - JPG files with white background
- `logos-jpg-dark` - JPG files with black background
- `logos-thumbnails` - Thumbnail versions
- `logos-complete-package` - Everything in one package

**Release Assets (when a release is published):**
- Automatically attached to GitHub releases as downloadable assets
- `release-logos-png-light.zip` - High-quality PNG files with white backgrounds
- `release-logos-png-dark.zip` - High-quality PNG files with black backgrounds
- `release-logos-png-alpha.zip` - High-quality PNG files with transparency
- `release-logos-jpg-light.zip` - High-quality JPG files with white backgrounds
- `release-logos-jpg-dark.zip` - High-quality JPG files with black backgrounds
- `release-logos-thumbnails.zip` - Thumbnail versions for all formats
- `release-logos-ultimate.zip` - Complete package with all files
- `RELEASE_DOCUMENTATION.md` - Detailed documentation and file inventory

Artifacts are retained for 30 days (90 days for complete packages). Release assets are permanent.

## File Naming Convention

The conversion process automatically renames files:
- `*-Vector.svg` becomes:
  - `*-Light.png/jpg` (white background)
  - `*-Dark.png/jpg` (black background)
  - `*-Alpha.png` (transparent background)

## Usage Guidelines

### When to use each format:

**PNG files:**
- Use PNG for web applications requiring transparency
- Use PNG-Light for light-themed interfaces
- Use PNG-Dark for dark-themed interfaces
- Use PNG-Alpha when you need to overlay on custom backgrounds

**JPG files:**
- Use JPG for print materials and presentations
- Use JPG-Light for documents with light backgrounds
- Use JPG-Dark for documents with dark backgrounds
- Smaller file sizes than PNG, but no transparency support

**Thumbnails:**
- Use for favicons, small UI elements, or preview images
- Available in both PNG and JPG formats

## Contributing

When adding or modifying SVG files:
1. Ensure the filename ends with `-Vector.svg`
2. Test that the SVG renders correctly at different sizes
3. The conversion workflow will automatically run on push to any branch
4. For releases, create a GitHub release and the assets will be automatically generated and attached

## Creating Releases with Logo Assets

To create a release with automatically generated logo assets:
1. Create a new release in GitHub (Releases → Create a new release)
2. Choose a tag version (e.g., `v1.0.0`)
3. Add release notes
4. Publish the release
5. The workflows will automatically run and attach all converted logo files to the release
6. Users can download the assets directly from the release page

The release will include optimized PNG and JPG files in multiple formats, thumbnails, and comprehensive documentation.

## License

See [LICENSE](LICENSE) file for license information.