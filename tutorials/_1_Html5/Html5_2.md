

### 1. Temel HTML5 Sayfa Yapısı

```html
<!-- HTML5 standart yapısının başlangıç noktasıdır -->
<!DOCTYPE html>
<!-- HTML belgesinin başladığını belirtir -->
<html lang="tr">

<!-- Sayfa ile ilgili meta veriler, başlık vs. burada yer alır -->
<head>
  <!-- Karakter kodlaması: Türkçe karakterler için UTF-8 -->
  <meta charset="UTF-8">
  <!-- Sayfanın mobil uyumlu olmasını sağlar -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <!-- Tarayıcı sekmesinde görünen başlıktır -->
  <title>HTML5 Örnek Sayfa</title>
</head>

<!-- Sayfa içeriğinin yer aldığı ana bölüm -->
<body>
  <!-- Sayfanın görünen kısmı buraya yazılır -->
</body>

</html>
```

---

### 2. Başlık ve Paragraf Etiketleri

```html
<!-- H1 en büyük başlıktır. Sayfanın ana başlığı için kullanılır -->
<h1>HTML5 Eğitimi</h1>

<!-- Diğer başlık seviyeleri: h2, h3, ..., h6 -->
<h2>Giriş</h2>

<!-- Paragraf metni oluşturur -->
<p>HTML5, web sayfalarını yapılandırmak için kullanılan bir işaretleme dilidir.</p>
```

---

### 3. Bağlantı ve Görsel

```html
<!-- Başka bir sayfaya veya siteye bağlantı verir -->
<a href="https://www.google.com" target="_blank">Google'a Git</a>

<!-- Görsel eklemek için kullanılır -->
<img src="resim.jpg" alt="Açıklayıcı alternatif metin" width="200">
```

---

### 4. Listeleme Etiketleri

```html
<!-- Sırasız liste (madde işaretli) -->
<ul>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ul>

<!-- Sıralı liste (numaralı) -->
<ol>
  <li>Başlık ekle</li>
  <li>Paragraf yaz</li>
  <li>Bağlantı ver</li>
</ol>
```

---

HTML’de liste türleri ikiye ayrılır:

* **Düzenli liste (Ordered List)** → `<ol>`
* **Düzensiz liste (Unordered List)** → `<ul>`

Her birinin içinde listelenen öğeler `<li>` etiketiyle yazılır. Bu listelerin çeşitli **`attribute` (özellik)** değerleri vardır. Aşağıda her birini örneklerle ve açıklamalarıyla birlikte detaylı şekilde açıklıyorum.

---

## ✅ 1. DÜZENLİ LİSTE (Ordered List) – `<ol>`

### Temel Kullanım:

```html
<ol>
  <li>HTML</li>
  <li>CSS</li>
  <li>JavaScript</li>
</ol>
```

### 💡 Kullanılabilir `attribute`'lar:

#### ✔️ `type`: Sıralama stilini belirler

| Değer | Açıklama            | Görünüm    |
| ----- | ------------------- | ---------- |
| `1`   | Sayılar (default)   | 1, 2, 3    |
| `A`   | Büyük harfler       | A, B, C    |
| `a`   | Küçük harfler       | a, b, c    |
| `I`   | Roma rakamı (büyük) | I, II, III |
| `i`   | Roma rakamı (küçük) | i, ii, iii |

**Örnek:**

```html
<ol type="A">
  <li>Başlık</li>
  <li>İçerik</li>
</ol>
```

#### ✔️ `start`: Kaçtan başlayacağını belirler

```html
<ol type="1" start="5">
  <li>Beşinci</li>
  <li>Altıncı</li>
</ol>
```

#### ✔️ `reversed`: Listeyi tersten yazdırır

```html
<ol reversed>
  <li>Son</li>
  <li>Ortada</li>
  <li>İlk</li>
</ol>
```

---

## ✅ 2. DÜZENSİZ LİSTE (Unordered List) – `<ul>`

### Temel Kullanım:

```html
<ul>
  <li>Elma</li>
  <li>Armut</li>
  <li>Muz</li>
</ul>
```

### 💡 Kullanılabilir `attribute`:

#### ✔️ `type`: Madde işaretinin şeklini belirler

(HTML5’te artık önerilmez, CSS ile yapılması daha doğrudur)

| Değer    | Açıklama                   |
| -------- | -------------------------- |
| `disc`   | Dolu yuvarlak (varsayılan) |
| `circle` | Boş yuvarlak               |
| `square` | Kare kutu                  |

**Örnek:**

```html
<ul type="square">
  <li>Elma</li>
  <li>Armut</li>
</ul>
```

🟡 **Not:** HTML5’te `type` kullanımını doğrudan `ul` içinde kullanmak yerine CSS ile yapılması önerilir:

```html
<ul style="list-style-type: square;">
  <li>Elma</li>
  <li>Armut</li>
</ul>
```

---

## ✅ 3. Liste Öğesi (`<li>`) içinde `value` attribute (sadece `<ol>` için geçerli)

