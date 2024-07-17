## Comment link: https://github.com/storybookjs/storybook/issues/28567#issuecomment-2230911682

**Reproduction steps:**
- 1. `yarn create vue`
- 2. `yarn dlx storybook init`

**Reproduction repo:**
https://github.com/issue-reproduction/vue-vite-storybook-issue/tree/yarn/nodeLinker-node-modules

```
"vue": "^3.4.31",
"storybook": "^8.2.4",
"vite": "^5.3.4",
"@vitejs/plugin-vue": "^5.0.5"
```

**Full log:**

<details><summary><b><code>yarn storybook dev -p 6006</code></b></summary>
<p>

```log
D:\Code\issue\vue-vite-storybook-issue>yarn storybook dev -p 6006
storybook v8.2.4

info => Starting manager..
info => Starting preview..
╭───────────────────────────────────────────────────╮
│                                                   │
│   Storybook 8.2.4 for vue3-vite started           │
│   411 ms for manager and 672 ms for preview       │
│                                                   │
│    Local:            http://localhost:6006/       │
│    On your network:  http://192.168.1.20:6006/    │
│                                                   │
╰───────────────────────────────────────────────────╯
Sourcemap for "/virtual:/@storybook/builder-vite/setup-addons.js" points to missing source files
Sourcemap for "/virtual:/@storybook/builder-vite/vite-app.js" points to missing source files
```

</p>
</details> 

<details><summary><b><code>yarn storybook build</code></b></summary>
<p>

```log
D:\Code\issue\vue-vite-storybook-issue>yarn storybook build
storybook v8.2.4

info => Cleaning outputDir: storybook-static
info => Loading presets
info => Building manager..
info => Manager built (221 ms)
info => Building preview..
vite v5.3.4 building for production...
node_modules/telejson/dist/index.mjs (1413:15): Use of eval in "node_modules/telejson/dist/index.mjs" is strongly discouraged as it poses security risks and may cause issues with minification.
node_modules/telejson/dist/index.mjs (1416:18): Use of eval in "node_modules/telejson/dist/index.mjs" is strongly discouraged as it poses security risks and may cause issues with minification.
node_modules/@storybook/vue3/dist/entry-preview-docs.mjs (9:1345): Use of eval in "node_modules/@storybook/vue3/dist/entry-preview-docs.mjs" is strongly discouraged as it poses security risks and may cause issues with minification.
✓ 497 modules transformed.
storybook-static/assets/context-C0qIqeS4.png                   6.12 kB
storybook-static/assets/styling-Bk6zjRzU.png                   7.24 kB
storybook-static/iframe.html                                  16.36 kB │ gzip:   4.44 kB
storybook-static/assets/docs---vsFbMi.png                     27.88 kB
storybook-static/assets/share-DGA-UcQf.png                    40.77 kB
storybook-static/assets/accessibility-W_h2acOZ.png            42.34 kB
storybook-static/assets/figma-plugin-CH2hELiO.png             44.25 kB
storybook-static/assets/theming-D6WJLNoW.png                  44.37 kB
storybook-static/assets/testing-cbzR9l9r.png                  49.31 kB
storybook-static/assets/addon-library-BWUCAmyN.png           467.37 kB
storybook-static/assets/Header-BjLH3naM.css                    0.51 kB │ gzip:   0.30 kB
storybook-static/assets/Button-BfyGbg8N.css                    0.52 kB │ gzip:   0.29 kB
storybook-static/assets/Page-B9ntr4df.css                      0.93 kB │ gzip:   0.40 kB
storybook-static/assets/preview-BnWGZYux.js                    0.07 kB │ gzip:   0.08 kB
storybook-static/assets/preview-CIRcjyVj.js                    0.11 kB │ gzip:   0.11 kB
storybook-static/assets/preview-DE7p7AzZ.js                    0.16 kB │ gzip:   0.16 kB
storybook-static/assets/index-BoSSb2R6.js                      0.26 kB │ gzip:   0.18 kB
storybook-static/assets/index-CjvHkRZd.js                      0.39 kB │ gzip:   0.26 kB
storybook-static/assets/preview-BJPLiuSt.js                    0.64 kB │ gzip:   0.45 kB
storybook-static/assets/preview-BpcF_O6y.js                    0.71 kB │ gzip:   0.50 kB
storybook-static/assets/index-DrFu-skq.js                      0.77 kB │ gzip:   0.47 kB
storybook-static/assets/preview-2enRuHIs.js                    0.77 kB │ gzip:   0.50 kB
storybook-static/assets/Header.stories-BGlEp0Gs.js             1.02 kB │ gzip:   0.52 kB
storybook-static/assets/Button.stories-C57JHs79.js             1.56 kB │ gzip:   0.58 kB
storybook-static/assets/Header-DHOsF23d.js                     1.60 kB │ gzip:   0.89 kB
storybook-static/assets/index-Dym7vi56.js                      1.68 kB │ gzip:   0.85 kB
storybook-static/assets/DocsRenderer-PKQXORMH-DOdF88mr.js      1.78 kB │ gzip:   0.88 kB
storybook-static/assets/entry-preview-DM95eRMn.js              2.33 kB │ gzip:   1.25 kB
storybook-static/assets/index-D-8MO0q_.js                      2.58 kB │ gzip:   1.26 kB
storybook-static/assets/preview-9hFJSo5S.js                    3.20 kB │ gzip:   1.38 kB
storybook-static/assets/preview-Ct5NkTJf.js                    3.50 kB │ gzip:   1.69 kB
storybook-static/assets/Page.stories-Dks3FqcD.js               3.54 kB │ gzip:   1.68 kB
storybook-static/assets/iframe-Dly9Xvin.js                     4.54 kB │ gzip:   1.82 kB
storybook-static/assets/preview-DB9FwMii.js                    7.62 kB │ gzip:   1.56 kB
storybook-static/assets/preview-Cdum89jS.js                    8.12 kB │ gzip:   3.10 kB
storybook-static/assets/entry-preview-docs-xQ1Zq6ry.js        14.89 kB │ gzip:   5.81 kB
storybook-static/assets/Configure-CYEWVRpQ.js                 26.65 kB │ gzip:  11.53 kB
storybook-static/assets/Color-KGDBMAHA-NqxdIwus.js            30.80 kB │ gzip:  11.70 kB
storybook-static/assets/index-DZLKizrv.js                     61.57 kB │ gzip:  21.47 kB
storybook-static/assets/index-TAVom-gR.js                     80.58 kB │ gzip:  23.98 kB
storybook-static/assets/vue.esm-bundler-CMiB1aF2.js          156.87 kB │ gzip:  58.77 kB
storybook-static/assets/Button-BQ2yOadR.js                   642.77 kB │ gzip: 148.44 kB
storybook-static/assets/index-C8IehePe.js                  1,023.04 kB │ gzip: 325.85 kB

(!) Some chunks are larger than 500 kB after minification. Consider:
- Using dynamic import() to code-split the application
- Use build.rollupOptions.output.manualChunks to improve chunking: https://rollupjs.org/configuration-options/#output-manualchunks
- Adjust chunk size limit for this warning via build.chunkSizeWarningLimit.
✓ built in 6.28s
info => Preview built (6.91 s)
info => Output directory: D:\Code\issue\vue-vite-storybook-issue\storybook-static
```

</p>
</details> 

---

With `Yarn 4 (nodeLinker: pnpm)`, I got another error [#28620](https://github.com/storybookjs/storybook/issues/28620)
