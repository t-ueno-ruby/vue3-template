# Vue.js(ver3)のテンプレート

## バージョン

- Vue.js: 3.5.3
- TypeScript: 5.4.5
- Vite: 5.4.3

### 確認コマンド

<details>
<summary>プロジェクト作成</summary>

```bash
docker compose run --rm frontend npm create vue@latest
# Need to install the following packages:
# create-vue@3.10.4
# Ok to proceed? (y) y
# 
# 
# > npx
# > create-vue
# 
# 
# Vue.js - The Progressive JavaScript Framework
# 
# ✔ Project name: … frontend
# ✔ Add TypeScript? … Yes
# ✔ Add JSX Support? … No
# ✔ Add Vue Router for Single Page Application development? … No
# ✔ Add Pinia for state management? … No
# ✔ Add Vitest for Unit Testing? … No
# ✔ Add an End-to-End Testing Solution? › No
# ✔ Add ESLint for code quality? … Yes
# ✔ Add Prettier for code formatting? … Yes
# ✔ Add Vue DevTools 7 extension for debugging? (experimental) … No
# 
# Scaffolding project in /app/frontend...
# 
# Done. Now run:
# 
#   cd front
#   npm install
#   npm run format
#   npm run dev
# 
# npm notice
# npm notice New patch version of npm available! 10.8.2 -> 10.8.3
# npm notice Changelog: https://github.com/npm/cli/releases/tag/v10.8.3
# npm notice To update run: npm install -g npm@10.8.3
# npm notice
```

</details>
<details>
<summary>Vue.js、TypeScriptのバージョン確認</summary>

```bash
# Vue.js
docker compose run --rm frontend npm list vue
# frontend@0.0.0 /app/frontend
# +-- @vitejs/plugin-vue@5.1.3
# | `-- vue@3.5.3 deduped
# `-- vue@3.5.3
#   `-- @vue/server-renderer@3.5.3
#     `-- vue@3.5.3 deduped

# TypeScript
docker compose run --rm frontend npm list typescript
# frontend@0.0.0 /app/frontend
# +-- @vue/eslint-config-typescript@13.0.0
# | +-- @typescript-eslint/eslint-plugin@7.18.0
# | | `-- ts-api-utils@1.3.0
# | |   `-- typescript@5.4.5 deduped
# | `-- typescript@5.4.5 deduped
# +-- typescript@5.4.5
# +-- vue-tsc@2.1.6
# | +-- @vue/language-core@2.1.6
# | | `-- typescript@5.4.5 deduped
# | `-- typescript@5.4.5 deduped
# `-- vue@3.5.3
#   `-- typescript@5.4.5 deduped
```

</details>

## 使い方(最小限)

### imageの構築、コンテナの起動、動作確認

```bash
docker compose up
```

<http://localhost:5173>にアクセスすれば動作確認できる

### コンテナに入る

```bash
docker compose up -d;
docker compose exec -it frontend bash
```

### コンテナに入らずにコマンドを実行

```bash
docker compose run --rm frontend <npmのコマンド>
```