```html
<ol>
  <li value="10">Onuncu</li>
  <li>On birinci</li>
</ol>
```

Bu durumda `li` 10’dan başlar, sonra sıradaki 11 olur.

---

## 📌 Tüm Liste Özelliklerinin Örnekli Kullanımı

```html
<h2>Düzenli Liste (start, type, reversed)</h2>
<ol type="I" start="3" reversed>
  <li>Üçüncü</li>
  <li>İkinci</li>
  <li>Birinci</li>
</ol>

<h2>Düzensiz Liste (type)</h2>
<ul type="circle">
  <li>Kedi</li>
  <li>Köpek</li>
  <li>Balık</li>
</ul>

<h2>Liste İçinde Değer Atama (value)</h2>
<ol>
  <li value="5">Beşinci</li>
  <li>Altıncı</li>
</ol>
```

---

## 🎯 Liste Biçimlendirmede CSS ile Alternatif Özellikler

```css
ul {
  list-style-type: square;   /* disc, circle, none */
}

ol {
  list-style-type: upper-roman;  /* lower-alpha, decimal, etc. */
}
```






### 5. Tablo Yapısı

```html
<!-- Basit bir tablo oluşturur -->
<table border="1">
  <!-- Tablo başlığı -->
  <thead>
    <tr>
      <th>Ad</th>
      <th>Soyad</th>
    </tr>
  </thead>

  <!-- Tablo gövdesi -->
  <tbody>
    <tr>
      <td>Ali</td>
      <td>Yılmaz</td>
    </tr>
    <tr>
      <td>Ayla</td>
      <td>Demir</td>
    </tr>
  </tbody>
</table>
```

---

### 6. Form ve Giriş Alanları

```html
<!-- Basit bir form yapısı -->
<form action="/gonder" method="post">
  <!-- Kullanıcıdan metin girişi almak için -->
  <label for="ad">Adınız:</label>
  <input type="text" id="ad" name="ad" required>

  <!-- E-posta adresi girişi -->
  <label for="email">Email:</label>
  <input type="email" id="email" name="email">

  <!-- Renk seçici -->
  <label for="renk">Renk Seç:</label>
  <input type="color" id="renk" name="renk">

  <!-- Gönder butonu -->
  <button type="submit">Gönder</button>
</form>
```

---

### 7. Semantik HTML5 Etiketleri

```html
<!-- Sayfa başlığı bölgesi -->
<header>
  <h1>Haber Sitesi</h1>
</header>

<!-- Navigasyon menüsü -->
<nav>
  <ul>
    <li><a href="#">Anasayfa</a></li>
    <li><a href="#">Hakkımızda</a></li>
  </ul>
</nav>

<!-- Ana içerik bölgesi -->
<main>
  <!-- Bağımsız bir içerik bloğu -->
  <article>
    <h2>Yeni Gelişmeler</h2>
    <p>Bugün HTML5 hakkında yeni bilgiler öğreniyoruz.</p>
  </article>

  <!-- İçeriğe ek bilgi veya yan içerik -->
  <aside>
    <p>Yan menü veya reklam alanı.</p>
  </aside>
</main>

<!-- Sayfa alt bilgi alanı -->
<footer>
  <p>Telif Hakkı © 2025</p>
</footer>
```

---

### 8. Video ve Ses

```html
<!-- Video oynatıcı -->
<video controls width="320">
  <source src="video.mp4" type="video/mp4">
  Tarayıcınız video etiketini desteklemiyor.
</video>

<!-- Ses oynatıcı -->
<audio controls>
  <source src="ses.mp3" type="audio/mpeg">
  Tarayıcınız audio etiketini desteklemiyor.
</audio>
```

---

### 9. `<div>` ve `<span>`

```html
<!-- Div: blok elemandır, genellikle stil ve düzen için kullanılır -->
<div style="background-color: lightgray; padding: 10px;">
  <p>Bu bir div bloğudur.</p>
</div>

<!-- Span: satır içi elementtir, genellikle kısa içeriklerde stil vermek için -->
<p>Bu yazı <span style="color: red;">kırmızı</span> kelime içeriyor.</p>
```

---

### 10. `<br>`, `<hr>` ve Yorum Satırı

```html
<!-- Satır sonu (yeni satıra geçmek için) -->
Merhaba<br>Dünya

<!-- Yatay çizgi (içerikleri ayırmak için) -->
<hr>

<!-- HTML yorum satırı (tarayıcıda görünmez) -->
<!-- Bu bir açıklama satırıdır -->
```

 Aşağıda HTML5’te kullanılan bazı **biçimlendirici (formatter)** etiketleri olan `<b>`, `<i>`, `<big>`, `<small>`, `<mark>`, `<strong>`, `<em>` gibi öğeleri **örneklerle birlikte** detaylı olarak açıklıyorum.

Bu etiketler genellikle metinlerin **görsel vurgusunu** veya **anlamsal önemini** belirtmek için kullanılır.

