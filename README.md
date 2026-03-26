<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Investor Muda News - Berita saham, cryptocurrency, ekonomi global & politik Indonesia terkini. Analisis mendalam untuk investor muda.">
    <meta name="keywords" content="saham, crypto, bitcoin, ihsg, cryptocurrency, ekonomi indonesia, politik indonesia">
    <meta property="og:title" content="Investor Muda News | Saham & Crypto Terkini">
    <meta property="og:description" content="Berita pasar modal, crypto, dan ekonomi Indonesia terbaru.">
    <meta property="og:image" content="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEirha7BR1FwJG8pt7XQ-b5cNOqHM0A49lhGOMyan-vAyTMB5jVsuDWsxwiFjq7GhZbWEnxhcNmL2tqs5LezGASg6G1yBDh3s4voeV7pVH_KADviVZkE3zBph69Khbk83v7x6By1Y9YW5B1ZGGiSxfw6hF3t88Z9P4A-EVuVw2jNm5Zofoukcehv4DnkuBrd/s512/1000130602.png">
    <title>Investor Muda News • investormuda.com</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;display=swap">
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;display=swap');
        
        :root {
            --font-inter: 'Inter', system_ui, sans-serif;
        }
        
        * {
            font-family: 'Inter', system_ui, sans-serif;
        }
        
        body {
            background-color: #0a0a0a;
        }
        
        .ticker {
            animation: marquee 25s linear infinite;
        }
        
        @keyframes marquee {
            0% { transform: translateX(0); }
            100% { transform: translateX(-50%); }
        }
        
        .hero-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        
        .hero-card:hover {
            transform: translateY(-4px);
            box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.3);
        }
        
        .nav-link {
            position: relative;
            transition: all 0.3s ease;
        }
        
        .nav-link:after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: #22c55e;
            transition: all 0.3s ease;
        }
        
        .nav-link:hover:after {
            width: 100%;
        }
        
        .price-up {
            color: #22c55e;
        }
        
        .price-down {
            color: #ef4444;
        }
        
        .section-header {
            position: relative;
        }
        
        .section-header:after {
            content: '';
            position: absolute;
            width: 60px;
            height: 3px;
            background: linear-gradient(to right, #22c55e, #eab308);
            bottom: -6px;
            left: 0;
        }
        
        .lazy {
            opacity: 0;
            transition: opacity 0.4s ease;
        }
        
        .lazy.loaded {
            opacity: 1;
        }
    </style>
</head>
<body class="text-white">
    <!-- TOP MARKET TICKER (WAJIB - REAL-TIME CRYPTO + CURRENT OTHERS) -->
    <div class="bg-zinc-900 py-2 border-b border-zinc-800 overflow-hidden">
        <div class="max-w-screen-2xl mx-auto px-6">
            <div id="ticker-container" class="flex items-center gap-x-8 whitespace-nowrap text-sm font-medium overflow-hidden">
                <!-- JS akan isi secara dinamis -->
                <div class="flex items-center gap-x-8 ticker" id="ticker-content">
                    <!-- Dummy placeholder, akan diganti JS -->
                </div>
            </div>
        </div>
    </div>

    <!-- HEADER -->
    <header class="bg-zinc-950 border-b border-zinc-800 sticky top-0 z-50">
        <div class="max-w-screen-2xl mx-auto">
            <div class="flex items-center justify-between px-6 py-5">
                <!-- Logo -->
                <a href="https://investormuda.com" class="flex items-center gap-x-3">
                    <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEirha7BR1FwJG8pt7XQ-b5cNOqHM0A49lhGOMyan-vAyTMB5jVsuDWsxwiFjq7GhZbWEnxhcNmL2tqs5LezGASg6G1yBDh3s4voeV7pVH_KADviVZkE3zBph69Khbk83v7x6By1Y9YW5B1ZGGiSxfw6hF3t88Z9P4A-EVuVw2jNm5Zofoukcehv4DnkuBrd/s512/1000130602.png" 
                         alt="Investor Muda News" 
                         class="h-10 w-auto">
                    <div>
                        <h1 class="text-2xl font-semibold tracking-tighter">Investor Muda</h1>
                        <p class="text-xs text-emerald-400 -mt-1">NEWS</p>
                    </div>
                </a>

                <!-- Menu -->
                <nav class="hidden md:flex items-center gap-x-8 text-sm font-medium">
                    <a href="#" onclick="navigateToSection('home')" class="nav-link text-white hover:text-emerald-400">Home</a>
                    <a href="#" onclick="navigateToSection('saham')" class="nav-link text-white hover:text-emerald-400">Saham</a>
                    <a href="#" onclick="navigateToSection('crypto')" class="nav-link text-white hover:text-emerald-400">Crypto</a>
                    <a href="#" onclick="navigateToSection('ekonomi')" class="nav-link text-white hover:text-emerald-400">Ekonomi Global</a>
                    <a href="#" onclick="navigateToSection('politik')" class="nav-link text-white hover:text-emerald-400">Politik</a>
                </nav>

                <!-- Mobile menu button -->
                <button onclick="toggleMobileMenu()" class="md:hidden text-white">
                    <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                    </svg>
                </button>

                <!-- Right side -->
                <div class="flex items-center gap-x-4">
                    <div class="hidden sm:flex items-center bg-zinc-900 rounded-full px-4 py-1 text-xs font-medium">
                        <div class="w-2 h-2 bg-emerald-400 rounded-full animate-pulse mr-2"></div>
                        MARKET OPEN
                    </div>
                    <a href="https://x.com/ShunilChenk" target="_blank" 
                       class="text-zinc-400 hover:text-white transition-colors">
                        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
                            <path d="M18.901 1.153h3.68l-8.04 9.19L24 22.479h-7.406l-5.796-7.568-6.638 7.568H1.2l8.61-9.84L0 1.153h7.64l5.27 6.96L18.901 1.153z"/>
                        </svg>
                    </a>
                </div>
            </div>
            
            <!-- Mobile menu -->
            <div id="mobile-menu" class="hidden md:hidden px-6 pb-6 border-t border-zinc-800">
                <div class="flex flex-col gap-y-4 text-sm font-medium pt-4">
                    <a href="#" onclick="navigateToSection('home');toggleMobileMenu()" class="py-2">Home</a>
                    <a href="#" onclick="navigateToSection('saham');toggleMobileMenu()" class="py-2">Saham</a>
                    <a href="#" onclick="navigateToSection('crypto');toggleMobileMenu()" class="py-2">Crypto</a>
                    <a href="#" onclick="navigateToSection('ekonomi');toggleMobileMenu()" class="py-2">Ekonomi Global</a>
                    <a href="#" onclick="navigateToSection('politik');toggleMobileMenu()" class="py-2">Politik</a>
                </div>
            </div>
        </div>
    </header>

    <!-- HERO SECTION -->
    <section id="home" class="max-w-screen-2xl mx-auto px-6 pt-8 pb-12">
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">
            <!-- Big hero -->
            <div class="lg:col-span-8">
                <div class="relative rounded-3xl overflow-hidden hero-card group">
                    <img src="https://picsum.photos/id/1015/1200/680" 
                         alt="IHSG menguat" 
                         class="w-full h-[420px] object-cover lazy"
                         loading="lazy">
                    <div class="absolute inset-0 bg-gradient-to-t from-black/90 via-black/50 to-transparent"></div>
                    <div class="absolute bottom-0 left-0 p-8 text-left max-w-2xl">
                        <div class="inline-flex items-center gap-2 bg-emerald-500 text-white text-xs font-bold px-4 py-1.5 rounded-full mb-4">
                            <span class="relative flex h-3 w-3">
                                <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
                                <span class="relative inline-flex rounded-full h-3 w-3 bg-emerald-500"></span>
                            </span>
                            BREAKING
                        </div>
                        <h2 class="text-4xl md:text-5xl font-semibold leading-tight mb-4">
                            IHSG Ditutup Menguat 2,75% di 7.302, BBCA &amp; BBRI Pimpin Penguatan
                        </h2>
                        <p class="text-lg text-zinc-300 mb-6">
                            Pasar saham Indonesia melonjak di tengah optimisme investor asing dan stabilnya rupiah. Crypto juga ikut naik.
                        </p>
                        <div class="flex items-center gap-3 text-sm">
                            <span class="text-emerald-400">26 Maret 2026 • 11:15 WIT</span>
                            <span class="px-3 py-1 bg-white/10 rounded-full text-xs">SAHAM</span>
                        </div>
                    </div>
                    <div class="absolute top-6 right-6 bg-black/70 text-white text-xs px-3 py-1 rounded-2xl flex items-center gap-1">
                        <span class="text-emerald-400">LIVE</span>
                    </div>
                </div>
            </div>

            <!-- 3 small news -->
            <div class="lg:col-span-4 flex flex-col gap-4">
                <div class="flex gap-4 hero-card bg-zinc-900 rounded-3xl p-4 hover:bg-zinc-800 transition-all">
                    <img src="https://picsum.photos/id/201/280/180" alt="" class="w-28 h-20 object-cover rounded-2xl lazy" loading="lazy">
                    <div class="flex-1">
                        <h3 class="font-medium leading-tight line-clamp-3">Bitcoin Tembus $70.920, Investor Muda Mulai FOMO?</h3>
                        <p class="text-xs text-emerald-400 mt-3">Crypto • 45 menit lalu</p>
                    </div>
                </div>
                <div class="flex gap-4 hero-card bg-zinc-900 rounded-3xl p-4 hover:bg-zinc-800 transition-all">
                    <img src="https://picsum.photos/id/870/280/180" alt="" class="w-28 h-20 object-cover rounded-2xl lazy" loading="lazy">
                    <div class="flex-1">
                        <h3 class="font-medium leading-tight line-clamp-3">Inflasi AS Turun, Fed Diprediksi Tahan Suku Bunga</h3>
                        <p class="text-xs text-amber-400 mt-3">Ekonomi Global • 2 jam lalu</p>
                    </div>
                </div>
                <div class="flex gap-4 hero-card bg-zinc-900 rounded-3xl p-4 hover:bg-zinc-800 transition-all">
                    <img src="https://picsum.photos/id/1016/280/180" alt="" class="w-28 h-20 object-cover rounded-2xl lazy" loading="lazy">
                    <div class="flex-1">
                        <h3 class="font-medium leading-tight line-clamp-3">Prabowo Resmi Umumkan Tim Transisi, Pasar Respons Positif</h3>
                        <p class="text-xs text-rose-400 mt-3">Politik • 4 jam lalu</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- SECTION SAHAM (Fokus utama) -->
    <section id="saham" class="max-w-screen-2xl mx-auto px-6 py-12 border-t border-zinc-800">
        <div class="flex justify-between items-end mb-8">
            <div>
                <span class="uppercase text-emerald-400 text-xs font-bold tracking-widest">PRIORITAS</span>
                <h2 class="section-header text-3xl font-semibold">Saham Indonesia</h2>
            </div>
            <a href="#" class="flex items-center gap-2 text-sm text-emerald-400 hover:text-white">Lihat semua saham →</a>
        </div>

        <!-- Mini stock prices -->
        <div class="grid grid-cols-3 md:grid-cols-6 gap-4 mb-10">
            <div class="bg-zinc-900 rounded-3xl p-5 text-center">
                <p class="text-xs text-zinc-400">BBCA</p>
                <p class="text-2xl font-semibold mt-1">9.625</p>
                <p class="text-emerald-400 text-sm font-medium">+125 (+1,31%)</p>
                <span class="inline-block px-3 py-0.5 bg-emerald-400/10 text-emerald-400 text-xs rounded-2xl mt-3">Bullish</span>
            </div>
            <div class="bg-zinc-900 rounded-3xl p-5 text-center">
                <p class="text-xs text-zinc-400">BBRI</p>
                <p class="text-2xl font-semibold mt-1">4.780</p>
                <p class="text-emerald-400 text-sm font-medium">+90 (+1,92%)</p>
                <span class="inline-block px-3 py-0.5 bg-emerald-400/10 text-emerald-400 text-xs rounded-2xl mt-3">Bullish</span>
            </div>
            <div class="bg-zinc-900 rounded-3xl p-5 text-center">
                <p class="text-xs text-zinc-400">TLKM</p>
                <p class="text-2xl font-semibold mt-1">3.150</p>
                <p class="text-emerald-400 text-sm font-medium">+45 (+1,45%)</p>
                <span class="inline-block px-3 py-0.5 bg-emerald-400/10 text-emerald-400 text-xs rounded-2xl mt-3">Bullish</span>
            </div>
            <div class="bg-zinc-900 rounded-3xl p-5 text-center">
                <p class="text-xs text-zinc-400">ASII</p>
                <p class="text-2xl font-semibold mt-1">7.200</p>
                <p class="text-amber-400 text-sm font-medium">+30 (+0,42%)</p>
                <span class="inline-block px-3 py-0.5 bg-amber-400/10 text-amber-400 text-xs rounded-2xl mt-3">Neutral</span>
            </div>
            <div class="bg-zinc-900 rounded-3xl p-5 text-center">
                <p class="text-xs text-zinc-400">UNVR</p>
                <p class="text-2xl font-semibold mt-1">4.910</p>
                <p class="text-rose-400 text-sm font-medium">-40 (-0,81%)</p>
                <span class="inline-block px-3 py-0.5 bg-rose-400/10 text-rose-400 text-xs rounded-2xl mt-3">Bearish</span>
            </div>
            <div class="bg-zinc-900 rounded-3xl p-5 text-center">
                <p class="text-xs text-zinc-400">BMRI</p>
                <p class="text-2xl font-semibold mt-1">5.050</p>
                <p class="text-emerald-400 text-sm font-medium">+80 (+1,61%)</p>
                <span class="inline-block px-3 py-0.5 bg-emerald-400/10 text-emerald-400 text-xs rounded-2xl mt-3">Bullish</span>
            </div>
        </div>

        <!-- Berita saham -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
            <div class="bg-zinc-900 rounded-3xl overflow-hidden hover:scale-[1.02] transition-all">
                <img src="https://picsum.photos/id/1015/600/340" alt="" class="w-full h-48 object-cover lazy" loading="lazy">
                <div class="p-6">
                    <span class="text-emerald-400 text-xs">SAHAM • 1 jam lalu</span>
                    <h3 class="font-semibold text-xl mt-2 leading-tight">Bank Central Asia (BBCA) Catat Laba Bersih Rp 18 T di Q1 2026</h3>
                    <p class="text-zinc-400 text-sm mt-3 line-clamp-3">Analis memprediksi target harga BBCA naik ke Rp 10.500 dalam 12 bulan ke depan.</p>
                </div>
            </div>
            <div class="bg-zinc-900 rounded-3xl overflow-hidden hover:scale-[1.02] transition-all">
                <img src="https://picsum.photos/id/29/600/340" alt="" class="w-full h-48 object-cover lazy" loading="lazy">
                <div class="p-6">
                    <span class="text-emerald-400 text-xs">BREAKING • 3 jam lalu</span>
                    <h3 class="font-semibold text-xl mt-2 leading-tight">IHSG Ditopang Saham Big Caps, Asing Net Buy Rp 1,2 Triliun</h3>
                    <p class="text-zinc-400 text-sm mt-3 line-clamp-3">Investor asing kembali masuk ke pasar saham Indonesia.</p>
                </div>
            </div>
            <div class="bg-zinc-900 rounded-3xl overflow-hidden hover:scale-[1.02] transition-all">
                <img src="https://picsum.photos/id/201/600/340" alt="" class="w-full h-48 object-cover lazy" loading="lazy">
                <div class="p-6">
                    <span class="text-amber-400 text-xs">SAHAM • 5 jam lalu</span>
                    <h3 class="font-semibold text-xl mt-2 leading-tight">TLKM Siap Luncurkan 5G Massal, Saham Naik 1,45%</h3>
                    <p class="text-zinc-400 text-sm mt-3 line-clamp-3">Perusahaan telekomunikasi terbesar Indonesia optimis dengan ekspansi 5G.</p>
                </div>
            </div>
            <div class="bg-zinc-900 rounded-3xl overflow-hidden hover:scale-[1.02] transition-all">
                <img src="https://picsum.photos/id/870/600/340" alt="" class="w-full h-48 object-cover lazy" loading="lazy">
                <div class="p-6">
                    <span class="text-rose-400 text-xs">BEARISH • 7 jam lalu</span>
                    <h3 class="font-semibold text-xl mt-2 leading-tight">Harga Batu Bara Turun, Saham ADRO &amp; PTBA Tekanan Jual</h3>
                    <p class="text-zinc-400 text-sm mt-3 line-clamp-3">Komoditas energi masih lemah di pasar global.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- SECTION CRYPTO (Harga sudah dikoreksi ke data terkini) -->
    <section id="crypto" class="max-w-screen-2xl mx-auto px-6 py-12 bg-zinc-950 border-t border-b border-zinc-800">
        <div class="flex justify-between items-end mb-8">
            <div>
                <span class="uppercase text-emerald-400 text-xs font-bold tracking-widest">LIVE</span>
                <h2 class="section-header text-3xl font-semibold">Cryptocurrency</h2>
            </div>
            <div id="crypto-sentiment" class="flex items-center gap-2 text-sm bg-zinc-900 px-5 py-2 rounded-3xl">
                <!-- JS update -->
                <span class="font-medium">Market Sentiment:</span>
                <span id="sentiment-badge" class="px-4 py-1 bg-emerald-400 text-white text-xs rounded-2xl">Bullish</span>
            </div>
        </div>

        <!-- Live crypto prices (sudah dikoreksi ke harga sekarang) -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-10" id="crypto-prices">
            <!-- Diisi JS dengan harga real-time dari CoinGecko -->
        </div>

        <!-- Berita crypto -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
            <div class="bg-zinc-900 rounded-3xl overflow-hidden hover:scale-[1.02] transition-all">
                <img src="https://picsum.photos/id/1015/600/340" alt="" class="w-full h-48 object-cover lazy" loading="lazy">
                <div class="p-6">
                    <span class="text-emerald-400 text-xs">CRYPTO • 30 menit lalu</span>
                    <h3 class="font-semibold text-xl mt-2 leading-tight">Bitcoin Capai $70.920, ETF Bitcoin Catat Rekor Inflow</h3>
                    <p class="text-zinc-400 text-sm mt-3 line-clamp-3">BTC naik 0,4% dalam 24 jam terakhir.</p>
                </div>
            </div>
            <div class="bg-zinc-900 rounded-3xl overflow-hidden hover:scale-[1.02] transition-all">
                <img src="https://picsum.photos/id/201/600/340" alt="" class="w-full h-48 object-cover lazy" loading="lazy">
                <div class="p-6">
             
