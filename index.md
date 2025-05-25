---
layout: single
author_profile: true
quick_start: false
toc: true
toc_sticky: true

header:
  show_title: false
---
## About me
hello
## Works
以下のデモはすべてブラウザ上で動作します（一部のデモは WebGPU 対応が必要です）．
### WebGPU-Ocean
<blockquote class="twitter-tweet" data-media-max-width="560"><p lang="ja" dir="ltr">WebGPU で実装した，MLS-MPM による流体シミュレーションをデプロイしました．ブラウザ上で動きます．SPH よりもかなり高速です．/ A MLS-MPM fluid simulation in WebGPU has been deployed! <br>demo : <a href="https://t.co/Dm8QTxo6gO">https://t.co/Dm8QTxo6gO</a><br>repo : <a href="https://t.co/X0I484K4i5">https://t.co/X0I484K4i5</a> <a href="https://t.co/wW1Gn3pXEo">pic.twitter.com/wW1Gn3pXEo</a></p>&mdash; matsuoka-601 (@matsuoka_601) <a href="https://twitter.com/matsuoka_601/status/1877570211013902497?ref_src=twsrc%5Etfw">January 10, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

WebGPU を用いて，ブラウザ上で動作するリアルタイム流体シミュレーションを実装しました．シミュレーションは，2018 年に Hu らによって提案された MLS-MPM という新しい手法を，GPGPU で並列化したものを用いています．ブラウザ上で動作する流体シミュレーションとしては，自分が知る限りでは現時点で最大クラスの規模のものです．

