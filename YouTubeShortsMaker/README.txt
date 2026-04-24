╔══════════════════════════════════════╗
║       YT SHORTS MAKER — SETUP        ║
╚══════════════════════════════════════╝

QUICK START
───────────
1. Keep index.html and the "YT Shorts Maker.app" in the same folder.
2. Run this ONE-TIME setup command in Terminal to make the app work:
   
   chmod +x "/path/to/YT Shorts Maker.app/Contents/MacOS/launcher"
   
   (Replace /path/to with the actual folder path)

3. Double-click "YT Shorts Maker.app" — it opens the app in your browser.

4. To add to your Applications folder:
   - Move the entire folder (index.html + app) to ~/Applications
   - Or keep it anywhere and add an alias to /Applications

CREATING THE APP ICON (.icns)
──────────────────────────────
Run this in Terminal (one time only, from the folder containing the app):

   iconutil -c icns "YT Shorts Maker.app/Contents/Resources/AppIcon.iconset" \
            -o "YT Shorts Maker.app/Contents/Resources/AppIcon.icns"

This converts the included PNG set into a proper macOS icon.

YOUTUBE VIDEOS
──────────────
To clip YouTube videos, first download with yt-dlp:
   brew install yt-dlp
   yt-dlp -f mp4 "https://youtu.be/VIDEO_ID" -o ~/Downloads/video.mp4

Then use "Browse File" to open the downloaded MP4.

BEST BROWSER
────────────
Use Google Chrome or Microsoft Edge for best MediaRecorder support.
Safari has limited codec support — Chrome is recommended.
