## Vite config - Path Aliases

```ts
// vite.config.ts

export default defineConfig({
  plugins: [react()],
  resolve: {
    // requires @types/node (dev dependency)
    alias: {
      "@components": path.resolve(__dirname, "./src/components"),
    },
  },
  server: {
    port: 3000,
    open: true,
  },
});
```

```json
// tsconfig.json

{
  [...]
  paths: {
    "@/*":["./src/*"],
  }
}
```

For VS Code to use the `paths` configuration from typescript

```json
  // VS Code settings.json

  "typescript.preferences.importModuleSpecifier": "non-relative"
```
