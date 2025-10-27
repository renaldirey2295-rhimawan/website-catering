# website-catering

<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Dapur Mama Hilda</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body {
      background: linear-gradient(135deg, #e0f7fa, #ffffff);
      font-family: 'Poppins', sans-serif;
      color: #333;
    }
    header {
      background-color: #0077b6;
      color: white;
      padding: 20px 0;
      text-align: center;
      border-bottom: 4px solid #00b4d8;
    }
    header img {
      width: 90px;
      height: 90px;
      border-radius: 50%;
      object-fit: cover;
      margin-bottom: 10px;
      border: 3px solid #ffffff;
      box-shadow: 0 0 10px rgba(0,0,0,0.2);
    }
    .banner {
      width: 100%;
      height: 350px;
      background: url('https://images.unsplash.com/photo-1600891964599-f61ba0e24092?auto=format&fit=crop&w=1600&q=80') center/cover no-repeat;
      border-bottom: 4px solid #00b4d8;
    }
    .menu-card {
      border: none;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      transition: transform 0.3s ease;
    }
    .menu-card:hover {
      transform: scale(1.03);
    }
    .menu-card img {
      border-top-left-radius: 15px;
      border-top-right-radius: 15px;
      height: 180px;
      object-fit: cover;
    }
    .search-box {
      max-width: 400px;
      margin: 0 auto 30px;
    }
    footer {
      background-color: #0077b6;
      color: white;
      text-align: center;
      padding: 30px 0;
      margin-top: 50px;
    }
    #noResult {
      display: none;
      text-align: center;
      font-size: 18px;
      color: #888;
      margin-top: 30px;
    }
  </style>
</head>
<body>

<header>
  <img src="images/logo.webp" alt="Logo Dapur Mama Hilda">
  <h1 class="fw-bold">DAPUR MAMA HILDA</h1>
  <p>Catering Lezat, Higienis, dan Terpercaya</p>
</header>

<div class="banner"></div>

