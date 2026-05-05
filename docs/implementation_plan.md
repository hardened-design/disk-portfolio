# 実装計画: Three.js ASCII Art Hero Section

softglossary.space風の、3Dオブジェクトがアスキーアートとして描画されるメインビジュアルを実装する。

## フェーズ 1: パッケージの導入とセットアップ
*   `three` および `@types/three` のインストール。

## フェーズ 2: AsciiHeroコンポーネントの作成
*   `src/components/AsciiHero.astro` の作成。
*   Vanilla JS + Three.jsによるセットアップ（Scene, Camera, WebGLRenderer）。
*   `AsciiEffect` を用いたレンダラーのラップ。
*   3Dオブジェクト（幾何学模様）の配置とアニメーションの実装。

## フェーズ 3: ページへの統合とスタイリング
*   `src/pages/index.astro` に `AsciiHero` コンポーネントを配置。
*   `src/styles/global.css` を用いたベーススタイルの設定。

## フェーズ 4: 検証と調整
*   アスキーアートの文字セット、解像度、色、回転スピードの微調整。
