<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Usaha Risol</title>
    <style>
        body {
            background: linear-gradient(to right, #ffafbd, #ffc3a0);
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 0;
            color: #333;
            overflow-x: hidden;
        }
        .blur {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: inherit;
            filter: blur(10px);
            z-index: -1;
        }
        .bubble {
            position: absolute;
            bottom: -100px;
            width: 20px;
            height: 20px;
            background-color: rgba(255, 255, 255, 0.6);
            border-radius: 50%;
            animation: rise 10s infinite ease-in;
            z-index: -1;
        }
        .bubble:nth-child(2) {
            width: 25px;
            height: 25px;
            left: 10%;
            animation-duration: 12s;
        }
        .bubble:nth-child(3) {
            width: 15px;
            height: 15px;
            left: 20%;
            animation-duration: 8s;
        }
        .bubble:nth-child(4) {
            width: 30px;
            height: 30px;
            left: 30%;
            animation-duration: 15s;
        }
        .bubble:nth-child(5) {
            width: 10px;
            height: 10px;
            left: 50%;
            animation-duration: 10s;
        }
        .bubble:nth-child(6) {
            width: 35px;
            height: 35px;
            left: 65%;
            animation-duration: 14s;
        }
        .bubble:nth-child(7) {
            width: 18px;
            height: 18px;
            left: 80%;
            animation-duration: 9s;
        }
        @keyframes rise {
            0% {
                bottom: -100px;
                transform: translateX(0);
            }
            50% {
                transform: translateX(20px);
            }
            100% {
                bottom: 100%;
                transform: translateX(-20px);
            }
        }
        header {
            background-color: rgba(255, 138, 101, 0.8);
            color: white;
            padding: 20px 0;
            text-align: center;
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            padding: 10px 0;
            background-color: rgba(255, 112, 67, 0.8);
        }
        nav a {
            color: white;
            text-decoration: none;
            font-size: 18px;
            transition: color 0.3s;
        }
        nav a:hover {
            color: #ff5722;
        }
        .container {
            padding: 20px;
            text-align: center;
            position: relative;
            z-index: 1;
        }
        footer {
            background-color: rgba(255, 112, 67, 0.8);
            color: white;
            padding: 10px 0;
            text-align: center;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
        .home, .menu, .order, .about, .public-services {
            display: none;
        }
        .active {
            display: block;
        }
        .menu-item {
            margin: 20px 0;
            padding: 10px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            display: inline-block;
            width: calc(33.333% - 40px);
            margin: 10px;
            vertical-align: top;
            cursor: pointer;
            transition: transform 0.3s;
        }
        .menu-item:hover {
            transform: scale(1.05);
        }
        .menu-item img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }
        .menu-item h3 {
            margin: 10px 0;
        }
        .menu-item p {
            margin: 5px 0;
        }
        .description {
            display: none;
            padding: 10px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 5px;
            margin-top: 10px;
        }
        form {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        form input, form select, form textarea {
            margin: 10px 0;
            padding: 10px;
            width: 80%;
            max-width: 400px;
            border: 2px solid #ff7043;
            border-radius: 5px;
        }
        form button {
            padding: 10px 20px;
            background-color: #ff7043;
            color: white;
            border: none;
            cursor: pointer;
            font-size: 16px;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        form button:hover {
            background-color: #ff5722;
        }
        .banner {
            width: 150%;
            height: 300px;
            background-image: url('https://i.pinimg.com/474x/67/08/fb/6708fbd42adf24f6f1605f5f9f20957d.jpg');
            background-size: cover;
            background-position: center;
            position: relative;
            z-index: 0;
        }
        .decorative-element {
            width: 80px;
            height: 80px;
            background: rgba(255, 235, 238, 0.8);
            border: 5px solid rgba(255, 112, 67, 0.8);
            border-radius: 50%;
            position: absolute;
            z-index: -1;
        }
        .decorative-element:nth-child(1) {
            top: 20%;
            left: 10%;
        }
        .decorative-element:nth-child(2) {
            top: 40%;
            right: 15%;
        }
        .decorative-element:nth-child(3) {
            bottom: 20%;
            left: 5%;
        }
        .decorative-element:nth-child(4) {
            bottom: 30%;
            right: 10%;
        }
        @media (max-width: 400px) {
            nav a {
                font-size: 14px;
            }
            form input, form select, form textarea {
                width: 100%;
                max-width: 300px;
            }
            .menu-item {
                width: calc(50% - 20px);
            }
        }
    </style>
</head>
<body>
    <div class="blur"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="bubble"></div>
    <div class="Smoke"></div>
    <div class="border-radius"></div>
    <header>
        <h1>RISOL MBAK DINI</h1>
    </header>
    <nav>
        <a href="#" onclick="showPage('home')">Home</a>
        <a href="#" onclick="showPage('menu')">Menu</a>
        <a href="#" onclick="showPage('order')">Pesan</a>
        <a href="#" onclick="showPage('about')">Tentang Kami</a>
        <a href="#" onclick="showPage('public-services')">Kritik dan Saran</a>
    </nav>
    <div id="home" class="container home active">
        <div class="banner"></div>
        <h2>Selamat Datang di Risol Buk Dini</h2>
        <p>Tempat terbaik untuk menemukan risol lezat dengan berbagai macam isian.</p>
    </div>
    <div id="menu" class="container menu">
        <h2>Menu</h2>
        <div class="menu-item" onclick="toggleDescription(this)">
            <img src="https://example.com/img/risol_mayo.jpg" alt="Risol Mayo">
            <h3>Risol Mayo</h3>
            <p>Harga: Rp 15.000</p>
            <div class="description">
                <p>Risol isi mayonaise, telur, dan daging yang lezat.</p>
            </div>
        </div>
        <div class="menu-item" onclick="toggleDescription(this)">
            <img src="https://example.com/img/risol_ayam.jpg" alt="Risol Ayam">
            <h3>Risol Ayam</h3>
            <p>Harga: Rp 15.000</p>
            <div class="description">
                <p>Risol dengan isian ayam yang gurih dan lezat.</p>
            </div>
        </div>
        <div class="menu-item" onclick="toggleDescription(this)">
            <img src="https://example.com/img/risol_sayur.jpg" alt="Risol Sayur">
            <h3>Risol Sayur</h3>
            <p>Harga: Rp 15.000</p>
            <div class="description">
                <p>Risol dengan berbagai macam sayuran segar.</p>
            </div>
        </div>
    </div>
    <div id="order" class="container order">
        <h2>Pesan Sekarang</h2>
        <form id="orderForm">
            <input type="text" id="nama" placeholder="Nama" required>
            <input type="text" id="alamat" placeholder="Alamat" required>
            <input type="text" id="nohp" placeholder="No. HP" required>
            <textarea id="pesanan" placeholder="Pesanan (cth: 2 Risol Mayo, 3 Risol Ayam)" required></textarea>
            <button type="button" onclick="kirimPesanan()">Kirim Pesanan</button>
        </form>
    </div>
    <div id="about" class="container about">
        <h2>Tentang Kami</h2>
        <p>Risol Buk Dini berdiri sejak 2020 dan terus berkembang hingga saat ini. Kami menyajikan risol dengan bahan berkualitas tinggi dan resep rahasia turun-temurun.</p>
        <p>kakak bisa datang langsung ke usaha kami, sebelah selatan jembatan Ki Ronggo RBA Bondowoso</p>
    </div>
    <div id="public-services" class="container public-services">
        <h2>Kritik dan Saran</h2>
        <form>
            <textarea placeholder="Tulis kritik dan saran Anda di sini"></textarea>
            <button type="submit">Kirim</button>
        </form>
    </div>
    <footer>
        <p>&copy; 2023 Risol Buk Dini</p>
    </footer>
    <script>
        function showPage(page) {
            document.querySelectorAll('.container').forEach(container => {
                container.classList.remove('active');
            });
            document.getElementById(page).classList.add('active');
        }

        function toggleDescription(element) {
            const description = element.querySelector('.description');
            description.style.display = description.style.display === 'block' ? 'none' : 'block';
        }

        function kirimPesanan() {
            const nama = document.getElementById('nama').value;
            const alamat = document.getElementById('alamat').value;
            const nohp = document.getElementById('nohp').value;
            const pesanan = document.getElementById('pesanan').value;

            // Simpan data ke localStorage
            const orderData = {
                nama: nama,
                alamat: alamat,
                nohp: nohp,
                pesanan: pesanan
            };
            localStorage.setItem('orderData', JSON.stringify(orderData));

            const pesan = `Halo mbak Dini, saya ingin memesan:%0ANama: ${nama}%0AAlamat: ${alamat}%0ANo. HP: ${nohp}%0APesanan: ${pesanan}`;
            const whatsappUrl = `https://api.whatsapp.com/send?phone=+6285748772015&text=${pesan}`;
            window.open(whatsappUrl, '_blank');
        }

        // Fungsi untuk mengambil dan menampilkan data pesanan yang tersimpan
        function loadOrderData() {
            const orderData = JSON.parse(localStorage.getItem('orderData'));
            if (orderData) {
                document.getElementById('nama').value = orderData.nama;
                document.getElementById('alamat').value = orderData.alamat;
                document.getElementById('nohp').value = orderData.nohp;
                document.getElementById('pesanan').value = orderData.pesanan;
            }
        }

        // Panggil fungsi loadOrderData ketika halaman dimuat
        window.onload = loadOrderData;
    </script>
</body>
</html>