- **デモ** : [WebGPU-Ocean](https://webgpu-ocean.netlify.app/)
- **GitHub** : [WebGPU-Ocean](https://github.com/matsuoka-601/WebGPU-Ocean)
- **解説記事** : [WebGPU で MLS-MPM を実装し，ブラウザ上で 10 万粒子規模のリアルタイムシミュレーションを実現する](https://zenn.dev/sparkle/articles/3eb1225f891a87)
- CG 関連の外部サイトにも掲載していただきました．
    - [80lv]()
    - [CGWorld]()
    - [3D人]()
    - [WebGPU Experts]()
    
### WaterBall
<blockquote class="twitter-tweet" data-media-max-width="560"><p lang="en" dir="ltr">Deployed a new real-time fluid simulation - &quot;waterball&quot;! <br><br>Interact with the water on a sphere🌏. <br><br>demo : <a href="https://t.co/HLyL5OtTwQ">https://t.co/HLyL5OtTwQ</a><br>repo : <a href="https://t.co/RKji8V6IbG">https://t.co/RKji8V6IbG</a><br><br>The demo runs smoothly even on my 6-year-old iPad! (see the reply) <a href="https://t.co/qCC9Pj1Uqw">pic.twitter.com/qCC9Pj1Uqw</a></p>&mdash; matsuoka-601 (@matsuoka_601) <a href="https://twitter.com/matsuoka_601/status/1886294037499695274?ref_src=twsrc%5Etfw">February 3, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

球体上の流体シミュレーションに挑戦しました．WebGPU-Ocean と同じく，MLS-MPM を GPGPU 並列化したものを用いており，高速です．

- **デモ** : [WaterBall](https://waterball.netlify.app/)
- **GitHub** : [WaterBall](https://github.com/matsuoka-601)
- CG 関連の外部サイトにも掲載していただきました．
    - [WebGPU Experts](https://www.webgpuexperts.com/best-webgpu-updates-february-2025)
    - [80lv](https://80.lv/articles/control-this-water-sphere-fluid-simulation-directly-in-your-browser)

### Splash
<blockquote class="twitter-tweet" data-media-max-width="560"><p lang="en" dir="ltr">Deployed a new fluid simulation - &quot;Splash&quot;! <br>- Cleaner fluid surface thanks to Narrow-Range Filter<br>- Shadows using ray marching (particles mode only)<br>- More interaction (see the video)<br><br>Enjoy!<br><br>demo: <a href="https://t.co/F00L9XiD7b">https://t.co/F00L9XiD7b</a><br>repo: <a href="https://t.co/Zqxy4QDnAc">https://t.co/Zqxy4QDnAc</a> <a href="https://t.co/tqv8WTcIfw">pic.twitter.com/tqv8WTcIfw</a></p>&mdash; matsuoka-601 (@matsuoka_601) <a href="https://twitter.com/matsuoka_601/status/1902990065737011336?ref_src=twsrc%5Etfw">March 21, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

WebGPU-Ocean をさらに発展させた流体シミュレーションです．2018 年に提案された Narrow-Range Filter という手法を用いて，流体表面をより美しくレンダリングし，さらにレイマーチングによる影の表現も行いました．パフォーマンスもさらに向上させ，GPU によってはブラウザ上で 100 万粒子規模のリアルタイムシミュレーションも可能です．
- **デモ** : [Splash](https://splash-fluid.netlify.app/)
- **GitHub** : [Splash](https://github.com/matsuoka-601/Splash)
- **解説記事** : [Splash: A Real-Time Fluid Simulation in Browsers Implemented in WebGPU](https://www.reddit.com/r/GraphicsProgramming/comments/1jh3pd2/splash_a_realtime_fluid_simulation_in_browsers/)

### Wasm-Slime
<img src="https://raw.githubusercontent.com/matsuoka-601/Wasm-Slime/refs/heads/main/img/demo.gif">

Rust + wasm-bindgen-rayon を用いて，ブラウザ上で動作する並列流体シミュレーションを実装しました．マルチスレッドによる並列化により，シングルスレッドだけで達成するのが困難なスケールのシミュレーションを実現しました．
- **デモ** : [Wasm-Slime](https://fluid-simulation-test.netlify.app/)
- **GitHub** : [Wasm-Slime](https://github.com/matsuoka-601/wasm-slime)
- **解説記事** : [ブラウザ上でヌルヌル動作する流体シミュレーションを Rust + wasm-bindgen-rayon で実装する](https://zenn.dev/sparkle/articles/8f9fb109c0d5aa)

### Coupling of fluid & softbody simulation (WIP)

<img src="assets/imgs/buoyancy.gif">

Position Based Dynamics という手法を用いて，流体とソフトボディを融合したシミュレーションを実装することに挑戦しています．
## Articles
作った作品に関する技術の発信を，英語・日本語を問わず行っています．
### [WebGPU Fluid Simulations: High Performance & Real-Time Rendering](https://tympanus.net/codrops/2025/02/26/webgpu-fluid-simulations-high-performance-real-time-rendering/)

ハイパフォーマンスな 3D 流体シミュレーションをブラウザ上で実現するために用いた技術について，Codrops という企業から依頼をいただき書いた記事です．記事の紹介ツイートは 2000 いいねを超えるなど，話題になりました．

<div style="display: flex; justify-content: center;">

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">When <a href="https://twitter.com/matsuoka_601?ref_src=twsrc%5Etfw">@matsuoka_601</a> dropped his WebGPU fluid simulation demos, they left everyone in awe—pushing the limits of what&#39;s possible in the browser with breathtaking realism and incredible performance. 💦<br><br>Now, he&#39;s been kind enough to take us behind the scenes, breaking down the magic… <a href="https://t.co/YBnABYnpFS">pic.twitter.com/YBnABYnpFS</a></p>&mdash; Codrops (@codrops) <a href="https://twitter.com/codrops/status/1894642198165299391?ref_src=twsrc%5Etfw">February 26, 2025</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

</div>

### [Splash: A Real-Time Fluid Simulation in Browsers Implemented in WebGPU](https://www.reddit.com/r/GraphicsProgramming/comments/1jh3pd2/splash_a_realtime_fluid_simulation_in_browsers/)

作品の 1 つである [Splash](https://github.com/matsuoka-601/Splash) を紹介するために，英語掲示板である reddit に書いた記事です．1400 以上の upvote をいただき，[r/GraphicsProgramming というサブレディットの中で歴代 5 番目に注目された記事](https://www.reddit.com/r/GraphicsProgramming/top/?t=all)となっています（2025/05/25 現在）．

<blockquote class="reddit-embed-bq" style="height:500px" data-embed-height="584"><a href="https://www.reddit.com/r/GraphicsProgramming/comments/1jh3pd2/splash_a_realtime_fluid_simulation_in_browsers/">Splash: A Real-Time Fluid Simulation in Browsers Implemented in WebGPU</a><br> by<a href="https://www.reddit.com/user/matsuoka-601/">u/matsuoka-601</a> in<a href="https://www.reddit.com/r/GraphicsProgramming/">GraphicsProgramming</a></blockquote><script async="" src="https://embed.reddit.com/widgets.js" charset="UTF-8"></script>

### Zenn
Zenn にも積極的に記事を投稿しています．

- [ブラウザ上でヌルヌル動作する流体シミュレーションを Rust + wasm-bindgen-rayon で実装する](https://zenn.dev/sparkle/articles/8f9fb109c0d5aa)
- [WebGPU で実装したリアルタイム 3D 流体シミュレーションの紹介](https://zenn.dev/sparkle/articles/217cc2bb44fd9e)
- [WebGPU で MLS-MPM を実装し，ブラウザ上で 10 万粒子規模のリアルタイムシミュレーションを実現する](https://zenn.dev/sparkle/articles/3eb1225f891a87)
- [爆速な素数判定の怪](https://zenn.dev/sparkle/articles/f76ebe29e093e2)

## Skills
### WebGPU (WGSL)
WGSL のコンピュートシェーダーを用いて，GPGPU を用いた，ブラウザ上で動作する大規模な物理シミュレーションを作ってきました．
- [WebGPU-Ocean](https://github.com/matsuoka-601/WebGPU-Ocean)
- [Splash](https://github.com/matsuoka-601/Splash)
- [WaterBall](https://github.com/matsuoka-601/WaterBall)

WebGL では難しかった GPGPU 最適化の中には，WebGPU のコンピュートシェーダーのおかげで書きやすくなっているものが多くあります．そのため，将来的には，WebGPU によってブラウザ上でできることの幅が大きく広がりうると予想しています．

### SIMD を用いた高速化
プログラムの高速化のコンペティションサイトである [highload.fun](https://highload.fun/) に趣味で参加しています．AVX2 という SIMD の命令セットを用いて，プログラムを極限まで高速化することに挑戦しています．以下が成績の一部です（いずれも 2025/05/25 時点）．

- [Parse Integers](https://highload.fun/tasks/1/leaderboard) : **3 位**（735 人中）
- [Unique Strings](https://highload.fun/tasks/2/leaderboard) : **3 位**（215 人中）
- [Format Integers](https://highload.fun/tasks/4/leaderboard) : **2 位**（69 人中）
- [Fizz Buzz](https://highload.fun/tasks/16/leaderboard) : **1 位**（68 人中）
- [Large Integer Multiplication](https://highload.fun/tasks/20/leaderboard) : **1 位**（42 人中）

最近では wasm の SIMD サポートも充実してきているため，SIMD 最適化されたシミュレーションやアプリケーションをブラウザ上で動かすことにも挑戦したいと考えています．

### 競技プログラミング
大学時代は，趣味として競技プログラミングをしていました．データ構造やアルゴリズムに関する知識を応用して，問題を解くのが好きです（アカウント : [SPARKLE](https://atcoder.jp/users/SPARKLE)）．

### TypeScript
ここまでに紹介した，ブラウザ上のアプリケーションはすべて TypeScript で実装しています．

### Rust
Rust と wasm-bindgen-rayon を用いて，ブラウザ上で動作する並列流体シミュレーションを実装しました．[紹介記事はこちら](https://zenn.dev/sparkle/articles/8f9fb109c0d5aa)

### C++
競技プログラミングや highload.fun のコンペティションには C++ で参加しています．