# @snow-the/dsh-bundle-dev

開發者工具：git、技能包、插件掃描

## 成員

- `dsh-gitkit` → `@snow-the/dsh-gitkit`
- `dsh-skill-pack` → `@snow-the/dsh-skill-pack`
- `dsh-plugin-guide` → `@snow-the/dsh-plugin-guide`

## 它解決什麼

profile 的 `dsh.profile.bundles` 從 19 條收成 5 條，讓「裝了什麼、哪一塊負責什麼」一眼看得懂。

## 它不解決什麼

- **不搬程式碼**：成員仍是獨立套件，可以單獨安裝、單獨測試、單獨升級。
- **不保證相依**：這個聚合包的 `dependencies` 是空的，成員由 profile 提供（本機是 `file:` 連結）。要發佈到 npm 就得把成員寫進 `dependencies`，那是另一件事。
- **不是 plugin**：入口是 `export {}`，沒有 `apply`，不會被當成插件載入。