<div class="container my-5">
  <h2 class="text-center mb-4 text-primary fw-semibold">Menu Kami</h2>

  <!-- 🔍 Pencarian -->
  <div class="search-box">
    <input type="text" id="searchInput" class="form-control" placeholder="Cari menu berdasarkan nama atau kategori...">
  </div>

  <!-- 🔘 Tombol Filter -->
  <div class="text-center mb-4">
    <button class="btn btn-outline-primary filter-btn active" data-category="all">Semua</button>
    <button class="btn btn-outline-primary filter-btn" data-category="nasi">Nasi Box</button>
    <button class="btn btn-outline-primary filter-btn" data-category="prasmanan">Prasmanan</button>
    <button class="btn btn-outline-primary filter-btn" data-category="snack">Snack Box</button>
    <button class="btn btn-outline-primary filter-btn" data-category="minuman">Minuman</button>
  </div>

  <!-- 🍱 Daftar Menu -->
  <div class="row g-4" id="menu-list">
    <!-- NASI BOX -->
    <div class="col-md-4 menu-item" data-category="nasi">
      <div class="card menu-card">
        <img src="images/nasi_ayam_bakar.jpg" alt="Nasi Ayam Bakar" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Nasi Ayam Bakar</h5>
          <p class="card-text">Ayam bakar bumbu kecap manis, sambal, dan lalapan segar.</p>
          <p class="text-primary fw-semibold">Rp25.000</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 menu-item" data-category="nasi">
      <div class="card menu-card">
        <img src="images/nasi-rendang.jpeg" alt="Nasi Rendang" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Nasi Rendang</h5>
          <p class="card-text">Rendang daging sapi empuk dengan bumbu rempah khas Minang.</p>
          <p class="text-primary fw-semibold">Rp28.000</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 menu-item" data-category="nasi">
      <div class="card menu-card">
        <img src="images/nasi-uduk.jpeg" alt="Nasi Uduk Spesial" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Nasi Uduk Spesial</h5>
          <p class="card-text">Nasi uduk gurih, ayam goreng, sambal kacang, dan telur balado.</p>
          <p class="text-primary fw-semibold">Rp24.000</p>
        </div>
      </div>
    </div>
    <!-- PRASMANAN -->
    <div class="col-md-4 menu-item" data-category="prasmanan">
      <div class="card menu-card">
        <img src="images/prasmanan.jpeg" alt="Paket Prasmanan A" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Paket Prasmanan A</h5>
          <p class="card-text">Nasi putih, ayam rica, sayur asem, sambal, dan buah potong.</p>
          <p class="text-primary fw-semibold">Rp35.000/porsi</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 menu-item" data-category="prasmanan">
      <div class="card menu-card">
        <img src="images/prasmanan.jpeg" alt="Paket Prasmanan B" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Paket Prasmanan B</h5>
          <p class="card-text">Nasi putih, ayam kecap, tahu balado, sayur lodeh, dan kerupuk.</p>
          <p class="text-primary fw-semibold">Rp40.000/porsi</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 menu-item" data-category="prasmanan">
      <div class="card menu-card">
        <img src="images/prasmanan_c.jpg" alt="Paket Prasmanan C" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Paket Prasmanan C</h5>
          <p class="card-text">Nasi putih, ikan bakar, urap sayur, sambal matah, dan buah potong.</p>
          <p class="text-primary fw-semibold">Rp42.000/porsi</p>
        </div>
      </div>
    </div>
    <!-- SNACK BOX -->
    <div class="col-md-4 menu-item" data-category="snack">
      <div class="card menu-card">
        <img src="images/snack_box_a.jpg" alt="Snack Box A" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Snack Box A</h5>
          <p class="card-text">Kue lumpur, risoles mayo, pastel isi ayam, air mineral kecil.</p>
          <p class="text-primary fw-semibold">Rp18.000/box</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 menu-item" data-category="snack">
      <div class="card menu-card">
        <img src="images/snack_box_b.jpg" alt="Snack Box B" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Snack Box B</h5>
          <p class="card-text">Bolu kukus, lemper ayam, kroket kentang, air mineral kecil.</p>
          <p class="text-primary fw-semibold">Rp20.000/box</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 menu-item" data-category="snack">
      <div class="card menu-card">
        <img src="images/snack_box_c.jpg" alt="Snack Box C" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Snack Box C</h5>
          <p class="card-text">Lapis legit, risoles sayur, donat tabur gula, air mineral.</p>
          <p class="text-primary fw-semibold">Rp22.000/box</p>
        </div>
      </div>
    </div>
    <!-- MINUMAN -->
    <div class="col-md-4 menu-item" data-category="minuman">
      <div class="card menu-card">
        <img src="images/es_teh_manis.jpg" alt="Es Teh Manis" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Es Teh Manis</h5>
          <p class="card-text">Minuman segar teh melati manis dingin.</p>
          <p class="text-primary fw-semibold">Rp5.000</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 menu-item" data-category="minuman">
      <div class="card menu-card">
        <img src="images/es_jeruk.jpg" alt="Es Jeruk Segar" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Es Jeruk Segar</h5>
          <p class="card-text">Perasan jeruk segar alami, tanpa bahan pengawet.</p>
          <p class="text-primary fw-semibold">Rp6.000</p>
        </div>
      </div>
    </div>
    <div class="col-md-4 menu-item" data-category="minuman">
      <div class="card menu-card">
        <img src="images/kopi_susu.jpg" alt="Kopi Susu Dingin" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Kopi Susu Dingin</h5>
          <p class="card-text">Kopi robusta pilihan dicampur susu manis, disajikan dingin.</p>
          <p class="text-primary fw-semibold">Rp10.000</p>
        </div>
      </div>
    </div>

  </div>

  <!-- 🚫 Pesan jika tidak ada hasil -->
  <div id="noResult">Menu tidak ditemukan 😔</div>
</div>

<footer>
  <h5>Hubungi Kami</h5>
  <p>WhatsApp: <a href="https://wa.me/6281281948632" class="text-white fw-bold" target="_blank">+62 812-8194-8632</a></p>
  <p>Instagram: <a href="(https://www.instagram.com/renaldirey1?igsh=MXJnMGQxOTI4Ymx1dQ==)" class="text-white">@renaldirey1</a></p>
  <p>© 2025 Dapur Mama Hilda. Semua Hak Dilindungi.</p>
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
<script>
  const filterButtons = document.querySelectorAll('.filter-btn');
  const menuItems = document.querySelectorAll('.menu-item');
  const searchInput = document.getElementById('searchInput');
  const noResult = document.getElementById('noResult');
  let currentCategory = 'all';

  filterButtons.forEach(button => {
    button.addEventListener('click', () => {
      currentCategory = button.getAttribute('data-category');
      filterButtons.forEach(btn => btn.classList.remove('active'));
      button.classList.add('active');
      applyFilter();
    });
  });

  searchInput.addEventListener('input', applyFilter);

  function applyFilter() {
    const searchTerm = searchInput.value.toLowerCase();
    let visibleCount = 0;

    menuItems.forEach(item => {
      const category = item.getAttribute('data-category');
      const text = item.innerText.toLowerCase();
      const matchCategory = currentCategory === 'all' || category === currentCategory;
      const matchSearch = text.includes(searchTerm);

      if (matchCategory && matchSearch) {
        item.style.display = 'block';
        visibleCount++;
      } else {
        item.style.display = 'none';
      }
    });

    noResult.style.display = visibleCount === 0 ? 'block' : 'none';
  }
</script>

</body>
</html>

images/
logo.webp
nasi_ayam_bakar.jpg
