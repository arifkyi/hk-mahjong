# Hong Kong Mahjong 香港麻雀

[English](README.md) · [Bahasa Indonesia](README.id.md)

A complete Hong Kong mahjong game in a single HTML file. You play against three computer opponents. No installation, no dependencies, no internet connection. Download the file, double-click it, and play in any modern browser.

**Play online:** https://arifkyi.github.io/hk-mahjong/HK-Mahjong.html
**Download:** [`HK-Mahjong.html`](HK-Mahjong.html)

## Features

- Full 144-tile set drawn as inline SVG: characters 萬, dots 筒, bamboo 條, winds 東南西北, dragons 中發白, and 8 flower and season tiles
- Two views: a 3D table and a top-down view, switched with one button
- Interface in English and Indonesian, switched with one button
- Player names you can change, including your own
- Claim buttons show the actual tiles: the incoming tile is outlined in gold, and the tiles it would take from your hand light up when you hover or touch the button
- The tile you just drew sits apart at the right end of your hand
- The wall around the table shrinks as tiles are drawn
- Full faan 番 breakdown after every win, so you can check your own counting
- Minimum faan to win is selectable: 0, 1 or 3

## Rules implemented

Four sets plus one pair, or Seven Pairs, or Thirteen Orphans. Chow only from the player on your left; pung, kong and winning from anyone. Flowers are revealed and replaced automatically. Play stops when only the 14 dead wall tiles remain.

| Hand pattern | Faan |
|---|---|
| 雞糊 Chicken hand | 0 |
| 平糊 All chows | 1 |
| 花幺九 Mixed orphans | 1 (always with All pungs) |
| 對對糊 All pungs | 3 |
| 混一色 Mixed one suit | 3 |
| 小三元 Small dragons | 3 (+1 per dragon pung) |
| 七對子 Seven pairs | 4 (variant rule) |
| 大三元 Great dragons | 5 (+1 per dragon pung) |
| 小四喜 Small winds | 6 |
| 清一色 Pure one suit | 7 |

Limit hands 例牌 score on their own, with no wind, dragon or flower bonus added:

| Limit hand | Faan |
|---|---|
| 字一色 All honours | 10 |
| 清么九 All terminals | 10 |
| 九子連環 Nine gates | 10 |
| 坎坎糊 Four concealed pungs | 10 |
| 大四喜 Great winds | 13 |
| 十八羅漢 Four kongs | 13 |
| 十三么 Thirteen orphans | 13 |
| 天糊 / 地糊 Heavenly / earthly hand | 13 |
| 八仙過海 All eight flowers | 13 |

Bonus points: 正花 seat flower 1, 無花 no flowers 1, 一台花 complete flower or season set 2, 役牌 dragon pung 1 each, 門風 seat wind 1, 圈風 prevailing wind 1, 自摸 self-draw 1, 門前清 concealed hand 1, 槓上開花 replacement tile 1, 搶槓 robbing the kong 1, 海底撈月 last catch 1.

Values follow the [Hong Kong mahjong scoring rules](https://en.wikipedia.org/wiki/Hong_Kong_mahjong_scoring_rules) on Wikipedia. Tables and associations vary; the HKMA, for example, caps hands at 10 faan.

**Points:** points equal the faan value and everyone starts at 0. On a discard win only the discarder loses points; on a self-draw each of the other three loses points. Points are only a way of keeping score. There is no betting of any kind in this game.

## Security and integrity

This game is a single HTML file with no network access of any kind. Everything below is checkable by anyone.

**1. It works with the internet switched off.** Turn off your wifi, open the file, and play a full game. Nothing stops working, because nothing is ever fetched or sent.

**2. The file blocks its own network access.** The page carries a Content Security Policy that the browser enforces:

```
default-src 'none'; style-src 'unsafe-inline'; script-src 'unsafe-inline';
img-src 'none'; connect-src 'none'; font-src 'none'; frame-src 'none';
object-src 'none'; base-uri 'none'; form-action 'none'
```

`connect-src 'none'` means the browser itself refuses any outbound request from this page, whatever the code tries to do.

**3. Verify the file you have is the file I published.**

```
SHA-256  ee1e4c1f90220ee551f47f56cca601cf0c339f5064fb3d97c1c6684c004da18d
```

```bash
# macOS / Linux
shasum -a 256 HK-Mahjong.html
# Windows PowerShell
Get-FileHash HK-Mahjong.html -Algorithm SHA256
```

If your hash is different, the file has been modified and did not come from me.

**4. Independent antivirus scan.** Scanned by 59 antivirus engines on VirusTotal: **0 detections**.

[View the full report](https://www.virustotal.com/gui/file/ee1e4c1f90220ee551f47f56cca601cf0c339f5064fb3d97c1c6684c004da18d)

The report is tied to the SHA-256 above, so it describes exactly this file and nothing else.

**5. One official source.** The only official copies are this repository and the GitHub Pages link above. A copy received through WhatsApp, Telegram, a file-sharing site or any other channel is outside my control. Check the hash before trusting it.

**6. The code is readable.** It is never minified or obfuscated, and there are no encoded blobs. Open it in any text editor and read it.

## Privacy

The game stores two things in your own browser, using `localStorage`: your chosen interface language and the four player names. They stay on your device, are never transmitted, and you can clear them by clearing site data for the file. Nothing else is stored, and no analytics or tracking of any kind is present.

## How to play

1. A tile is drawn automatically on your turn. Click any tile in your hand to discard it.
2. When an opponent discards a tile you can use, buttons appear: 上 Chow, 碰 Pung, 槓 Kong, 食糊 Hu or 過 Pass.
3. Concealed kong 暗槓 and added kong 加槓 buttons appear on your own turn when available.
4. If the tile you drew completes your hand, a 自摸 Win button appears with the faan count.
5. Each name plate shows the seat wind and the seat number: 東 1, 南 2, 西 3, 北 4. That number is also the flower or season number that scores 正花 for that player.
6. The red tile in the middle is the round wind 圈風. It is the same for everyone and is not a seat.

## License

MIT License © 2026 Ahmad Rifky Idrus

## Credits

Made by Rifky, [rifky the lifestyle](https://www.youtube.com/@rifkythelifestyle) on YouTube.
If this is useful to you, you can support my work at [ko-fi.com/rifkythecyber](https://ko-fi.com/rifkythecyber).
