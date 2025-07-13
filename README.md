# Welcome to GitHub Desktop!

This is your README. READMEs are where you can communicate what your project is and how to use it.

Write your name on line 6, save it, and then head back to GitHub Desktop.
My name is yag88



---

# Perplexity : how to create a PWA app with github ?

Yes, you can create and host your basic "Hello World" PWA app using GitHub. In fact, GitHub Pages is a popular and free way to deploy static web apps, including PWAs. Here’s how you can do it:

## How to Create and Deploy a PWA with GitHub

### 1. Create Your PWA Locally

- Follow the step-by-step guide you already have to build your PWA, making sure you include all required files: `index.html`, `style.css`, `app.js`, `manifest.json`, `service-worker.js`, and icons.


### 2. Push Your Project to GitHub

- Initialize a new Git repository in your project folder.
- Add your files, commit, and push them to a new repository on GitHub.


### 3. Configure GitHub Pages

- Go to your repository’s **Settings**.
- Find the **Pages** section.
- Set the source branch (usually `main` or `master`) and the folder (typically `/root` or `/docs` if you use a subfolder).
- Save the settings. Your app will be available at `https://<your-username>.github.io/<repo-name>/`.


### 4. Adjust Paths for GitHub Pages

- Since GitHub Pages serves your app from a subdirectory (unless it’s your user/organization site), you must update file paths in your HTML and service worker registration:
    - In your `index.html`, set the manifest and service worker paths to include the repository name, e.g.:

```html
<link rel="manifest" href="/<repo-name>/manifest.json">
```

    - Register your service worker using the correct path:

```js
navigator.serviceWorker.register('/<repo-name>/service-worker.js', {scope: '/<repo-name>/'})
```

- This ensures the service worker and manifest are found correctly[^1][^2].


### 5. Test Your PWA

- Visit your GitHub Pages URL.
- Open DevTools (F12) > Application tab to verify the manifest and service worker.
- Try installing the app and using it offline.


### 6. Troubleshooting

- Service worker not registering? Double-check the file paths and ensure your repository name is included in all relevant URLs[^2].
- GitHub Pages automatically serves content over HTTPS, which is required for PWAs.


## Resources and Templates

- You can find template repositories and detailed guides to help you get started:
    - [Bare-bones GitHub PWA template][^3]
    - [Step-by-step deployment video][^2]
    - [Official GitHub Pages documentation][^1]


## Summary Table

| Step | Description |
| :-- | :-- |
| Build Locally | Create all PWA files |
| Push to GitHub | Commit and push to a new repository |
| Configure Pages | Enable GitHub Pages in repo settings |
| Adjust File Paths | Update manifest/service worker paths |
| Test \& Troubleshoot | Verify installability and offline support |

You can absolutely use GitHub to create, host, and share your PWA with the world—no server setup required[^1][^2][^3].

<div style="text-align: center">⁂</div>

[^1]: https://christianheilmann.com/2022/01/13/turning-a-github-page-into-a-progressive-web-app/

[^2]: https://www.youtube.com/watch?v=30bL4UR4wTw

[^3]: https://github.com/codepo8/github-page-pwa

[^4]: https://github.com/pwa-builder/PWABuilder

[^5]: https://github.com/scriptex/create-pwa

[^6]: https://github.com/amankhan404/Progressive-Web-Apps-PWAs-Tutorial

[^7]: https://subscription.packtpub.com/book/web-development/9781838826345/2/ch02lvl1sec12/creating-the-pwa

[^8]: https://dev.to/pixeline/how-to-deploy-a-sapper-pwa-on-github-pages-47lc

[^9]: https://github.com/g105b/pwa

[^10]: https://microsoft.github.io/workshop-library/full/mood-journal-progressive-web-app/1-create-pwa.html

[^11]: https://www.youtube.com/watch?v=7LhSxfFufH0

[^12]: https://dev.to/nimblesite/deploy-a-flutter-pwa-on-github-pages-and-use-a-custom-domain-3mk5

[^13]: https://velog.io/@sk1440sk/Vue-PWA-Github-배포하기

[^14]: https://www.pwabuilder.com

[^15]: https://dev.to/iamfranco/deploy-react-vite-pwa-to-github-pages-35i

[^16]: https://github.com/hhimanshu/create-pwa-app

[^17]: https://github.com/pwa-builder/PWABuilder/actions/workflows/docs-github-pages.yml

[^18]: https://github.com/pwa-builder/pwa-starter

[^19]: https://stackoverflow.com/questions/71004874/deploying-pwa-to-gh-pages

[^20]: https://github.com/mohanramphp/pwa-tutorial

