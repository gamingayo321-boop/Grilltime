# Grilltime
Menu
# Definisikan ulang seluruh konten HTML termasuk html_content, karena sebelumnya belum didefinisikan ulang

# Buat konten HTML dengan gambar base64
html_content = f"""<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Grill Time!</title>
  <style>
    body {{
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #fff8f0;
    }}
    header {{
      background-color: #8b0000;
      color: white;
      padding: 1rem;
    }}
    nav {{
      display: flex;
      justify-content: space-between;
      align-items: center;
    }}
    nav h1 {{
      margin: 0;
    }}
    nav ul {{
      list-style: none;
      display: flex;
      gap: 1rem;
    }}
    nav ul li a {{
      color: white;
      text-decoration: none;
    }}
    .hero {{
      position: relative;
      text-align: center;
    }}
    .hero img {{
      width: 100%;
      max-height: 400px;
      object-fit: cover;
    }}
    .hero-text {{
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      background: rgba(0, 0, 0, 0.5);
      padding: 1rem;
      border-radius: 8px;
    }}
    .menu, .order, .contact {{
      padding: 2rem;
      text-align: center;
    }}
    .menu-container {{
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 1rem;
      margin-top: 1rem;
    }}
    .menu-item {{
      border: 1px solid #ccc;
      padding: 1rem;
      border-radius: 8px;
      width: 200px;
      background: #fff;
    }}
    .order-btn {{
      display: inline-block;
      background-color: #8b0000;
      color: white;
      padding: 1rem 2rem;
      text-decoration: none;
      border-radius: 5px;
      margin-top: 1rem;
    }}
    footer {{
      text-align: center;
      background-color: #333;
      color: white;
      padding: 1rem;
      margin-top: 2rem;
    }}
  </style>
</head>
<body>
  <header>
    <nav>
      <h1>🔥 Grill Time!</h1>
      <ul>
        <li><a href="#menu">Menu</a></li>
        <li><a href="#order">Pesan</a></li>
        <li><a href="#contact">Kontak</a></li>
      </ul>
    </nav>
  </header>

  <section class="hero">
    <img src="data:image/jpeg;base64,{img_base64}" alt="BBQ Grill" />
    <div class="hero-text">
      <h2>Selamat Datang di Grill Time!</h2>
      <p>Sajian grill terbaik, langsung dari bara api ke meja Anda.</p>
    </div>
  </section>

  <section id="menu" class="menu">
    <h2>🍽️ Menu Favorit</h2>
    <div class="menu-container">
      <div class="menu-item">
        <h3>Steak Sapi</h3>
        <p>Daging sapi panggang dengan bumbu spesial.</p>
      </div>
      <div class="menu-item">
        <h3>Ayam BBQ</h3>
        <p>Ayam panggang dengan saus manis pedas.</p>
      </div>
      <div class="menu-item">
        <h3>Sosis Bakar</h3>
        <p>Sosis premium dibakar hingga juicy.</p>
      </div>
    </div>
  </section>

  <section id="order" class="order">
    <h2>📲 Pesan Sekarang!</h2>
    <p>Klik tombol di bawah untuk langsung pesan lewat WhatsApp:</p>
    <a href="https://wa.me/6281234567890" target="_blank" class="order-btn">Pesan via WhatsApp</a>
  </section>

  <section id="contact" class="contact">
    <h2>📍 Lokasi & Kontak</h2>
    <p>Grill Time! - Jl. Lezat No. 10, Jakarta</p>
    <p>☎️ 0812-3456-7890</p>
    <p>📧 grilltime@email.com</p>
  </section>

  <footer>
    <p>© 2025 Grill Time! All rights reserved.</p>
  </footer>
</body>
</html>
"""

# Simpan ke file HTML
html_file_path = "/mnt/data/index.html"
with open(html_file_path, "w", encoding="utf-8") as f:
    f.write(html_content)

html_file_path
