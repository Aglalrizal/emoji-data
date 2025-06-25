# 😎 Emoji Data API (Static JSON)

[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages-green?style=flat-square&logo=github)](https://aglalrizal.github.io/emoji-data/data/emojis.json)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

Repositori ini berisi data emoji dalam format JSON yang di-host secara publik menggunakan GitHub Pages. Cocok digunakan sebagai sumber data pada aplikasi front-end seperti pencari emoji, filter keyword, dan projek edukasi lainnya.

---

## 🌐 URL Data Publik

📦 **JSON URL**  
[`https://aglalrizal.github.io/emoji-data/data/emojis.json`](https://aglalrizal.github.io/emoji-data/data/emojis.json)

---

## 🧱 Struktur Data

```json
[
  {
    "title": "100",
    "symbol": "💯",
    "keywords": "hundred points symbol wow win perfect parties"
  },
  {
    "title": "Party Popper",
    "symbol": "🎉",
    "keywords": "celebration party birthday congrats yay"
  }
]
```

---

## 🧑‍💻 Contoh Penggunaan (JS/React)

🔹 Mengambil data dengan fetch:

```js
fetch("https://aglalrizal.github.io/emoji-data/data/emojis.json")
  .then((res) => res.json())
  .then((data) => {
    console.log("Emoji List:", data);
  });
```

🔹 Dengan Axios (React):

```js
import axios from "axios";
import { useEffect, useState } from "react";

function App() {
  const [emojis, setEmojis] = useState([]);

  useEffect(() => {
    axios
      .get("https://aglalrizal.github.io/emoji-data/data/emojis.json")
      .then((res) => setEmojis(res.data))
      .catch((err) => console.error("Gagal ambil data emoji:", err));
  }, []);

  return (
    <ul>
      {emojis.map((emoji) => (
        <li key={emoji.title}>
          {emoji.symbol} - {emoji.title}
        </li>
      ))}
    </ul>
  );
}
```
---
