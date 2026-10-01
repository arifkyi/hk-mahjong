# Hong Kong Mahjong 香港麻雀

[Bahasa Indonesia](README.id.md) · [English](README.md)

Game mahjong Hong Kong lengkap dalam satu file HTML. Kamu bermain melawan tiga lawan komputer. Tanpa instalasi, tanpa dependensi, tanpa koneksi internet. Unduh filenya, klik dua kali, lalu main di browser apa saja.

**Main online:** https://arifkyi.github.io/hk-mahjong/HK-Mahjong.html
**Unduh:** [`HK-Mahjong.html`](HK-Mahjong.html)

## Fitur

- Set lengkap 144 tile digambar sebagai SVG: karakter 萬, lingkaran 筒, bambu 條, angin 東南西北, naga 中發白, serta 8 tile bunga dan musim
- Dua tampilan: meja 3D dan tampak atas, berpindah dengan satu tombol
- Antarmuka bahasa Indonesia dan Inggris, berpindah dengan satu tombol
- Nama pemain bisa diganti, termasuk namamu sendiri
- Tombol klaim menampilkan tilenya langsung: tile yang datang dari meja bergaris emas, dan tile dari tanganmu ikut menyala saat tombol disorot atau disentuh
- Tile yang baru kamu ambil berdiri terpisah di ujung kanan tangan
- Tembok di sekeliling meja menyusut seiring tile terambil
- Rincian faan 番 lengkap setiap kali ada yang menang, jadi kamu bisa mencocokkan hitunganmu sendiri
- Minimum faan untuk menang bisa dipilih: 0, 1 atau 3

## Aturan yang dipakai

Empat set ditambah satu pasangan, atau Seven Pairs, atau 13 Orphans. Chow hanya dari pemain di sebelah kirimu; pung, kong dan menang boleh dari siapa saja. Bunga dibuka dan diganti otomatis. Permainan berhenti ketika tersisa 14 tile dead wall.

| Kombinasi tangan | Faan |
|---|---|
| 雞糊 Tangan Ayam | 0 |
| 平糊 Semua Chow | 1 |
| 花幺九 Mixed Orphans | 1 (selalu ikut All Pungs) |
| 對對糊 Pung Semua | 3 |
| 混一色 Half Flush | 3 |
| 小三元 Tiga Naga Kecil | 3 (+1 per pung naga) |
| 七對子 Seven Pairs | 4 (aturan varian) |
| 大三元 Tiga Naga Besar | 5 (+1 per pung naga) |
| 小四喜 Empat Angin Kecil | 6 |
| 清一色 Full Flush | 7 |

Tangan limit 例牌 dihitung sendiri, tanpa tambahan bonus angin, naga, atau bunga:

| Tangan limit | Faan |
|---|---|
| 字一色 Semua Kehormatan | 10 |
| 清么九 Semua 1 & 9 | 10 |
| 九子連環 Sembilan Gerbang | 10 |
| 坎坎糊 Empat Pung Tertutup | 10 |
| 大四喜 Empat Angin Besar | 13 |
| 十八羅漢 Empat Kong | 13 |
| 十三么 13 Yatim | 13 |
| 天糊 / 地糊 Tangan Langit / Bumi | 13 |
| 八仙過海 Delapan Bunga | 13 |

Poin bonus: 正花 bunga kursi 1, 無花 tanpa bunga 1, 一台花 set bunga atau musim lengkap 2, 役牌 set naga 1 per set, 門風 angin kursi 1, 圈風 angin ronde 1, 自摸 ambil sendiri 1, 門前清 tangan tertutup 1, 槓上開花 pengganti kong 1, 搶槓 rebut kong 1, 海底撈月 tile terakhir 1.

Istilah baku seperti Full Flush, Half Flush, Ping Hu dan Zi Mo sengaja tidak diterjemahkan paksa, karena itulah sebutan yang dipakai pemain di meja.

