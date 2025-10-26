# website-catering
indeks.html
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
      background: url('images/banner.jpg') center/cover no-repeat;
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
    footer {
      background-color: #0077b6;
      color: white;
      text-align: center;
      padding: 30px 0;
      margin-top: 50px;
    }
    .search-bar {
      max-width: 400px;
      margin: 30px auto;
    }
  </style>
</head>
<body>

<header>
  <img src="images/logo.png" alt="Logo Dapur Mama Hilda">
  <h1 class="fw-bold">DAPUR MAMA HILDA</h1>
  <p>Catering Lezat, Higienis, dan Terpercaya</p>
</header>

<div class="banner"></div>

<div class="container my-5">
  <h2 class="text-center mb-4 text-primary fw-semibold">Menu Kami</h2>

  <!-- Search Bar -->
  <div class="search-bar text-center">
    <input type="text" id="searchInput" class="form-control" placeholder="Cari kategori atau nama menu...">
  </div>

  <div class="row g-4" id="menuContainer">
    <!-- Menu Cards -->
    <div class="col-md-4 menu-item" data-category="nasi box">
      <div class="card menu-card">
        <img src="images/nasi_ayam_bakar.jpg" alt="Nasi Ayam Bakar" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Nasi Ayam Bakar</h5>
          <p class="card-text">Nasi hangat dengan ayam bakar bumbu kecap, sambal, dan lalapan segar.</p>
          <p class="text-primary fw-semibold">Rp25.000</p>
        </div>
      </div>
    </div>

    <div class="col-md-4 menu-item" data-category="nasi box">
      <div class="card menu-card">
        <img src="images/nasi-rendang.jpg" alt="Nasi Rendang" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Nasi Rendang</h5>
          <p class="card-text">Nasi dengan rendang daging sapi empuk dan bumbu rempah khas Padang.</p>
          <p class="text-primary fw-semibold">Rp28.000</p>
        </div>
      </div>
    </div>

    <div class="col-md-4 menu-item" data-category="nasi box">
      <div class="card menu-card">
        <img src="images/nasi-uduk.jpg" alt="Nasi Uduk" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Nasi Uduk</h5>
          <p class="card-text">Nasi uduk gurih dengan telur balado, bihun goreng, dan tempe orek.</p>
          <p class="text-primary fw-semibold">Rp22.000</p>
        </div>
      </div>
    </div>

    <div class="col-md-4 menu-item" data-category="prasmanan">
      <div class="card menu-card">
        <img src="images/prasmanan.jpg" alt="Paket Prasmanan" class="card-img-top">
        <div class="card-body">
          <h5 class="card-title fw-bold">Paket Prasmanan</h5>
          <p class="card-text">Nasi putih, ayam rica, sayur asem, sambal, dan buah potong segar.</p>
          <p class="text-primary fw-semibold">Rp35.000/porsi</p>
        </div>
      </div>
    </div>
  </div>
</div>

<footer>
  <h5>Hubungi Kami</h5>
  <p>WhatsApp: <a href="https://wa.me/6281234567890" class="text-white fw-bold" target="_blank">+62 812-3456-7890</a></p>
  <p>Instagram: <a href="https://instagram.com/dapurmamahilda" class="text-white">@dapurmamahilda</a></p>
  <p>© 2025 Dapur Mama Hilda. Semua Hak Dilindungi.</p>
</footer>

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
<script>
  const searchInput = document.getElementById('searchInput');
  const menuItems = document.querySelectorAll('.menu-item');

  searchInput.addEventListener('keyup', function() {
    const searchValue = this.value.toLowerCase();
    menuItems.forEach(item => {
      const category = item.getAttribute('data-category').toLowerCase();
      const title = item.querySelector('.card-title').textContent.toLowerCase();
      if (category.includes(searchValue) || title.includes(searchValue)) {
        item.style.display = '';
      } else {
        item.style.display = 'none';
      }
    });
  });
</script>
</body>
</html>
