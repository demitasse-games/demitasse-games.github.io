# demitasse-games.github.io

DEMITASSE Games の公開ページ。**プライバシーポリシーの掲載先。**

- PokerShiftRogue: `pokershiftrogue/privacy/index.html`
  → <https://demitasse-games.github.io/pokershiftrogue/privacy/>
- PokerShiftRogue の使用ソフトウェアの権利表記: `pokershiftrogue/licenses/index.html`
  → <https://demitasse-games.github.io/pokershiftrogue/licenses/>

## 直し方

**このリポジトリの HTML を手で直さない。** 文面はゲーム側のリポジトリの
`docs/privacy-policy.md` にあり、そこから機械で作っている。

```sh
cd <PokerShiftRogue>
python3 tool/gen_privacy_page.py
cp build/privacy/index.html <ここ>/pokershiftrogue/privacy/index.html
```

**書いてある内容と実装が食い違うのが、審査でも規約でもいちばん重い。**
写しを2つ持つと、片方だけ直したときに必ずずれる。

権利表記も同じ。Flutter がビルドのたびに作る `NOTICES` を原文のまま載せる
(ウェブ版のアプリからは外してあり、アプリからここへは飛ばさない)。

```sh
cd <PokerShiftRogue>
tool/install.sh web
python3 tool/gen_notices_page.py
cp build/notices/index.html <ここ>/pokershiftrogue/licenses/index.html
```
