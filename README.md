<div align="center">

<img src="docs/banner.svg" alt="Komponent Depo" width="100%">

<h3>A fast, colorful and completely free inventory app for your electronic parts</h3>

<p>
  <a href="https://cafu1107.github.io/komponent-depo/"><img src="https://img.shields.io/badge/▶_Live_Demo-8b5cf6?style=for-the-badge" alt="Live demo"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-22d3ee?style=for-the-badge" alt="MIT"></a>
  <img src="https://img.shields.io/badge/Dependencies-0-34d399?style=for-the-badge" alt="Zero dependencies">
  <img src="https://img.shields.io/badge/Single_file-HTML-ff5fa2?style=for-the-badge&logo=html5&logoColor=white" alt="Single HTML file">
</p>

<p>
  🇬🇧 <b>English</b> (default) &nbsp;·&nbsp; 🇹🇷 Türkçe &nbsp;·&nbsp; 🇩🇪 Deutsch
</p>

<b><a href="https://cafu1107.github.io/komponent-depo/">Try it now →</a></b> &nbsp;|&nbsp; <a href="#-türkçe">🇹🇷 Türkçe açıklama ↓</a>

<br><br>

<img src="docs/dark.png" alt="Komponent Depo — dark theme" width="92%">

</div>

---

## ✨ What can it do?

<table>
<tr>
<td width="50%" valign="top">

### 📷 Finds photos by itself
Type a part name (`ESP32`, `HC-SR04`, `BC547`…). The app searches **Wikipedia**, **Wikimedia Commons** and **Openverse**, picks the first photo that actually loads, and offers up to 12 alternatives.

</td>
<td width="50%" valign="top">

### 🎯 Photo editor
**Drag to center**, scroll to **zoom**, **rotate**, switch between *Fill* and *Fit*, and choose a backdrop color. The card shows exactly what you see in the editor.

</td>
</tr>
<tr>
<td valign="top">

### 🛒 Smart shopping list
Low and out-of-stock parts are listed automatically, with a suggested amount and estimated cost. Hit **“Bought”** to add them to your stock. Copy the list in one click.

</td>
<td valign="top">

### 📈 Stock history
Every increase and decrease is logged with a timestamp, so you can see what you used and when.

</td>
</tr>
<tr>
<td valign="top">

### 🌐 3 languages, 4 currencies
English by default. **Türkçe** and **Deutsch** are one click away in the top-right menu. ₺ · $ · € · £. Categories, dates and number formats follow the language you choose.

</td>
<td valign="top">

### 🔒 Your data stays with you
No server, no account. Everything is stored in your browser. Back it up as **JSON** or export it to **Excel (CSV)**.

</td>
</tr>
</table>

### …and more

| | |
|---|---|
| ⚡ **Fast quantity** | Hold − / + and the count speeds up. <kbd>Shift</kbd> changes it by 10, or click the number and type |
| 🧠 **Auto category** | Typing `BC547` selects *Transistor*, `DHT22` selects *Sensor* |
| 🔎 **Instant search** | Searches name, category, location, package and notes, and highlights the matches |
| ⭐ **Favorites & duplicate** | Star the parts you use often and clone a similar part in one click |
| ↩️ **Undo** | Bring back a part you deleted by mistake |
| ▦ **Card / list view** | Photo cards or a compact list |
| 🌗 **Dark / light theme** | Vivid violet-cyan palette and smooth animations |
| ⌨️ **Shortcuts** | <kbd>/</kbd> search · <kbd>N</kbd> new part · <kbd>Esc</kbd> close |

<div align="center">
<br>
<img src="docs/editor.png" alt="Photo editor" width="46%">&nbsp;&nbsp;
<img src="docs/light.png" alt="Light theme, Turkish" width="46%">
<br><sub>Automatic photo search & editor &nbsp;·&nbsp; Light theme (Türkçe)</sub>
</div>

---

## 🚀 Getting started

