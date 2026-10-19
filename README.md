# ✈ SKYFIRE VECTOR ― 蒼穹のベクトル

**[日本語](#日本語)** | [English](#english) | [简体中文](#简体中文) | [한국어](#한국어) | [Español](#español)

---

## 日本語

3Dフライトシューティングゲーム。**単一の HTML ファイル完結**で、ブラウザがあれば PC でもスマートフォンでも遊べます。

### 特徴
- 🛩️ **3D フライト**: Three.js による無限生成地形（山岳・海岸）・雲・追従カメラ
- 👾 **敵機3種**: 戦闘機 / エリート / 爆撃機。ウェーブが上がるほど強化
- 🎯 **機関銃 & 誘導ミサイル**: LOCK 枠を捉えてホーミングミサイル発射（リード誘導・自動再ロック）
- 📱 **スマホ対応**: 仮想スティック + FIRE / MSL / BST ボタン。横画面推奨（縦持ち時は回転案内を表示）
- 🔊 **サウンド On/Off**: WebAudio 合成音。`M` キーでも切替、設定は保存
- 🌍 **多言語対応**: 日本語 / English / 简体中文 / 한국어 / Español（ブラウザ言語を自動検出）
- 💾 **ローカルセーブ**: `localStorage` にハイスコア TOP5・難易度・言語・サウンド・累計戦績を保存

### 動作環境
- WebGL2 対応の最新ブラウザ（Chrome / Edge / Firefox / Safari）
- インターネット接続（Three.js を CDN から読み込みます）

### 遊び方
1. `index.html` をブラウザで開く（スマホから遊ぶ場合は PC 等でローカル配信し、同一 Wi-Fi からアクセス）
   ```bash
   python -m http.server 8000   # 例: http://<PCのIP>:8000/
   ```
2. タイトル画面で難易度・言語・サウンドを選択 → **発進**

### 操作方法
| 操作 | PC | スマホ |
|---|---|---|
| 操縦 | WASD / 矢印キー | 左画面の仮想スティック |
| 機関銃 | SPACE | FIRE ボタン長押し |
| ミサイル | X または E | MSL ボタン |
| ブースト | SHIFT 長押し | BST ボタン長押し |
| ポーズ | P | ‖ ボタン |
| サウンド切替 | M | タイトル画面の 🔊 ボタン |

### 攻略ヒント
- 赤い **LOCK** 枠に捉えてからミサイルを発射すると自動追跡します
- 環状ピックアップで装甲（緑）/ ミサイル弾数（橙）を補給
- 40秒ごとにウェーブが上昇し、敵の数・性能が増加します

### セーブデータ
ブラウザの `localStorage`（キー: `skyfire_vector_save_v1`）に保存されます。削除したい場合は
DevTools → Application → Local Storage から該当キーを消去してください。

### 技術構成
- [Three.js](https://threejs.org/) r160（CDN・ES Modules / importmap）
- WebAudio API による効果音・エンジン音のリアルタイム合成
- 外部アセットなし（メッシュ・テクスチャ・音声はすべてコード生成）

---

## English

A 3D flight shooter in a **single HTML file** — playable on desktop and mobile browsers.

### Features
- 🛩️ Infinite procedural terrain, clouds and chase camera (Three.js)
- 👾 3 enemy types: Fighter / Elite / Bomber, scaling by wave
- 🎯 Guns & homing missiles with lead targeting and auto re-lock
- 📱 Mobile controls: virtual stick + FIRE / MSL / BST buttons (landscape recommended)
- 🔊 Synthesized sound with On/Off toggle (persisted)
- 🌍 5 languages with auto-detection: ja / en / zh / ko / es
- 💾 Local save via `localStorage`: top-5 high scores, settings and career stats

### Requirements
- A modern WebGL2 browser (Chrome / Edge / Firefox / Safari); internet access for the Three.js CDN

### How to play
1. Open `index.html` in your browser (on mobile, serve it from a PC, e.g. `python -m http.server 8000`)
2. Pick difficulty, language and sound on the title screen → **LAUNCH**

### Controls
| Action | Keyboard | Touch |
|---|---|---|
| Steer | WASD / Arrows | Left-side virtual stick |
| Guns | SPACE | Hold FIRE |
| Missile | X or E | MSL |
| Boost | Hold SHIFT | Hold BST |
| Pause | P | ‖ button |
| Mute | M | 🔊 on title screen |

### Tips
- Put enemies inside the red **LOCK** box before firing missiles
- Collect rings: green = hull, orange = missiles
- Difficulty rises every 40 s (new wave)

Save data lives in `localStorage` (key `skyfire_vector_save_v1`).

---

## 简体中文

**单个 HTML 文件**的 3D 飞行射击游戏，PC 与手机浏览器均可游玩。

### 特色
- 🛩️ Three.js 无限地形、云层与追尾镜头
- 👾 三种敌机（战斗机 / 精英 / 轰炸机），随波次增强
- 🎯 机炮与诱导导弹（提前量追踪、自动重新锁定）
- 📱 手机虚拟摇杆 + FIRE / MSL / BST 按钮（建议横屏）
- 🔊 合成音效，可开关并保存设置
- 🌍 五语言自动检测：日 / EN / 简中 / 한국어 / ES
- 💾 `localStorage` 本地存档：TOP5 分数、设置与生涯统计

### 开始游戏
1. 用浏览器打开 `index.html`（手机可通过 `python -m http.server 8000` 局域网访问）
2. 在标题界面选择难度、语言、音效 → **出击**

### 操作
| 动作 | 键盘 | 触屏 |
|---|---|---|
| 操纵 | WASD / 方向键 | 左侧摇杆 |
| 机炮 | 空格 | 按住 FIRE |
| 导弹 | X 或 E | MSL |
| 加速 | 按住 SHIFT | 按住 BST |
| 暂停 | P | ‖ 按钮 |

存档位于 `localStorage`（键：`skyfire_vector_save_v1`）。

---

## 한국어

**단일 HTML 파일**로 이루어진 3D 비행 슈팅 게임. PC와 모바일 브라우저에서 플레이할 수 있습니다.

### 특징
- 🛩️ Three.js 기반 무한 지형 · 구름 · 체이징 카메라
- 👾 적기 3종(전투기/엘리트/폭격기), 웨이브에 따라 강화
- 🎯 기관총 & 호밍 미사일(리드 유도·자동 재록)
- 📱 모바일: 가상 스틱 + FIRE / MSL / BST 버튼(가로 모드 권장)
- 🔊 합성 사운드 On/Off(설정 저장)
- 🌍 5개 언어 자동 감지
- 💾 `localStorage` 로컬 저장: 하이스코어 TOP5, 설정, 전적

### 플레이 방법
1. 브라우저에서 `index.html` 열기 (모바일은 PC에서 `python -m http.server 8000` 등으로 배포)
2. 타이틀에서 난이도·언어·사운드 선택 → **출격**

### 조작
| 동작 | 키보드 | 터치 |
|---|---|---|
| 조종 | WASD / 방향키 | 왼쪽 가상 스틱 |
| 기관총 | SPACE | FIRE 길누르기 |
| 미사일 | X 또는 E | MSL |
| 부스트 | SHIFT 길누르기 | BST 길누르기 |
| 일시정지 | P | ‖ 버튼 |

저장 데이터는 `localStorage`(키 `skyfire_vector_save_v1`)에 보관됩니다.

---

## Español

Un shooter de vuelo 3D en **un solo archivo HTML**, jugable en escritorio y móviles.

### Características
- 🛩️ Terreno infinito procedural, nubes y cámara de persecución (Three.js)
- 👾 3 tipos de enemigos: caza / élite / bombardero, escalados por oleada
- 🎯 Cañones y misiles teledirigidos con predicción y re-lock automático
- 📱 Controles táctiles: palanca virtual + botones FIRE / MSL / BST (mejor en horizontal)
- 🔊 Sonido sintetizado con interruptor On/Off persistente
- 🌍 5 idiomas con detección automática
- 💾 Guardado local (`localStorage`): top-5 récords, ajustes y estadísticas

### Cómo jugar
1. Abre `index.html` en el navegador (en móvil: sirve la carpeta con `python -m http.server 8000`)
2. Elige dificultad, idioma y sonido → **DESPEGAR**

### Controles
| Acción | Teclado | Táctil |
|---|---|---|
| Pilotar | WASD / Flechas | Palanca izquierda |
| Cañones | ESPACIO | Mantener FIRE |
| Misil | X o E | MSL |
| Turbo | Mantener SHIFT | Mantener BST |
| Pausa | P | Botón ‖ |

Los datos se guardan en `localStorage` (clave `skyfire_vector_save_v1`).

---

## License / ライセンス
- Personal use & modification: free / 個人利用・改変は自由です（attribution appreciated / 出典歓迎）
- Three.js license: MIT — https://threejs.org/