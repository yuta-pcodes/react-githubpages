# React + Vite アプリをGitHub Pagesに公開する手順

多分これが一番早いと思います

```sh:bash
npm install gh-pages --save-dev
```

```json:package.json
{
  "scripts": {
    "build": "npm run build",
    "deploy": "gh-pages -d dist"
  }
}
```

**注意**: `/リポジトリ名/` は実際のリポジトリ名に置き換えてください

```typescript:vite.config.ts
export default defineConfig({
  plugins: [react()],
  base: '/リポジトリ名/',
});
```

```sh:bash
npm run deploy
```
