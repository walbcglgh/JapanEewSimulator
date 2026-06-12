# 強震モニタ風地震シミュレーション

日本の地震情報を視覚的にシミュレートするWebアプリケーションです。TurboWarpで実装された地震シミュレータで、強震モニタのようなリアルタイム地震情報の表現を学ぶことができます。

## 🎮 使用方法

### キーボード操作
- **← / →**: 地震の規模（マグニチュード）を調整 (M0～M12)
- **↑ / ↓**: 震源の深さを調整 (0～1000km)
- **Q / W**: 発生時間を調整 (0～300秒)
- **A**: 地震イベントの開始を主要動の到着と同期
- **スペースキー** または **Startボタン**: シミュレーション開始
- **マウスホイール**: マップズーム
- **R**: カメラリセット

### 機能
- 📊 地震の規模・深さ・発生時間をリアルタイム調整
- 🗺️ 日本全国の地震情報表示
- 🌊 津波警報シミュレーション
- 🔊 サウンドアラート機能
- 📈 震度分布のリアルタイム表示
- 💾 地震イベント情報の詳細表示

## ⚙️ UI改善内容

### v2.0 アップデート
- **スライダーの美化**: グラデーション橙色デザインに変更
  - ホバー時にスライダーが1.2倍に拡大
  - 発光効果でより視覚的に
  
- **震央選択ボタンの改善**: 立体的なグラデーション設計
  - ホバー時に1.05倍縮放
  - より鮮やかな発光エフェクト
  
- **パラメータ範囲の拡張**
  - 規模: M0～M12対応
  - 深さ: 0～1000km対応
  - 発生時間: 0～300秒対応

## 🚀 デプロイ方法

### Cloudflare Pages でのデプロイ

1. **リポジトリをフォーク/クローン**
   ```bash
   git clone https://github.com/walbcglgh/JapanEewSimulator.git
   cd JapanEewSimulator
   ```

