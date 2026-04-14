<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Harga Barang Disnaker - Referensi Harga Kebutuhan Dasar</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #eb2525;
            --primary-dark: #1d4ed8;
            --secondary: #f8fafc;
            --accent: #10b981;
            --danger: #ef4444;
            --text-primary: #1e293b;
            --text-secondary: #64748b;
            --white: #ffffff;
            --shadow: 0 10px 25px rgba(0,0,0,0.1);
            --shadow-lg: 0 20px 40px rgba(0,0,0,0.15);
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--text-primary);
            background: linear-gradient(135deg, #f8fafc 0%, #e2e8f0 100%);
        }

        /* Header */
        .header {
            background: var(--white);
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            display: flex;
            align-items: center;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }

        .logo i {
            margin-right: 0.5rem;
            font-size: 2rem;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-menu a {
            text-decoration: none;
            color: var(--text-primary);
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-menu a:hover {
            color: var(--primary);
        }

        .search-box {
            position: relative;
            min-width: 300px;
        }

        .search-input {
            width: 100%;
            padding: 0.75rem 1rem 0.75rem 3rem;
            border: 2px solid #e2e8f0;
            border-radius: 50px;
            font-size: 1rem;
            transition: all 0.3s;
        }

        .search-input:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }

        .search-icon {
            position: absolute;
            left: 1rem;
            top: 50%;
            transform: translateY(-50%);
            color: var(--text-secondary);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: var(--white);
            padding: 4rem 2rem;
            text-align: center;
        }

        .hero-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            font-weight: 700;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.25rem;
            margin-bottom: 2rem;
            opacity: 0.9;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .stat-card {
            background: rgba(255,255,255,0.1);
            backdrop-filter: blur(10px);
            padding: 2rem;
            border-radius: 20px;
            text-align: center;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            display: block;
        }

        /* Main Content */
        .container {
            max-width: 1200px;
            margin: 4rem auto;
            padding: 0 2rem;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 3rem;
            background: linear-gradient(135deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        /* Price Cards */
        .price-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
            gap: 2rem;
        }

        .price-card {
            background: var(--white);
            border-radius: 20px;
            padding: 2rem;
            box-shadow: var(--shadow);
            transition: all 0.3s;
            border: 1px solid #f1f5f9;
        }

        .price-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-lg);
        }

        .category-badge {
            display: inline-block;
            padding: 0.25rem 1rem;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .category-peternak { background: linear-gradient(135deg, #f59e0b, #d97706); color: white; }
        .category-penebang { background: linear-gradient(135deg, #15803d, #166534); color: white; }
        .category-penambang { background: linear-gradient(135deg, #ea580c, #c2410c); color: white; }
        .category-petani { background: linear-gradient(135deg, #10b981, #059669); color: white; }
        .category-nelayan { background: linear-gradient(135deg, #0ea5e9, #0284c7); color: white; }
        .category-recycle { background: linear-gradient(135deg, #00ff95, #91ff00); color: white; }
        .category-penjahit { background: linear-gradient(135deg, #e5ff00, #ff00c8); color: white; }

        .price-item-name {
            font-size: 1.25rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: var(--text-primary);
        }

        .price-range {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
            margin-bottom: 1rem;
        }

        .price-details {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem;
            background: var(--secondary);
            border-radius: 12px;
            margin-top: 1rem;
        }

        .update-info {
            font-size: 0.9rem;
            color: var(--text-secondary);
            margin-top: 1rem;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .nav-menu {
                display: none;
            }

            .search-box {
                min-width: 200px;
            }

            .stats {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        /* Animation */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in-up {
            animation: fadeInUp 0.6s ease-out;
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="nav-container">
            <div class="logo">
                <i class="fas fa-balance-scale"></i>
                Disnaker Harga Barang
            </div>
            <ul class="nav-menu">
                <li><a href="#home">Beranda</a></li>
                <li><a href="#harga">Harga Barang</a></li>
            </ul>
            <div class="search-box">
                <i class="fas fa-search search-icon"></i>
                <input type="text" class="search-input" placeholder="Cari harga barang...">
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="hero-container fade-in-up">
            <h1>Referensi Harga Kebutuhan Dasar</h1>
            <p>Update harga barang kebutuhan pokok terkini dari Dinas Tenaga Kerja</p>
            <div class="stats">
                <div class="stat-card">
                    <span class="stat-number">0</span>
                    <span>Barang Tersedia</span>
                </div>  
            </div>
        </div>
    </section>

    <!-- Main Content -->
    <div class="container">
        <!-- Price Grid - No Filter Section -->
        <h2 class="section-title" id="harga">Daftar Harga Barang Terkini</h2>
        <div class="price-grid">
            <div class="price-card fade-in-up">
                <span class="category-badge category-peternak">Peternak Ayam</span>
                <div class="price-item-name">Chiken Fillet </div>
                <div class="price-range">$470</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div> 

            <div class="price-card fade-in-up">
                <span class="category-badge category-penebang">Penebang Pohon</span>
                <div class="price-item-name">Paket Kayu</div>
                <div class="price-range">$370</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-petani">Petani</span>
                <div class="price-item-name">Teh</div>
                <div class="price-range">$900</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-petani">Petani</span>
                <div class="price-item-name">Tebu</div>
                <div class="price-range">$470</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-petani">Petani</span>
                <div class="price-item-name">Jeruk</div>
                <div class="price-range">$400</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-petani">Petani</span>
                <div class="price-item-name">Cabe</div>
                <div class="price-range">$400</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-penambang">Penambang</span>
                <div class="price-item-name">Iron</div>
                <div class="price-range">450</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-penambang">Penambang</span>
                <div class="price-item-name">Copper</div>
                <div class="price-range">450</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>
            
            <div class="price-card fade-in-up">
                <span class="category-badge category-penambang">Penambang</span>
                <div class="price-item-name">Diamond</div>
                <div class="price-range">$850</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-nelayan">Nelayan</span>
                <div class="price-item-name">Ikan Tuna</div>
                <div class="price-range">$1.500</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-nelayan">Nelayan</span>
                <div class="price-item-name">Ikan Salmon</div>
                <div class="price-range">$1.500</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-recycle">Recycle</span>
                <div class="price-item-name">Glass</div>
                <div class="price-range">$350</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>

            <div class="price-card fade-in-up">
                <span class="category-badge category-penjahit">Penjahit</span>
                <div class="price-item-name">Cloth</div>
                <div class="price-range">$300</div>
                <div class="price-details">
                    <span><i class="fas fa-store"></i> 0/5000 Distributor</span>
                </div>
                <div class="update-info">
                    <i class="fas fa-clock"></i> Update: 14 April 2026
                </div>
            </div>


    <script>
        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Search functionality - Only search remains
        const searchInput = document.querySelector('.search-input');
        searchInput.addEventListener('input', function() {
            const searchTerm = this.value.toLowerCase();
            const cards = document.querySelectorAll('.price-card');
            
            cards.forEach(card => {
                const name = card.querySelector('.price-item-name').textContent.toLowerCase();
                const category = card.querySelector('.category-badge').textContent.toLowerCase();
                
                if (name.includes(searchTerm) || category.includes(searchTerm)) {
                    card.style.display = 'block';
                } else {
                    card.style.display = 'none';
                }
            });
        });

        // Intersection Observer for animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animationPlayState = 'running';
                }
            });
        });

        document.querySelectorAll('.fade-in-up').forEach(el => {
            observer.observe(el);
        });
    </script>
</body>
</html>
