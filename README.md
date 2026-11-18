# Time Machine Earth for iPhone

A SwiftUI WKWebView shell (iOS 17+) around the live web app at https://time-machine-earth.vercel.app/, generated from the Kolam iOS shell template. Inside this app the page switches to the Apple HIG look (Kolam iOS kit: navigation bar, floating tab bar, SF-style icons); in Safari the website keeps its own look.

Bundle id `com.gopinath.timemachine`. Web source: https://github.com/tgopinath/time-machine-earth

```sh
xcodebuild -project TimeMachineEarth.xcodeproj -scheme TimeMachineEarth -destination 'platform=iOS Simulator,name=iPhone 17 Pro' \
  -derivedDataPath build CODE_SIGNING_ALLOWED=NO build
xcrun simctl install booted build/Build/Products/Debug-iphonesimulator/TimeMachineEarth.app
xcrun simctl launch booted com.gopinath.timemachine
```

Screenshots from the Simulator are in `screenshots/`.