2. **Cloudflare Pages に接続**
   - [Cloudflare Pages Dashboard](https://dash.cloudflare.com/) にアクセス
   - "Create a project" → "Connect to Git"
   - GitHubアカウントを接続
   - このリポジトリを選択

3. **ビルド設定**
   - Build command: なし（そのまま使用）
   - Build output directory: `/` （ルートフォルダ）
   - Environment variables: 不要

4. **デプロイ実行**
   - "Save and Deploy" をクリック
   - デプロイ完了待ち（通常2～3分）
   - 自動割り当てのURLでアクセス可能

### ローカルサーバーでのテスト
```bash
# Python 3を使用
python -m http.server 8000

# または Node.js
npx http-server
```

ブラウザで `http://localhost:8000` にアクセス

## 📱 性能最適化

- **クライアント負荷軽減**: Cloudflare Pages でホスティングすることで、複雑な計算をエッジで処理
- **モバイル対応**: レスポンシブデザインで全デバイスに対応
- **高速読み込み**: CDN経由で世界中から高速配信

**推奨環境:**
- Chrome/Edge/Firefox 最新版
- メモリ: 512MB以上推奨
- インターネット速度: 10Mbps以上推奨

## ⚠️ 注意事項

- 地震・津波シミュレーションは簡略化または独自の公式を使用しており、実際の現象と異なる場合があります
- サウンドアラートを含むため、ボリューム調整にご注意ください
- ブラウザのセキュリティ設定によっては一部機能が制限される可能性があります

## 📄 ライセンス

- **TurboWarp Packager**: Mozilla Public License 2.0
- **Scratch**: MIT License
- **このプロジェクト**: 改善版として配布

詳細は各ファイルのライセンス表記を参照してください。

## 🔗 参考リンク

- [TurboWarp - Scratch Accelerator](https://turbowarp.org)
- [TurboWarp 原始プロジェクト](https://turbowarp.org/1220818872)
- [Scratch 公式サイト](https://scratch.mit.edu)
- [Cloudflare Pages ドキュメント](https://developers.cloudflare.com/pages/)

## 👤 クレジット

- 原始プロジェクト作成者: TurboWarp/Scratch コミュニティ
- UI改善版: walbcglgh (2026)

---

**最終更新**: 2026年6月12日

ご質問やバグ報告は、GitHubのIssueセクションからお願いします。

---

# 強震監測風地震模擬器

一個用來視覺化展示日本地震資訊的網頁應用程式。使用TurboWarp實作的地震模擬器，能夠學習強震監測的即時地震資訊表現方式。

## 🎮 使用方法

### 鍵盤操作
- **← / →**: 調整地震規模（芮氏規模）(M0～M12)
- **↑ / ↓**: 調整震源深度 (0～1000km)
- **Q / W**: 調整發生時間 (0～300秒)
- **A**: 同步地震事件的開始與主要震波到達
- **空白鍵** 或 **Start按鈕**: 開始模擬
- **滑鼠滾輪**: 地圖縮放
- **R**: 重置相機

### 功能
- 📊 即時調整地震規模、深度、發生時間
- 🗺️ 展示日本全國地震資訊
- 🌊 海嘯警報模擬
- 🔊 聲音警報功能
- 📈 即時顯示震度分佈
- 💾 詳細的地震事件資訊顯示

## ⚙️ UI改善內容

### v2.0 更新
- **滑桿美化**: 改用漸層橙色設計
  - 滑鼠懸停時放大1.2倍
  - 發光效果使視覺更加吸引人
  
- **震央選擇按鈕改善**: 立體漸層設計
  - 懸停時縮放1.05倍
  - 更亮麗的發光效果
  
- **參數範圍擴展**
  - 規模: M0～M12支援
  - 深度: 0～1000km支援
  - 發生時間: 0～300秒支援

## 🚀 部署方法

### Cloudflare Pages 部署

1. **Fork/Clone 倉庫**
   ```bash
   git clone https://github.com/walbcglgh/JapanEewSimulator.git
   cd JapanEewSimulator
   ```

2. **連接到 Cloudflare Pages**
   - 進入 [Cloudflare Pages 儀表板](https://dash.cloudflare.com/)
   - 點擊 "Create a project" → "Connect to Git"
   - 連接 GitHub 帳戶
   - 選擇此倉庫

3. **建置設定**
   - Build command: 無（直接使用）
   - Build output directory: `/` （根資料夾）
   - Environment variables: 無需設定

4. **執行部署**
   - 點擊 "Save and Deploy"
   - 等待部署完成（通常2～3分鐘）
   - 可使用自動分配的URL訪問

### 本地伺服器測試
```bash
# 使用 Python 3
python -m http.server 8000

# 或使用 Node.js
npx http-server
```

在瀏覽器中訪問 `http://localhost:8000`

## 📱 效能最佳化

- **減輕客戶端負荷**: 透過Cloudflare Pages託管，複雜計算在邊緣伺服器處理
- **行動裝置相容**: 響應式設計支援所有裝置
- **快速載入**: 透過CDN在全球範圍內快速配送

**建議環境:**
- Chrome/Edge/Firefox 最新版本
- 記憶體: 512MB以上推薦
- 網際網路速度: 10Mbps以上推薦

## ⚠️ 注意事項

- 地震與海嘯模擬採用簡化或自訂公式，與實際現象可能不同
- 包含聲音警報功能，請注意音量調整
- 某些瀏覽器安全設定可能限制部分功能

## 📄 授權

- **TurboWarp Packager**: Mozilla Public License 2.0
- **Scratch**: MIT License
- **本專案**: 以改善版本發佈

詳細資訊請參閱各檔案的授權標示。

## 🔗 參考連結

- [TurboWarp - Scratch 加速器](https://turbowarp.org)
- [TurboWarp 原始專案](https://turbowarp.org/1220818872)
- [Scratch 官方網站](https://scratch.mit.edu)
- [Cloudflare Pages 文件](https://developers.cloudflare.com/pages/)

## 👤 致謝

- 原始專案作者: TurboWarp/Scratch 社群
- UI改善版本: walbcglgh (2026)

---

**最後更新**: 2026年6月12日

如有問題或錯誤報告，請使用 GitHub Issues 回報。

---

# Japan Earthquake Simulator (Kyou-shin Monitor Style)

A web application that visually simulates Japanese earthquake information. This Scratch-based simulator powered by TurboWarp helps you understand how real-time earthquake alerts and seismic intensity distributions are created and displayed.

## 🎮 How to Use

### Keyboard Controls
- **← / →**: Adjust earthquake magnitude (M0～M12)
- **↑ / ↓**: Adjust epicenter depth (0～1000km)
- **Q / W**: Adjust occurrence time (0～300 seconds)
- **A**: Sync earthquake event start with the arrival of the main seismic wave
- **Space Bar** or **Start Button**: Begin simulation
- **Mouse Wheel**: Zoom map
- **R**: Reset camera

### Features
- 📊 Real-time adjustment of earthquake magnitude, depth, and time
- 🗺️ Display earthquake information across Japan
- 🌊 Tsunami warning simulation
- 🔊 Sound alert functionality
- 📈 Real-time seismic intensity distribution display
- 💾 Detailed earthquake event information

## ⚙️ UI Improvements

### v2.0 Updates
- **Enhanced Sliders**: Gradient orange design
  - Expands to 1.2x on hover
  - Glowing effect for better visuals
  
- **Improved Epicenter Selector**: 3D gradient design
  - Scales to 1.05x on hover
  - Brighter glowing effects
  
- **Expanded Parameter Ranges**
  - Magnitude: M0～M12 supported
  - Depth: 0～1000km supported
  - Occurrence time: 0～300 seconds supported

## 🚀 Deployment Guide

### Deploy to Cloudflare Pages

1. **Fork/Clone the Repository**
   ```bash
   git clone https://github.com/walbcglgh/JapanEewSimulator.git
   cd JapanEewSimulator
   ```

2. **Connect to Cloudflare Pages**
   - Visit [Cloudflare Pages Dashboard](https://dash.cloudflare.com/)
   - Click "Create a project" → "Connect to Git"
   - Connect your GitHub account
   - Select this repository

3. **Build Configuration**
   - Build command: None (use as-is)
   - Build output directory: `/` (root folder)
   - Environment variables: Not required

4. **Deploy**
   - Click "Save and Deploy"
   - Wait for deployment to complete (usually 2～3 minutes)
   - Access via the automatically assigned URL

### Local Testing
```bash
# Using Python 3
python -m http.server 8000

# Or using Node.js
npx http-server
```

Visit `http://localhost:8000` in your browser

## 📱 Performance Optimization

- **Reduced Client Load**: Hosting on Cloudflare Pages processes complex computations on edge servers
- **Mobile Compatible**: Responsive design supports all devices
- **Fast Delivery**: Global CDN ensures fast loading worldwide

**Recommended Environment:**
- Chrome/Edge/Firefox latest version
- Memory: 512MB or more recommended
- Internet speed: 10Mbps or faster recommended

## ⚠️ Disclaimer

- The earthquake and tsunami simulations use simplified or custom formulas and may differ from real phenomena
- Sound alerts are included; please adjust volume accordingly
- Some browser security settings may restrict certain features

## 📄 License

- **TurboWarp Packager**: Mozilla Public License 2.0
- **Scratch**: MIT License
- **This Project**: Distributed as an improved version

See license notices in respective files for details.

## 🔗 References

- [TurboWarp - Scratch Accelerator](https://turbowarp.org)
- [Original TurboWarp Project](https://turbowarp.org/1220818872)
- [Scratch Official Site](https://scratch.mit.edu)
- [Cloudflare Pages Documentation](https://developers.cloudflare.com/pages/)

## 👤 Credits

- Original Project Creator: TurboWarp/Scratch Community
- UI Enhancement Version: walbcglgh (2026)

---

**Last Updated**: June 12, 2026

For questions or bug reports, please use GitHub Issues.
