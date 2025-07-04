# Clip Sync Project Instructions

## IMPORTANT: Version Updates

**ALWAYS increment the version number when making ANY commits to the web app.**

Version number locations to update:
1. `/index.html` - Line ~402 in the header span
2. `/sw.js` - Line 2 in CACHE_NAME constant

Version numbering scheme:
- **Patch** (1.0.X) - Bug fixes, style changes, minor updates
- **Minor** (1.X.0) - New features, significant improvements
- **Major** (X.0.0) - Breaking changes, major refactors

Current version: **v1.12.4**

## Project Structure

```
clip_sync/
├── index.html              # Main app - single file contains all code
├── manifest.json           # PWA manifest  
├── sw.js                   # Service worker for offline support
├── icon.svg                # App icon (SVG)
├── apple-touch-icon.png    # iOS home screen icon
├── README-app.md           # App deployment instructions
├── CLAUDE.md               # This file - project instructions
└── .gitignore             # Git ignore file
```

## Key Information

### GitHub Pages Deployment
- Hosted at: https://www.cabird.com/clip_sync/
- Deployed from main branch, root directory
- All app files now in root (no subdirectory)

### PWA Considerations
- The app is served from the repository root
- Manifest uses absolute paths: `/clip_sync/`
- Service worker uses relative paths for caching
- Both iOS and Windows PWA installations tested

### Technology Stack
- Pure HTML/CSS/JavaScript (no build process)
- Dual backend support:
  - Pantry Cloud (default) - simpler setup, QR code sharing
  - GitHub Gists - original method, requires PAT
- PWA features for mobile/desktop installation
- External libraries: QRCode.js, ZXing (for QR scanning)

### Color Scheme
- Light theme (changed from dark)
- Primary color: #2196F3 (blue)
- Background: #f5f5f5
- Cards: #ffffff with shadows

### Testing Checklist
When making changes:
1. Test on mobile browser
2. Test PWA installation (iOS/Android)
3. Test on desktop browser
4. Test PWA installation (Windows/Mac)
5. Verify clipboard operations work
6. Check that version number is visible

### Common Tasks

#### Adding new features
1. Update version number (minor increment)
2. Test thoroughly on mobile and desktop
3. Update README if needed
4. Commit with descriptive message

#### Fixing bugs
1. Update version number (patch increment)
2. Test the specific fix
3. Verify no regressions
4. Commit with "Fix: [description]" message

#### Style changes
1. Update version number (patch increment)
2. Maintain light theme consistency
3. Test on various screen sizes
4. Commit changes

### Browser Cache Issues
Users may need to:
- Force refresh (Ctrl+F5)
- Uninstall/reinstall PWA
- Clear browser cache
The version number helps identify cache issues.

## Recent Features Added (v1.9.0 - v1.12.4)
- ✅ Auto-sync with customizable intervals (15s/30s/60s)
- ✅ Visual sync indicator in header
- ✅ Delete button for removing sensitive items
- ✅ Cache-busting for faster updates
- ✅ Pantry Cloud backend support (now default!)
- ✅ Backend selection in settings (Pantry Cloud or GitHub Gist)
- ✅ QR code generation for sharing Pantry IDs
- ✅ QR code scanning for easy device pairing
- ✅ Improved error handling and user feedback

## Future Enhancements Discussed
- Windows system tray app (Electron)
- Encryption options
- Multiple clipboard support
- Search functionality for history
- Smart URL/email/phone detection

## Remember
- This is a simple, user-friendly tool
- No user accounts or complex setup
- One GitHub token works for all devices
- Keep the UI clean and minimal