---

## 1. `<b>` – Kalın (bold) yazı

**Anlamsal bir vurgusu yoktur**, sadece yazıyı görsel olarak kalınlaştırır.

```html
<p>Bu bir <b>kalın</b> kelimedir.</p>
```

📝 **Not:** Eğer metnin **önemli** olduğunu belirtmek istiyorsanız `<strong>` kullanmanız önerilir (aşağıda açıklanacak).

---

## 2. `<i>` – Eğik (italic) yazı

Yazıyı **eğik** yapar ancak yine **anlam belirtmez**. Genellikle teknik terimler, yabancı kelimeler veya düşünceler için kullanılır.

```html
<p><i>Carpe diem</i> bir Latince ifadedir.</p>
```

📝 **Not:** Anlamlı vurgu için `<em>` etiketi tercih edilmelidir.

---

## 3. `<strong>` – Güçlü vurgu

Yazıyı kalın yapar, ancak aynı zamanda **anlamsal olarak da önem** taşır. Ekran okuyucular buna vurgu yapar.

```html
<p><strong>Dikkat:</strong> Lütfen şifreyi unutmayın.</p>
```

🔊 **Erişilebilirlik açısından önerilen** etiket budur.

---

## 4. `<em>` – Vurgulu ifade (emphasis)

Yazıyı italik yapar ve **anlamsal vurguyu** belirtir. Yani yazının **vurgulu** okunması gerektiğini gösterir.

```html
<p>Ben <em>sadece</em> senin için geldim.</p>
```

---

## 5. `<mark>` – İşaretlenmiş metin (fosforlu)

Yazının **fosforlu kalemle işaretlenmiş gibi** görünmesini sağlar.

```html
<p>En önemli kelime <mark>burada</mark> yer alıyor.</p>
```

📌 Genellikle arama sonuçlarında, sınav açıklamalarında kullanılır.

---

## 6. `<small>` – Küçük yazı

Metni daha küçük puntoda gösterir. Dipnotlar veya açıklamalar için uygundur.

```html
<p>Bu bir metin <small>(küçük not)</small> içeriyor.</p>
```

---

## 7. `<big>` – Büyük yazı (HTML5’te artık kullanımı önerilmez)

Yazıyı bir miktar **büyütür**, ancak bu etiket **HTML5’te önerilmez** ve bazı tarayıcılarda desteklenmeyebilir.

```html
<p><big>Bu büyük yazıdır</big></p>
```

❌ HTML5 ile birlikte stil vermek için CSS önerilir:

```html
<span style="font-size: 1.5em;">Bu büyük yazıdır</span>
```

---

## 8. `<u>` – Altı çizili metin

Yazının altını çizer, ama **anlamsal vurgu taşımaz**.

```html
<p><u>Bu altı çizili metindir.</u></p>
```

🔎 Erişilebilirlik için `<ins>` veya CSS kullanımı önerilir.

---

## 9. `<sub>` ve `<sup>` – Alt ve üst simge

* `<sub>`: Alt simge (örneğin kimyasal formüller)
* `<sup>`: Üst simge (örneğin üs alma işlemleri)

```html
<p>H<sub>2</sub>O (su formülü)</p>
<p>2<sup>3</sup> = 8</p>
```

---

## 10. `<del>` ve `<ins>` – Silinmiş ve eklenmiş metin

* `<del>`: Silindiği anlamına gelir (üstü çizilir)
* `<ins>`: Eklendiği anlamına gelir (altı çizilir)

```html
<p>Fiyat: <del>100 TL</del> <ins>75 TL</ins></p>
```

---

## Karşılaştırmalı Örnek (hepsi bir arada):

```html
<p><strong>Uyarı:</strong> <em>Lütfen</em> <b>kural dışı</b> davranmayın. 
<mark>Bu çok önemli</mark>. Formül: H<sub>2</sub>O. 2<sup>3</sup> = 8.</p>
```

---

## Bonus: Biçimlendirme Etiketlerinin Anlamsal Karşılıkları

| Etiket     | Anlamsal mı? | Görsel Etki | Not                      |
| ---------- | ------------ | ----------- | ------------------------ |
| `<b>`      | ❌            | Kalın       | Görsel                   |
| `<strong>` | ✅            | Kalın       | Anlamsal vurgu           |
| `<i>`      | ❌            | Eğik        | Görsel                   |
| `<em>`     | ✅            | Eğik        | Vurgu                    |
| `<mark>`   | ✅            | Fosforlu    | Arama vurgusu için uygun |
| `<small>`  | ❌            | Küçük yazı  | CSS ile önerilir         |
| `<big>`    | ❌            | Büyük yazı  | KULLANILMASI ÖNERİLMEZ   |
| `<u>`      | ❌            | Altı çizili | CSS ile yap              |
| `<del>`    | ✅            | Üstü çizili | Silinmiş içerik          |
| `<ins>`    | ✅            | Altı çizili | Eklenmiş içerik          |

---