Nilainya mengikuti [Hong Kong mahjong scoring rules](https://en.wikipedia.org/wiki/Hong_Kong_mahjong_scoring_rules) di Wikipedia. Tiap meja dan asosiasi bisa berbeda; HKMA misalnya memakai batas 10 faan.

**Poin:** poin sama dengan jumlah faan dan semua pemain mulai dari 0. Menang dari buangan, hanya pemain yang membuang yang kehilangan poin; menang ambil sendiri, ketiga lawan masing-masing kehilangan poin. Poin hanya untuk mencatat skor. Tidak ada unsur taruhan dalam bentuk apa pun di game ini.

## Keamanan dan keaslian file

Game ini satu file HTML tanpa akses jaringan sama sekali. Semua hal di bawah bisa diperiksa siapa pun.

**1. Tetap jalan walau internet dimatikan.** Matikan wifi, buka filenya, lalu main satu ronde penuh. Tidak ada yang berhenti bekerja, karena memang tidak ada apa pun yang diambil atau dikirim.

**2. File ini memblokir akses jaringannya sendiri.** Halaman membawa Content Security Policy yang dijalankan oleh browser:

```
default-src 'none'; style-src 'unsafe-inline'; script-src 'unsafe-inline';
img-src 'none'; connect-src 'none'; font-src 'none'; frame-src 'none';
object-src 'none'; base-uri 'none'; form-action 'none'
```

`connect-src 'none'` berarti browser sendiri yang menolak permintaan keluar dari halaman ini, apa pun yang dicoba oleh kodenya.

**3. Pastikan file yang kamu punya sama dengan yang saya terbitkan.**

```
SHA-256  ee1e4c1f90220ee551f47f56cca601cf0c339f5064fb3d97c1c6684c004da18d
```

```bash
# macOS / Linux
shasum -a 256 HK-Mahjong.html
# Windows PowerShell
Get-FileHash HK-Mahjong.html -Algorithm SHA256
```

Kalau hash kamu berbeda, berarti file itu sudah diubah dan bukan berasal dari saya.

**4. Pemindaian antivirus independen.** Dipindai oleh 59 mesin antivirus di VirusTotal: **0 deteksi**.

[Lihat laporan lengkapnya](https://www.virustotal.com/gui/file/ee1e4c1f90220ee551f47f56cca601cf0c339f5064fb3d97c1c6684c004da18d)

Laporan itu terikat pada SHA-256 di atas, jadi yang dijelaskan persis file ini dan bukan file lain.

**5. Satu sumber resmi.** Satu-satunya salinan resmi adalah repositori ini dan link GitHub Pages di atas. Salinan yang kamu terima lewat WhatsApp, Telegram, situs berbagi file, atau jalur lain berada di luar kendali saya. Periksa hashnya sebelum dipercaya.

**6. Kodenya bisa dibaca.** Tidak pernah diminify maupun diobfuscate, dan tidak ada blok sandi apa pun di dalamnya. Buka dengan editor teks apa saja lalu baca sendiri.

## Privasi

Game menyimpan dua hal di browser kamu sendiri, lewat `localStorage`: pilihan bahasa antarmuka dan keempat nama pemain. Keduanya tinggal di perangkatmu, tidak pernah dikirim ke mana pun, dan bisa dihapus dengan membersihkan data situs untuk file ini. Tidak ada data lain yang disimpan, dan tidak ada analytics atau pelacakan dalam bentuk apa pun.

## Cara bermain

1. Tile diambil otomatis di giliranmu. Klik salah satu tile di tanganmu untuk membuangnya.
2. Saat lawan membuang tile yang bisa kamu pakai, tombol aksi muncul: 上 Chow, 碰 Pong, 槓 Kong, 食糊 Hu atau 過 Lewati.
3. Tombol kong tertutup 暗槓 dan tambah kong 加槓 muncul di giliranmu kalau tersedia.
4. Kalau tile yang kamu ambil melengkapi tangan, tombol 自摸 Hu muncul beserta jumlah faannya.
5. Setiap plat nama menampilkan angin kursi dan nomor kursinya: 東 1, 南 2, 西 3, 北 4. Nomor itu sekaligus nomor bunga atau musim yang memberi 正花 bagi pemain tersebut.
6. Tile merah di tengah meja adalah angin ronde 圈風. Berlaku sama untuk semua pemain dan bukan kursi.

## Lisensi

MIT License © 2026 Ahmad Rifky Idrus

## Kredit

Dibuat oleh Rifky, [rifky the lifestyle](https://www.youtube.com/@rifkythelifestyle) di YouTube.
Kalau game ini bermanfaat, kamu bisa mendukung karya saya di [ko-fi.com/rifkythecyber](https://ko-fi.com/rifkythecyber).
