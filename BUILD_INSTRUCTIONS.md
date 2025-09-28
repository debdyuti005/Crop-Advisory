# Android APK Build Instructions

## GitHub Actions Setup

This repository includes a GitHub Actions workflow that automatically builds your Android APK whenever you push code to the main branch.

### How to get your APK:

1. **Push your code to GitHub:**
   ```bash
   git add .
   git commit -m "Add Capacitor Android build setup"
   git push origin main
   ```

2. **Check the Actions tab:**
   - Go to your repository on GitHub
   - Click on the "Actions" tab
   - Look for the "Build Android APK" workflow
   - Wait for it to complete (usually takes 5-10 minutes)

3. **Download your APK:**
   - Click on the completed workflow run
   - Scroll down to the "Artifacts" section
   - Download the `crop-advisory-apk` file
   - Extract it to get your APK file

4. **Install on your device:**
   - Transfer the APK to your Android device
   - Enable "Install from unknown sources" in your device settings
   - Install the APK

### Manual Trigger:

You can also manually trigger the build:
- Go to Actions tab → Build Android APK → Run workflow

### Releases:

The workflow also creates automatic releases when you push to the main branch. Check the "Releases" section of your repository to download APKs from there.

## Local Development

To continue developing locally:

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Sync with Capacitor
npx cap sync android
```

## Notes:

- The APK built by GitHub Actions will be unsigned (for testing purposes)
- For production releases, you'll need to set up proper app signing
- The multiple drawable folders are normal Android behavior for different screen densities