**Easiest:** open the [live demo](https://cafu1107.github.io/komponent-depo/) and start adding parts.

**On your own computer:** download [`index.html`](index.html) and double-click it. There's nothing to install. You only need internet to search for photos.

```bash
git clone https://github.com/Cafu1107/komponent-depo.git
cd komponent-depo
start index.html      # macOS: open index.html · Linux: xdg-open index.html
```

### 🔗 URL parameters

| Parameter | Example | What it does |
|---|---|---|
| `lang` | `?lang=tr` | Sets the language (`en` default, `tr`, `de`) |
| `theme` | `?theme=light` | Sets the theme (`dark`, `light`) |
| `add` | `?add=ESP32` | Opens the “New part” form with this name |

> 💡 Want to link parts to QR labels? Use a URL like `…/komponent-depo/?add=NE555`.

---

## 🛠️ How it's built

- **Single file:** HTML + CSS + vanilla JavaScript. No framework, no build step.
- **Storage:** `localStorage`. Uploaded photos are automatically shrunk to 800 px WebP to save space.
- **Photo sources:** [Wikipedia](https://www.wikipedia.org/), [Wikimedia Commons](https://commons.wikimedia.org/) and [Openverse](https://openverse.org/). All are open APIs and need no key.

## 🤝 Contributing

Bug reports, ideas and pull requests are welcome. To add a new language, add one block to the `I18N` object.

## 📄 License

[MIT](LICENSE). Free to use, modify and share.

---

<a id="-türkçe"></a>

## 🇹🇷 Türkçe

**Komponent Depo**, elektronik parçaların için hızlı, renkli ve tamamen ücretsiz bir depo uygulaması. Tek bir HTML dosyasından oluşur ve hiçbir kurulum gerektirmez.

**[Canlı demoyu Türkçe aç →](https://cafu1107.github.io/komponent-depo/?lang=tr)**

### ✨ Özellikler

- 📷 **Fotoğrafı kendisi bulur.** Parçanın adını yazarsın (`ESP32`, `HC-SR04`, `BC547`…). Uygulama Wikipedia, Wikimedia Commons ve Openverse'te arar, gerçekten açılan ilk fotoğrafı seçer ve 12'ye kadar seçenek sunar.
- 🎯 **Fotoğraf düzenleyici.** Fotoğrafı sürükleyerek ortalarsın. Yakınlaştırabilir, döndürebilir, *Doldur / Sığdır* arasında geçebilir, zemin rengini seçebilirsin.
- 🛒 **Akıllı alışveriş listesi.** Az kalan ve tükenen parçalar önerilen miktar ve tahmini tutarla listelenir. **“Aldım”** deyince stoğa eklenir.
- 📈 **Stok geçmişi.** Her artış ve azalış zamanıyla kaydedilir.
- ⚡ **Hızlı adet.** Butonu basılı tutunca adet hızlanarak değişir, <kbd>Shift</kbd> ile 10'ar değişir.
- 🧠 **Otomatik kategori.** `BC547` yazınca *Transistör* seçilir.
- 🔎 **Anlık arama.** Eşleşen yerleri vurgular.
- ⭐ **Favoriler, kopyalama ve ↩️ geri alma.**
- 🌐 **3 dil ve 4 para birimi.** Site varsayılan olarak English açılır. Sağ üstten **Türkçe** veya **Deutsch** seçilebilir, seçimin hatırlanır. Para birimi ₺ · $ · € · £ olabilir.
- 🌗 **Koyu ve açık tema.**
- 🔒 **Verin sende kalır.** Sunucu ve hesap yok, her şey tarayıcında saklanır. JSON olarak yedekleyebilir, Excel (CSV) olarak dışa aktarabilirsin.
- ⌨️ **Kısayollar:** <kbd>/</kbd> ara · <kbd>N</kbd> yeni parça · <kbd>Esc</kbd> kapat.

### 🚀 Kullanım

[Canlı demoyu](https://cafu1107.github.io/komponent-depo/?lang=tr) açıp hemen kullanmaya başlayabilirsin. Ya da [`index.html`](index.html) dosyasını indirip çift tıklayarak kendi bilgisayarında açabilirsin. Kurulum gerekmez, internet yalnızca fotoğraf aramak için gerekir.

Adres parametreleri: `?lang=tr` dili seçer, `?theme=light` açık temayı açar, `?add=ESP32` “Yeni parça” formunu bu adla açar.

### 🤝 Katkı ve lisans

Hata bildirimi, öneri ve pull request'lere açığım. Proje **MIT** lisanslıdır; özgürce kullanabilir, değiştirebilir ve paylaşabilirsin.

<div align="center">
<br>
<sub>🔧 Happy soldering! · Kolay gelsin, iyi lehimler!</sub>
</div>
