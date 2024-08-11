This repo shows an issue with vscode not honoring tsconfig.app.json files

run `pnpm build`
notice it builds successfully.

But even though build is successful, vscode shows errors in the editor.

![editor_error.png](editor_error.png)

This is because the default value of `strictNullChecks` is `true`, and since vscode does not respect `tsconfig.app.json`, it does not know that `strictNullChecks` is set to `false`.
