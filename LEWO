<!DOCTYPE html>
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AKR SU ARITMA</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

  <style>
    /* YENİ RENK PALETİ */
    :root {
      --color-primary: #007B8A;       /* Ana Vurgu: Derin Turkuaz/Mavi */
      --color-secondary: #E5A84A;     /* İkincil Aksan: Kum Sarısı/Altın */
      --color-background-light: #F4F8F9; /* Açık Nötr: Gök Mavisi Nüansı */
      --color-text-dark: #2C3E50;     /* Koyu Metin: Mavi-Gri */
      --color-text-light: #eee;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      background: var(--color-background-light); /* Yeni Açık Arka Plan */
      color: var(--color-text-dark);
    }

    /* ÜST ALAN */
    .header-bg {
      background-image: url('sitem/images/akrsu1.jpg');
      background-size: cover;
      background-position: center;
      height: 420px;
      position: relative;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      align-items: center;
      overflow: hidden;
    }

    .header-bg::before {
      content: "";
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      /* Daha temiz bir geçiş */
      background: linear-gradient(to bottom, rgba(255,255,255,0.01), var(--color-background-light)); 
    }

    .marketing-text {
      position: absolute;
      top: 60px;
      text-align: center;
      color: white; /* Beyaz metin korundu */
      font-weight: 600;
      z-index: 2;
      text-shadow: 0 2px 10px rgba(0,0,0,0.6);
    }

    .marketing-text h2 { font-size: 2em; margin: 0; }
    .marketing-text p { font-size: 1.1em; margin: 5px 0 0; }

    .header-bg h1 {
      position: relative;
      z-index: 2;
      color: var(--color-text-dark); /* Koyu Metin */
      font-size: 2.4em;
      margin-bottom: 40px;
      text-transform: uppercase;
      text-align: center;
    }

    .slogan {
      text-align: center;
      font-size: 0.95em;
      color: #666; /* Gri tonu korundu */
      margin: 10px auto 40px;
      max-width: 90%;
      border-bottom: 2px solid #ccc;
      padding-bottom: 12px;
    }

    /* ÜRÜN LİSTESİ VE DETAY STİLLERİ */
    #urunListesi {
      max-width: 95%;
      margin: 0 auto 60px;
      background: var(--color-background); /* Saf Beyaz */
      border-radius: 20px;
      padding: 25px 15px;
      box-shadow: 0 4px 15px rgba(0,0,0,0.1);
    }

    .urun {
      background: white;
      border-radius: 16px;
      display: flex;
      align-items: center;
      padding: 12px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.08);
      margin-bottom: 18px;
      transition: 0.3s;
      cursor: pointer;
    }

    .urun img {
      width: 80px;
      height: 80px;
      border-radius: 10px;
      object-fit: contain;
      margin-right: 15px;
      border: 2px solid var(--color-primary); /* Yeni Mavi Çerçeve */
    }

    .urun-info h3 { margin: 0; font-size: 1.15em; color: var(--color-text-dark); }
    .urun-info small { color: #666; margin-top: 4px; display: block; }
    .urun-info p { 
        color: var(--color-primary); /* Fiyat Rengi Mavi */
        font-weight: bold; 
        font-size: 1.1em; 
        margin-top: 6px; 
    }

    .detay {
      max-width: 90%;
      margin: 30px auto;
      background: white;
      border-radius: 15px;
      padding: 20px;
      box-shadow: 0 3px 10px rgba(0,0,0,0.15);
      text-align: center;
    }

    .detay img { width: 100%; border-radius: 15px; margin-bottom: 15px; }

    button {
      background: var(--color-primary); /* Yeni Mavi Buton */
      color: white;
      border: none;
      padding: 10px 18px;
      border-radius: 10px;
      font-size: 1em;
      cursor: pointer;
      box-shadow: 0 2px 6px rgba(0,0,0,0.2);
      transition: background 0.3s ease;
    }

    button:hover { background: #005f6b; } /* Mavi Hover */

    /* YAZI ALANI İYİLEŞTİRMELERİ */
    #yaziAlani {
        max-width: 95%;
        margin: 40px auto; 
        padding: 20px;
        background: var(--color-background); /* Saf Beyaz */
        border-radius: 15px;
        box-shadow: 0 4px 12px rgba(0,0,0,0.08);
        line-height: 1.6; 
        color: #444;
    }

    #yaziAlani h2 {
        color: var(--color-primary); /* Yeni Mavi Başlık */
        font-size: 1.8em;
        text-align: center;
        margin-bottom: 25px;
    }

    #yaziAlani h3 {
        color: var(--color-text-dark); /* Koyu Metin Başlık */
        font-size: 1.3em;
        margin-top: 35px;
        margin-bottom: 15px;
        border-bottom: 1px dashed #e0e0e0;
        padding-bottom: 5px;
    }
    
    #yaziAlani ul {
        list-style-type: none; 
        padding-left: 0;
    }
    
    #yaziAlani ul li {
        margin-bottom: 10px;
        padding-left: 1.5em;
        text-indent: -1.5em; 
    }
    
    #yaziAlani ul li::before {
        content: "✔"; 
        color: var(--color-primary); /* Tik işaretleri Mavi */
        font-weight: bold;
        display: inline-block;
        width: 1.5em;
    }
    
    /* FOOTER (Üst Kısım) */
    .site-footer {
      background: var(--color-background); /* Saf Beyaz */
      text-align: center;
      padding: 50px 10px;
      margin-top: 50px;
      border-top: 3px solid var(--color-primary); /* Yeni Mavi Çizgi */
      color: var(--color-text-dark);
    }

    .footer-flex {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 40px;
    }

    .footer-flex > div {
        width: 90%; 
        max-width: 300px;
        margin-left: auto;
        margin-right: auto;
    }
    
    .site-footer .image-container { 
        width: 100%; 
        border: 3px solid var(--color-primary); /* Yeni Mavi Çerçeve */
        border-radius: 15px;
        padding: 0;
        margin: 0;
        overflow: hidden; 
    }

    .site-footer img {
      width: 100%; 
      height: auto;
      display: block;
      border-radius: 12px;
    }

    .footer-text, .product-description {
      margin-top: 15px;
      font-size: 1.1em;
      color: #555;
      line-height: 1.4em;
      font-weight: 500;
      margin-left: 0; 
      margin-right: 0;
    }

    .product-description {
      font-size: 1em;
      color: #666;
      margin-top: 5px;
    }

    .footer-title {
      margin-top: 15px;
      font-size: 1.7em;
      font-weight: 700;
      color: var(--color-text-dark);
    }

    /* YENİ ALT FOOTER STİLLERİ */
    .sub-footer {
        background: var(--color-text-dark); /* Koyu Mavi-Gri Arka Plan */
        color: var(--color-text-light);
        padding: 40px 10px;
        text-align: center;
        border-top: 1px solid #333;
    }

    .sub-footer .search-section {
        margin-bottom: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        gap: 10px;
    }

    .sub-footer .search-input {
        padding: 12px 15px;
        border: 1px solid #555;
        border-radius: 8px;
        font-size: 1em;
        width: 250px;
        background: #3c526a; /* Daha koyu arka plan */
        color: var(--color-text-light);
        outline: none;
    }

    .sub-footer .search-button {
        background: var(--color-primary); /* Mavi Buton */
        color: white;
        border: none;
        padding: 12px 20px;
        border-radius: 8px;
        font-size: 1em;
        cursor: pointer;
        transition: background 0.3s ease;
    }

    .sub-footer .search-button:hover {
        background: #005f6b;
    }

    .sub-footer .links-section {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        gap: 30px;
        margin-bottom: 40px;
    }

    .sub-footer .link-group {
        text-align: left;
        min-width: 150px;
    }

    .sub-footer .link-group h4 {
        color: var(--color-secondary); /* Yeni Altın Vurgu */
        font-size: 1.2em;
        margin-bottom: 15px;
    }

    .sub-footer .link-group ul {
        list-style: none;
        padding: 0;
        margin: 0;
    }

    .sub-footer .link-group ul li {
        margin-bottom: 8px;
    }

    .sub-footer .link-group ul li a {
        color: #ccc;
        text-decoration: none;
        font-size: 0.95em;
        transition: color 0.3s ease;
    }

    .sub-footer .link-group ul li a:hover {
        color: var(--color-secondary); /* Bağlantı Hover Altın */
    }

    .sub-footer .social-icons {
        margin-top: 20px;
        margin-bottom: 20px;
    }

    .sub-footer .social-icons a {
        color: var(--color-primary); /* Mavi İkonlar */
        font-size: 1.8em;
        margin: 0 12px;
        transition: color 0.3s ease;
    }

    .sub-footer .social-icons a:hover {
        color: var(--color-secondary); /* İkon Hover Altın */
    }

    .sub-footer .copyright {
        font-size: 0.85em;
        color: #888;
        margin-top: 30px;
    }

    @media (max-width: 600px) {
      .header-bg { height: 350px; }
      .header-bg h1 { font-size: 1.8em; }
      .marketing-text h2 { font-size: 1.6em; }
      
      .footer-flex > div {
          width: 90%; 
          max-width: 300px; 
      }

      .sub-footer .search-section {
          flex-direction: column;
          gap: 15px;
      }
      .sub-footer .search-input {
          width: 80%;
      }
      .sub-footer .link-group {
          width: 100%;
          text-align: center;
      }
    }
  </style>
