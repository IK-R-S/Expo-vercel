## Project setup 🔧
Creating and acessing a expo application directory with expo-cli
```
npx create-expo-app <appname>; cd <appname_dir>
```

Editing app.json to support web applications
```json
{
  "web": {
    "output": "server",
    "bundler": "metro",
    "favicon": "./assets/favicon.png"
  }
}
```

Creating vercel.json
```json
{
  "buildCommand": "expo export -p web",
  "outputDirectory": "dist",
  "devCommand": "expo",
  "cleanUrls": true,
  "framework": null,
  "rewrites": [
    {
      "source": "/:path*",
      "destination": "/"
    }
  ]
}

```

Installing some required dependencies
```
npx expo install react-dom react-native-web @expo/webpack-config expo-router
```

### Running locally
```
npx expo start
```

## Deploy 🚀
Build for web and enter on web-build location
```
expo build:web; cd web-build
```
` or >>> npx expo export -p web`

Install vercel CLI
```
npm install -g vercel@latest
```

Deploy your web app on vercel **(on web-build location)**
```
vercel
```
`or >>> vc`

