# Deployment Guide

This guide explains how to deploy the QR Code Generator to various hosting platforms.

## Prerequisites

- .NET 9 SDK installed
- Project built successfully

## Building for Production

1. Navigate to the project directory:
```bash
cd QRCodeGenerator
```

2. Publish the application:
```bash
dotnet publish -c Release -o publish
```

The output will be in the `publish/wwwroot` folder.

## Deployment Options

### GitHub Pages

1. Build the project for production
2. Copy the contents of `publish/wwwroot` to your GitHub Pages repository
3. Add a `.nojekyll` file to the root to prevent Jekyll processing
4. Update the `<base href="/">` in `index.html` to match your repository path (e.g., `<base href="/QRCode/">`)
5. Commit and push to GitHub

### Azure Static Web Apps

1. Create a new Static Web App in Azure Portal
2. Connect to your GitHub repository
3. Set the build configuration:
   - App location: `/QRCodeGenerator`
   - Output location: `wwwroot`
4. Azure will automatically deploy on push

### Netlify

1. Connect your repository to Netlify
2. Set build settings:
   - Build command: `dotnet publish -c Release -o publish`
   - Publish directory: `QRCodeGenerator/publish/wwwroot`
3. Deploy

### Vercel

1. Import your repository to Vercel
2. Configure build settings:
   - Build command: `dotnet publish -c Release -o publish`
   - Output directory: `QRCodeGenerator/publish/wwwroot`
3. Deploy

## Local Testing

To test the production build locally:

```bash
cd QRCodeGenerator
dotnet publish -c Release
cd publish/wwwroot
python -m http.server 8080
```

Then navigate to `http://localhost:8080`

## Configuration

### Base Path

If deploying to a subdirectory, update the `<base href="/">` tag in `wwwroot/index.html`:

```html
<base href="/your-subdirectory/" />
```

### Service Worker (Optional)

For offline functionality, you can add a service worker to cache the application files.

## Troubleshooting

### Blank Page After Deployment

- Check that the base href matches your deployment path
- Verify all files are copied to the hosting directory
- Check browser console for errors

### Download Not Working

- Ensure the JavaScript download function is present in `index.html`
- Check browser compatibility

## Performance Optimization

The Blazor WebAssembly framework automatically:
- Compresses assets with Brotli/Gzip
- Enables browser caching
- Lazy loads assemblies

For additional optimization:
- Use `dotnet publish -c Release` for production builds
- Enable static web asset compression
- Use CDN for Bootstrap files (optional)