</head>

<body>

  <div class="header-bg">
    <div class="marketing-text">
      <h2>AKR SU ARITMA</h2>
      <p>Geleceğin teknolojisiyle saf suyun gücü</p>
    </div>
    <h1>ÜRÜNLER</h1>
  </div>

  <p class="slogan">Sağlık, kalite ve güven: AKR Arıtma Sistemleri, evinizde mükemmel su deneyimi sunar.</p>

  <div id="icerik"></div>

  <div id="yaziAlani">
    <h2>💧 Su Arıtma Cihazları: Sağlık İçin Faydalı mı, Yoksa Riskli mi?</h2>
    
    <p>Son yıllarda, evlerimizde ve iş yerlerimizde *su arıtma cihazlarının popülerliği* hızla artmıştır. Şebeke suyunun kalitesi konusundaki endişeler, birçok kişiyi arıtılmış su tüketimine yönlendirmektedir. Peki, bu cihazlardan elde ettiğimiz su gerçekten sağlığımız için bir fayda sağlıyor mu, yoksa göz ardı edilen *potansiyel zararları* da mevcut mu?</p>

    <p>Günlük hayatımızın ayrılmaz bir parçası haline gelen arıtma suyunun, vücudumuz üzerindeki etkilerini anlamak büyük önem taşır. Bu cihazlar, suyu zararlı maddelerden, kirleticilerden ve mikroorganizmalardan temizleyerek *güvenli ve lezzetli* bir içme suyu sunar.</p>
    
    <h3>Faydaları ve Dikkat Edilmesi Gerekenler</h3>

    <p>Arıtma cihazları, suyun *klor, tortu, ağır metaller* ve diğer kimyasal kalıntılardan arındırılmasında etkilidir. Bu durum, özellikle şehir sularında yüksek düzeyde kirletici barındıran bölgelerde yaşayanlar için önemli bir *sağlık avantajı* sağlar.</p>
    
    <ul>
        <li>Zararlı maddelerden arınmış, güvenli içme suyu sağlar.</li>
        <li>Musluk suyunun tadını ve kokusunu iyileştirir.</li>
        <li>Böbrek taşı oluşumu riskini azaltmaya yardımcı olabilir (düşük mineral içeriği nedeniyle).</li>
    </ul>

    <p>Ancak, özellikle ters ozmoz (Reverse Osmosis - RO) sistemlerinde, suyun temizlenirken aynı zamanda *faydalı minerallerin (kalsiyum, magnezyum vb.)* de büyük ölçüde kaybedildiği bilinmektedir. Bu nedenle:</p>
    
    <ul>
        <li>Mineral dengesini korumak için *mineral filtresi (alkali filtre)* gibi ek aşamaları bulunan sistemler tercih edilmelidir.</li>
        <li>Cihazların *düzenli filtre değişimi* ve bakımı, arıtılmış suyun kalitesini sürekli yüksek tutmak ve olası *mikrobiyal riskleri* önlemek açısından hayati öneme sahiptir.</li>
    </ul>

    <p>Amacımız, bu yazıyla okuyucularımızın arıtma suyunun *faydaları* ile *uygulanması gereken doğru kullanım ve mineral takviyesi* konularında bilinçlenerek daha sağlıklı kararlar vermelerine yardımcı olmaktır.</p>

  </div>
  <script>
    const urunler = [
      { id: 1, isim: "SPACE", fiyat: "18.699 TL", aciklama: "Ultra premium model", resim: "sitem/images/Artboard-7-copy-4.png" },
      { id: 2, isim: "CLASSIC", fiyat: "5.999 TL", aciklama: "Ekonomik çözüm, giriş seviyesi", resim: "sitem/images/Artboard-7.png" },
      { id: 3, isim: "DIGITAL", fiyat: "5.999 TL", aciklama: "Modern dijital kontrol paneli", resim: "sitem/images/Artboard-7-copy-3.png" },
      { id: 4, isim: "RO SYSTEM", fiyat: "17.999 TL", aciklama: "Yüksek performanslı arıtma", resim: "sitem/images/Artboard-7-copy-2.png" },
      { id: 5, isim: "PRO II", fiyat: "11.899 TL", aciklama: "Kompakt tasarım, yüksek kalite", resim: "sitem/images/pro2.png" }
    ];

    const icerik = document.getElementById('icerik');

    function urunleriGoster() {
      icerik.innerHTML = '<div id="urunListesi"></div>'; 
      const liste = document.getElementById('urunListesi');

      urunler.forEach(u => {
        const div = document.createElement('div');
        div.className = 'urun';
        div.innerHTML = `
          <img src="${u.resim}" alt="${u.isim}">
          <div class="urun-info">
            <h3>${u.isim}</h3>
            <small>${u.aciklama}</small>
            <p>${u.fiyat}</p>
          </div>
        `;
        div.onclick = () => urunDetay(u);
        liste.appendChild(div);
      });
    }

    function urunDetay(u) {
      document.getElementById('yaziAlani').style.display = 'none'; // Detay açılınca yazı alanı gizlenir
      document.getElementById('icerik').innerHTML = `
        <div class="detay">
          <img src="${u.resim}" alt="${u.isim}">
          <h2>${u.isim}</h2>
          <p><strong>Açıklama:</strong> ${u.aciklama}</p>
          <p><strong>Fiyat:</strong> ${u.fiyat}</p>
          <button onclick="urunleriGoster(); document.getElementById('yaziAlani').style.display = 'block';">← Geri dön</button>
        </div>
      `;
    }
    
    urunleriGoster(); 
  </script>

  <footer class="site-footer">
    <div class="footer-flex">
      
      <div>
        <div class="image-container">
          <img src="sitem/images/Artboard-14-copy-2-100.jpg" alt="LG Purifier görseli">
        </div>
        <div class="footer-title">LG Purifier pH 8,5</div>
        <div class="product-description">
          Suyun kalitesini artırmak ve zararlı maddeleri, kirleticileri veya mikroorganizmaları temizlemek için kullanılır.
        </div>
      </div>

      <div>
        <div class="image-container">
          <img src="sitem/images/musluk-14-100-1.jpg" alt="İnox Musluk">
        </div>
        <div class="footer-title">Inox Musluk</div>
        <div class="footer-text">
          Orijinal Inox musluk, tıbbi malzemelerde kullanılan<br>
          304 kodlu paslanmaz çelikten üretiliyor.
        </div>
      </div>

    </div>
  </footer>

  <div class="sub-footer">
    <div class="search-section">
      <input type="text" placeholder="Sitede Arayın..." class="search-input">
      <button class="search-button">Ara</button>
    </div>

    <div class="links-section">
        <div class="link-group">
            <h4>Hızlı Bağlantılar</h4>
            <ul>
                <li><a href="#">Ana Sayfa</a></li>
                <li><a href="#">Ürünler</a></li>
                <li><a href="#">Hakkımızda</a></li>
                <li><a href="#">İletişim</a></li>
            </ul>
        </div>
        <div class="link-group">
            <h4>Ürün Kategorileri</h4>
            <ul>
                <li><a href="#">Su Arıtma Cihazları</a></li>
                <li><a href="#">Su Arıtma Filtreleri</a></li>
                <li><a href="#">Yedek Parçalar</a></li>
                <li><a href="#">Aksesuarlar</a></li>
            </ul>
        </div>
        <div class="link-group">
            <h4>Yardım & Destek</h4>
            <ul>
                <li><a href="#">Sıkça Sorulanlar</a></li>
                <li><a href="#">Servis Talebi</a></li>
                <li><a href="#">Garanti Koşulları</a></li>
                <li><a href="#">Kullanım Kılavuzları</a></li>
            </ul>
        </div>
    </div>

    <div class="social-icons">
      <a href="#" target="_blank" aria-label="Facebook"><i class="fab fa-facebook-f"></i></a>
      <a href="#" target="_blank" aria-label="Twitter"><i class="fab fa-twitter"></i></a>
      <a href="#" target="_blank" aria-label="Instagram"><i class="fab fa-instagram"></i></a>
      <a href="#" target="_blank" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
    </div>

    <div class="copyright">
      &copy; 2023 AKR Su Arıtma. Tüm Hakları Saklıdır. | So Good LG Purifier
    </div>
  </div>

</body>
</html>
