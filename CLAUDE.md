# 短歌ポートフォリオサイト（怪獣たちの眠るとこ）

## 構成
- `index.html` — 単一ファイルで完結（HTML + CSS + JS）
- Netlify でホスティング（main ブランチ push で自動デプロイ）

## 短歌の追加方法

「短歌を追加して」と言われたら:

1. `index.html` の `sourceTankaList` 配列に新しいエントリを追加する
2. フォーマット: `["上句（五七五）", "下句（七七）"]`
3. 配列の末尾（最後の `]` の直前）に追加する
4. commit して push する

```js
// 例: 新しい短歌を追加
const sourceTankaList = [
    // ... 既存の短歌 ...
    ["新しい上句をここに", "新しい下句をここに"],  // ← 追加
];
```

### 自動実行フロー
```bash
# 1. 短歌を配列に追加（Edit ツールで）
# 2. commit & push
git add index.html
git commit -m "Add new tanka: 上句の冒頭数文字..."
git push origin main
```

push すれば Netlify が自動デプロイする。確認不要。
