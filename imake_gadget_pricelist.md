<!DOCTYPE html>
<html lang="id" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>iMake Gadget - Pricelist Baterai & LCD</title>
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        dark: {
                            900: '#080808',
                            800: '#121212',
                            700: '#1e1e1e',
                            600: '#2a2a2a',
                            500: '#3f3f46'
                        }
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif']
                    }
                }
            }
        }
    </script>
    <!-- FontAwesome Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #080808;
            color: #f4f4f5;
        }
        ::-webkit-scrollbar {
            width: 8px;
            height: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #080808;
        }
        ::-webkit-scrollbar-thumb {
            background: #27272a;
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #3f3f46;
        }
        .glass-panel {
            background: rgba(18, 18, 18, 0.75);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.08);
        }
        .glass-card {
            background: rgba(30, 30, 30, 0.6);
            backdrop-filter: blur(8px);
            border: 1px solid rgba(255, 255, 255, 0.06);
            transition: all 0.25s ease-in-out;
        }
        .glass-card:hover {
            border-color: rgba(255, 255, 255, 0.25);
            transform: translateY(-2px);
            box-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.5);
        }
        .badge-warranty {
            background: linear-gradient(135deg, #ffffff 0%, #a1a1aa 100%);
            color: #000000;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col justify-between selection:bg-white selection:text-black">

    <!-- Navigation / Header -->
    <header class="sticky top-0 z-40 glass-panel border-b border-zinc-800">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex items-center justify-between h-20">
                <!-- Brand -->
                <div class="flex items-center space-x-3 cursor-pointer" onclick="switchCategory('all')">
                    <div class="w-10 h-10 rounded-xl bg-white text-black flex items-center justify-center font-bold text-2xl shadow-lg shadow-white/10">
                        <i class="fa-brands fa-apple"></i>
                    </div>
                    <div>
                        <div class="text-xl font-extrabold tracking-tight text-white flex items-center gap-2">
                            iMake <span class="font-light text-zinc-400">Gadget</span>
                        </div>
                        <p class="text-xs text-zinc-400 tracking-wider uppercase font-medium">Apple Service & Parts Specialist</p>
                    </div>
                </div>

                <!-- Warranty Highlight Banner -->
                <div class="hidden md:flex items-center bg-zinc-900 border border-zinc-700 px-4 py-2 rounded-full space-x-2">
                    <span class="inline-flex items-center justify-center w-5 h-5 rounded-full bg-white text-black font-bold text-xs">
                        <i class="fa-solid fa-shield-halved text-xs"></i>
                    </span>
                    <span class="text-xs font-semibold tracking-wide text-zinc-200">GARANSI 2 BULAN FULL COVER</span>
                </div>

                <!-- Action Button -->
                <div>
                    <a href="https://wa.me/6281234567890?text=Halo%20iMake%20Gadget,%20saya%20mau%20tanya%20pemasangan%20sparepart" 
                       target="_blank" 
                       class="inline-flex items-center space-x-2 bg-white hover:bg-zinc-200 text-black font-semibold px-4 py-2.5 rounded-xl transition-all duration-200 text-sm shadow-md hover:shadow-white/20">
                        <i class="fa-brands fa-whatsapp text-lg"></i>
                        <span class="hidden sm:inline">Konsultasi WA</span>
                    </a>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <main class="flex-grow max-w-7xl w-full mx-auto px-4 sm:px-6 lg:px-8 py-8 space-y-8">

        <!-- Hero Section -->
        <section class="text-center py-6 border-b border-zinc-800/80">
            <div class="inline-flex items-center gap-2 px-3 py-1.5 rounded-full bg-zinc-900 border border-zinc-800 text-zinc-300 text-xs font-medium mb-4">
                <i class="fa-solid fa-check-circle text-white"></i> Original Quality & Premium Replacement
            </div>
            <h1 class="text-3xl sm:text-5xl font-black tracking-tight text-white mb-3">
                Daftar Harga Baterai & LCD
            </h1>
            <p class="text-zinc-400 max-w-2xl mx-auto text-sm sm:text-base leading-relaxed">
                Transparan, Cepat & Terpercaya. Semua pengerjaan perbaikan Baterai dan LCD dilengkapi <span class="text-white font-bold underline underline-offset-4">Garansi Resmi 2 Bulan</span> dari iMake Gadget.
            </p>

            <!-- Search Bar & Filters -->
            <div class="mt-8 max-w-2xl mx-auto relative">
                <div class="relative flex items-center">
                    <i class="fa-solid fa-magnifying-glass absolute left-4 text-zinc-400 text-lg"></i>
                    <input type="text" id="searchInput" oninput="handleSearch()" 
                           placeholder="Cari Tipe Device (cth: iPhone 13 Pro, iPad Air 4, Macbook M1)..." 
                           class="w-full bg-zinc-900/90 text-white placeholder-zinc-500 pl-12 pr-10 py-4 rounded-2xl border border-zinc-700 focus:border-white focus:outline-none focus:ring-1 focus:ring-white transition-all text-sm sm:text-base shadow-xl">
                    <button id="clearSearch" onclick="clearSearchInput()" class="hidden absolute right-4 text-zinc-400 hover:text-white">
                        <i class="fa-solid fa-xmark text-lg"></i>
                    </button>
                </div>
            </div>
        </section>

        <!-- Category Selector -->
        <section class="flex flex-col sm:flex-row items-center justify-between gap-4">
            <div class="flex items-center gap-2 overflow-x-auto w-full sm:w-auto pb-2 sm:pb-0 scrollbar-none" id="categoryTabs">
                <button onclick="switchCategory('all')" id="btn-all" class="cat-btn px-5 py-2.5 rounded-xl font-semibold text-sm transition-all whitespace-nowrap bg-white text-black">
                    <i class="fa-solid fa-border-all mr-2"></i>Semua Tipe
                </button>
                <button onclick="switchCategory('iphone')" id="btn-iphone" class="cat-btn px-5 py-2.5 rounded-xl font-medium text-sm text-zinc-400 hover:text-white hover:bg-zinc-800 transition-all whitespace-nowrap border border-transparent">
                    <i class="fa-solid fa-mobile-screen mr-2"></i>iPhone
                </button>
                <button onclick="switchCategory('ipad')" id="btn-ipad" class="cat-btn px-5 py-2.5 rounded-xl font-medium text-sm text-zinc-400 hover:text-white hover:bg-zinc-800 transition-all whitespace-nowrap border border-transparent">
                    <i class="fa-solid fa-tablet-screen-button mr-2"></i>iPad
                </button>
                <button onclick="switchCategory('iwatch')" id="btn-iwatch" class="cat-btn px-5 py-2.5 rounded-xl font-medium text-sm text-zinc-400 hover:text-white hover:bg-zinc-800 transition-all whitespace-nowrap border border-transparent">
                    <i class="fa-solid fa-clock mr-2"></i>Apple Watch
                </button>
                <button onclick="switchCategory('macbook')" id="btn-macbook" class="cat-btn px-5 py-2.5 rounded-xl font-medium text-sm text-zinc-400 hover:text-white hover:bg-zinc-800 transition-all whitespace-nowrap border border-transparent">
                    <i class="fa-solid fa-laptop mr-2"></i>MacBook
                </button>
            </div>

            <!-- View Switcher (Cards / Table) -->
            <div class="flex items-center bg-zinc-900 border border-zinc-800 p-1 rounded-xl self-end sm:self-auto">
                <button onclick="setViewMode('cards')" id="btn-view-cards" class="px-3 py-1.5 rounded-lg text-xs font-semibold bg-zinc-800 text-white transition-all">
                    <i class="fa-solid fa-grip mr-1"></i> Kartu
                </button>
                <button onclick="setViewMode('table')" id="btn-view-table" class="px-3 py-1.5 rounded-lg text-xs font-medium text-zinc-400 hover:text-white transition-all">
                    <i class="fa-solid fa-list mr-1"></i> Tabel
                </button>
            </div>
        </section>

        <!-- Results Info & Counter -->
        <div class="flex items-center justify-between text-xs text-zinc-400 px-1">
            <span id="resultCount">Menampilkan 0 Tipe Perangkat</span>
            <span class="flex items-center gap-1.5"><i class="fa-solid fa-shield text-white text-xs"></i> Garansi Resmi 2 Bulan</span>
        </div>

        <!-- Dynamic Container Cards/Grid -->
        <div id="cardsView" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Dynamic Content loaded via JS -->
        </div>

        <!-- Dynamic Table View (Hidden by default) -->
        <div id="tableView" class="hidden overflow-x-auto rounded-2xl border border-zinc-800 glass-panel">
            <table class="w-full text-left text-sm text-zinc-300">
                <thead class="bg-zinc-900/90 text-xs uppercase tracking-wider text-zinc-400 border-b border-zinc-800">
                    <tr>
                        <th class="px-6 py-4">Tipe Perangkat</th>
                        <th class="px-6 py-4">Kategori</th>
                        <th class="px-6 py-4">Ganti Baterai</th>
                        <th class="px-6 py-4">Ganti LCD / Layar</th>
                        <th class="px-6 py-4">Garansi</th>
                        <th class="px-6 py-4 text-right">Aksi</th>
                    </tr>
                </thead>
                <tbody id="tableBody" class="divide-y divide-zinc-800/60">
                    <!-- Dynamic Table Rows -->
                </tbody>
            </table>
        </div>

        <!-- Empty Search Result State -->
        <div id="noResults" class="hidden text-center py-16 glass-panel rounded-3xl border border-zinc-800">
            <div class="w-16 h-16 mx-auto mb-4 rounded-full bg-zinc-900 border border-zinc-700 flex items-center justify-center text-zinc-500 text-2xl">
                <i class="fa-solid fa-magnifying-glass"></i>
            </div>
            <h3 class="text-lg font-bold text-white mb-1">Tidak Ditemukan</h3>
            <p class="text-zinc-400 text-sm max-w-sm mx-auto mb-6">Tipe perangkat yang Anda cari tidak ada dalam daftar cepat. Silakan hubungi admin kami untuk estimasi custom.</p>
            <a href="https://wa.me/6281234567890?text=Halo%20iMake%20Gadget,%20mau%20tanya%20harga%20service" target="_blank" class="inline-flex items-center gap-2 bg-white text-black font-semibold px-5 py-2.5 rounded-xl text-sm">
                <i class="fa-brands fa-whatsapp"></i> Tanya Langsung via WA
            </a>
        </div>

        <!-- Warranty Highlight Banner Section -->
        <section class="grid grid-cols-1 md:grid-cols-3 gap-6 pt-6">
            <div class="glass-card p-6 rounded-2xl border border-zinc-800 flex items-start space-x-4">
                <div class="p-3 bg-white text-black rounded-xl text-xl font-bold">
                    <i class="fa-solid fa-shield-halved"></i>
                </div>
                <div>
                    <h4 class="font-bold text-white text-base mb-1">Garansi 2 Bulan Full</h4>
                    <p class="text-xs text-zinc-400 leading-relaxed">Semua perbaikan Baterai & LCD mendapatkan garansi pengerjaan & fungsi penuh selama 60 hari.</p>
                </div>
            </div>
            <div class="glass-card p-6 rounded-2xl border border-zinc-800 flex items-start space-x-4">
                <div class="p-3 bg-white text-black rounded-xl text-xl font-bold">
                    <i class="fa-solid fa-screwdriver-wrench"></i>
                </div>
                <div>
                    <h4 class="font-bold text-white text-base mb-1">Teknisi Pengalaman</h4>
                    <p class="text-xs text-zinc-400 leading-relaxed">Dikerjakan dengan presisi tingi menggunakan peralatan standar Apple Service Center.</p>
                </div>
            </div>
            <div class="glass-card p-6 rounded-2xl border border-zinc-800 flex items-start space-x-4">
                <div class="p-3 bg-white text-black rounded-xl text-xl font-bold">
                    <i class="fa-solid fa-bolt"></i>
                </div>
                <div>
                    <h4 class="font-bold text-white text-base mb-1">Pengerjaan Cepat</h4>
                    <p class="text-xs text-zinc-400 leading-relaxed">Pemasangan baterai & LCD dapat ditunggu untuk tipe-tipe tertentu (30-60 menit).</p>
                </div>
            </div>
        </section>

    </main>

    <!-- Booking / Detail Modal -->
    <div id="serviceModal" class="fixed inset-0 z-50 flex items-center justify-center p-4 bg-black/80 backdrop-blur-md hidden">
        <div class="glass-panel w-full max-w-md rounded-3xl border border-zinc-700 p-6 sm:p-8 relative shadow-2xl">
            <button onclick="closeModal()" class="absolute top-5 right-5 text-zinc-400 hover:text-white p-2">
                <i class="fa-solid fa-xmark text-xl"></i>
            </button>
            <div class="mb-6">
                <div class="inline-block px-3 py-1 rounded-full bg-white/10 text-xs font-semibold text-white mb-2" id="modalDeviceType">
                    iPhone
                </div>
                <h3 class="text-xl font-extrabold text-white" id="modalDeviceTitle">iPhone 13 Pro</h3>
                <p class="text-xs text-zinc-400">Ringkasan Estimasi & Pemesanan Service</p>
            </div>

            <div class="space-y-4 mb-6">
                <div class="p-4 bg-zinc-900/80 rounded-2xl border border-zinc-800 space-y-3">
                    <div class="flex justify-between text-sm">
                        <span class="text-zinc-400">Pilihan Perbaikan:</span>
                        <span class="font-semibold text-white" id="modalServiceType">Baterai</span>
                    </div>
                    <div class="flex justify-between text-sm">
                        <span class="text-zinc-400">Estimasi Harga:</span>
                        <span class="font-bold text-white text-lg" id="modalPrice">Rp 350.000</span>
                    </div>
                    <div class="flex justify-between text-xs pt-2 border-t border-zinc-800">
                        <span class="text-zinc-400">Jaminan Garansi:</span>
                        <span class="font-bold text-emerald-400 flex items-center gap-1">
                            <i class="fa-solid fa-circle-check"></i> 2 Bulan (60 Hari)
                        </span>
                    </div>
                </div>

                <div class="text-xs text-zinc-400 leading-relaxed bg-zinc-950 p-3 rounded-xl border border-zinc-800">
                    <i class="fa-solid fa-circle-info text-white mr-1"></i> Harga tercantum sudah termasuk ongkos pasang teknisi & pengecekan fungsi menyeluruh.
                </div>
            </div>

            <a id="modalWaBtn" href="#" target="_blank" class="w-full flex items-center justify-center space-x-2 bg-white text-black hover:bg-zinc-200 font-bold py-3.5 rounded-2xl transition-all shadow-lg">
                <i class="fa-brands fa-whatsapp text-lg"></i>
                <span>Lanjutkan ke WhatsApp</span>
            </a>
        </div>
    </div>

    <!-- Footer -->
    <footer class="border-t border-zinc-800 bg-zinc-950/80 mt-12 py-10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col md:flex-row justify-between items-center gap-6">
                <div class="flex items-center space-x-3">
                    <div class="w-8 h-8 rounded-lg bg-white text-black flex items-center justify-center font-bold text-lg">
                        <i class="fa-brands fa-apple"></i>
                    </div>
                    <div>
                        <span class="font-bold text-white tracking-tight">iMake Gadget</span>
                        <p class="text-xs text-zinc-500">Service iPhone, iPad, iWatch & MacBook Profesional</p>
                    </div>
                </div>

                <div class="flex items-center space-x-6 text-xs text-zinc-400">
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-shield-halved text-white"></i> Garansi 2 Bulan</span>
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-check text-white"></i> Sparepart Presisi</span>
                    <span class="flex items-center gap-1.5"><i class="fa-solid fa-clock text-white"></i> Pengerjaan Cepat</span>
                </div>

                <div class="text-xs text-zinc-500">
                    &copy; 2026 iMake Gadget. All rights reserved.
                </div>
            </div>
        </div>
    </footer>

    <script>
        // Data Store
        const pricelistData = [
            // iPhone Series
            { category: 'iphone', model: 'iPhone 6G / 6S', battery: '125.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '185.000', lcdOri: '250.000' },
            { category: 'iphone', model: 'iPhone 6 Plus / 6S Plus', battery: '145.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '220.000', lcdOri: '290.000' },
            { category: 'iphone', model: 'iPhone 7G / 8G / SE2', battery: '155.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '235.000', lcdOri: '320.000' },
            { category: 'iphone', model: 'iPhone 7 Plus / 8 Plus', battery: '175.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '265.000', lcdOri: '360.000' },
            { category: 'iphone', model: 'iPhone X / XR', battery: '220.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '380.000', lcdOri: '550.000' },
            { category: 'iphone', model: 'iPhone XS / XS Max', battery: '250.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '420.000', lcdOri: '680.000' },
            { category: 'iphone', model: 'iPhone 11', battery: '265.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '450.000', lcdOri: '720.000' },
            { category: 'iphone', model: 'iPhone 11 Pro / 11 Pro Max', battery: '320.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '580.000', lcdOri: '950.000' },
            { category: 'iphone', model: 'iPhone 12 / 12 Mini', battery: '320.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '650.000', lcdOri: '1.150.000' },
            { category: 'iphone', model: 'iPhone 12 Pro / 12 Pro Max', battery: '360.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '780.000', lcdOri: '1.450.000' },
            { category: 'iphone', model: 'iPhone 13 / 13 Mini', battery: '380.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '850.000', lcdOri: '1.650.000' },
            { category: 'iphone', model: 'iPhone 13 Pro / 13 Pro Max', battery: '450.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.250.000', lcdOri: '2.450.000' },
            { category: 'iphone', model: 'iPhone 14 / 14 Plus', battery: '480.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.100.000', lcdOri: '2.100.000' },
            { category: 'iphone', model: 'iPhone 14 Pro / 14 Pro Max', battery: '550.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.850.000', lcdOri: '3.200.000' },
            { category: 'iphone', model: 'iPhone 15 / 15 Plus', battery: '580.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.650.000', lcdOri: '2.900.000' },
            { category: 'iphone', model: 'iPhone 15 Pro / 15 Pro Max', battery: '680.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '2.200.000', lcdOri: '3.800.000' },

            // iPad Series
            { category: 'ipad', model: 'iPad 5 / 6 (9.7")', battery: '280.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '480.000', lcdOri: '650.000' },
            { category: 'ipad', model: 'iPad 7 / 8 / 9 (10.2")', battery: '320.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '550.000', lcdOri: '820.000' },
            { category: 'ipad', model: 'iPad Mini 4 / 5', battery: '300.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '650.000', lcdOri: '950.000' },
            { category: 'ipad', model: 'iPad Mini 6', battery: '420.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.100.000', lcdOri: '1.600.000' },
            { category: 'ipad', model: 'iPad Air 3 / Air 4', battery: '380.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '950.000', lcdOri: '1.450.000' },
            { category: 'ipad', model: 'iPad Air 5 M1', battery: '450.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.250.000', lcdOri: '1.850.000' },
            { category: 'ipad', model: 'iPad Pro 11" (Gen 1 / 2)', battery: '450.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.350.000', lcdOri: '2.100.000' },
            { category: 'ipad', model: 'iPad Pro 11" M1 / M2', battery: '550.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.850.000', lcdOri: '2.800.000' },
            { category: 'ipad', model: 'iPad Pro 12.9" (Gen 3 / 4 / 5)', battery: '650.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '2.200.000', lcdOri: '3.600.000' },

            // Apple Watch Series
            { category: 'iwatch', model: 'Apple Watch Series 3 (38/42mm)', battery: '250.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '550.000', lcdOri: '750.000' },
            { category: 'iwatch', model: 'Apple Watch Series 4 (40/44mm)', battery: '280.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '680.000', lcdOri: '920.000' },
            { category: 'iwatch', model: 'Apple Watch Series 5 / SE (40/44mm)', battery: '320.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '750.000', lcdOri: '1.100.000' },
            { category: 'iwatch', model: 'Apple Watch Series 6 (40/44mm)', battery: '350.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '850.000', lcdOri: '1.250.000' },
            { category: 'iwatch', model: 'Apple Watch Series 7 / 8 (41/45mm)', battery: '420.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.150.000', lcdOri: '1.650.000' },
            { category: 'iwatch', model: 'Apple Watch Ultra (49mm)', battery: '580.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.850.000', lcdOri: '2.700.000' },

            // MacBook Series
            { category: 'macbook', model: 'MacBook Air 13" (A1466 / Older)', battery: '450.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.250.000', lcdOri: '1.750.000' },
            { category: 'macbook', model: 'MacBook Air Retina 13" (A1932 / A2179)', battery: '550.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.850.000', lcdOri: '2.450.000' },
            { category: 'macbook', model: 'MacBook Air M1 (A2337)', battery: '650.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.950.000', lcdOri: '2.650.000' },
            { category: 'macbook', model: 'MacBook Air M2 (A2681)', battery: '780.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '2.450.000', lcdOri: '3.400.000' },
            { category: 'macbook', model: 'MacBook Pro 13" Retina (A1502 / A1425)', battery: '580.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '1.650.000', lcdOri: '2.200.000' },
            { category: 'macbook', model: 'MacBook Pro 13" Touchbar (A1706 / A1708 / A1989)', battery: '650.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '2.100.000', lcdOri: '2.850.000' },
            { category: 'macbook', model: 'MacBook Pro M1 / M2 13" (A2338)', battery: '750.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '2.350.000', lcdOri: '3.100.000' },
            { category: 'macbook', model: 'MacBook Pro 14" M1 / M2 / M3', battery: '950.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '3.200.000', lcdOri: '4.500.000' },
            { category: 'macbook', model: 'MacBook Pro 16" M1 / M2 Pro/Max', battery: '1.150.000', batteryNote: 'Garansi 2 Bulan', lcdOem: '3.800.000', lcdOri: '5.200.000' }
        ];

        let currentCategory = 'all';
        let currentSearch = '';
        let currentView = 'cards';

        function initApp() {
            renderData();
        }

        function switchCategory(cat) {
            currentCategory = cat;
            
            document.querySelectorAll('.cat-btn').forEach(btn => {
                btn.classList.remove('bg-white', 'text-black');
                btn.classList.add('text-zinc-400', 'hover:text-white', 'border-transparent');
            });

            const activeBtn = document.getElementById(`btn-${cat}`);
            if (activeBtn) {
                activeBtn.classList.remove('text-zinc-400', 'hover:text-white', 'border-transparent');
                activeBtn.classList.add('bg-white', 'text-black');
            }

            renderData();
        }

        function handleSearch() {
            const val = document.getElementById('searchInput').value;
            currentSearch = val.toLowerCase().trim();
            document.getElementById('clearSearch').classList.toggle('hidden', currentSearch === '');
            renderData();
        }

        function clearSearchInput() {
            document.getElementById('searchInput').value = '';
            currentSearch = '';
            document.getElementById('clearSearch').classList.add('hidden');
            renderData();
        }

        function setViewMode(mode) {
            currentView = mode;
            const cardBtn = document.getElementById('btn-view-cards');
            const tableBtn = document.getElementById('btn-view-table');

            if (mode === 'cards') {
                cardBtn.className = "px-3 py-1.5 rounded-lg text-xs font-semibold bg-zinc-800 text-white transition-all";
                tableBtn.className = "px-3 py-1.5 rounded-lg text-xs font-medium text-zinc-400 hover:text-white transition-all";
                document.getElementById('cardsView').classList.remove('hidden');
                document.getElementById('tableView').classList.add('hidden');
            } else {
                tableBtn.className = "px-3 py-1.5 rounded-lg text-xs font-semibold bg-zinc-800 text-white transition-all";
                cardBtn.className = "px-3 py-1.5 rounded-lg text-xs font-medium text-zinc-400 hover:text-white transition-all";
                document.getElementById('tableView').classList.remove('hidden');
                document.getElementById('cardsView').classList.add('hidden');
            }
        }

        function getCategoryBadge(cat) {
            switch(cat) {
                case 'iphone': return '<span class="text-[10px] uppercase tracking-wider font-bold px-2 py-0.5 rounded bg-zinc-800 text-zinc-300 border border-zinc-700">iPhone</span>';
                case 'ipad': return '<span class="text-[10px] uppercase tracking-wider font-bold px-2 py-0.5 rounded bg-zinc-800 text-zinc-300 border border-zinc-700">iPad</span>';
                case 'iwatch': return '<span class="text-[10px] uppercase tracking-wider font-bold px-2 py-0.5 rounded bg-zinc-800 text-zinc-300 border border-zinc-700">Apple Watch</span>';
                case 'macbook': return '<span class="text-[10px] uppercase tracking-wider font-bold px-2 py-0.5 rounded bg-zinc-800 text-zinc-300 border border-zinc-700">MacBook</span>';
                default: return '';
            }
        }

        function renderData() {
            const filtered = pricelistData.filter(item => {
                const matchesCategory = currentCategory === 'all' || item.category === currentCategory;
                const matchesSearch = item.model.toLowerCase().includes(currentSearch);
                return matchesCategory && matchesSearch;
            });

            document.getElementById('resultCount').textContent = `Menampilkan ${filtered.length} Tipe Perangkat`;

            const cardsView = document.getElementById('cardsView');
            const tableBody = document.getElementById('tableBody');
            const noResults = document.getElementById('noResults');

            if (filtered.length === 0) {
                cardsView.innerHTML = '';
                tableBody.innerHTML = '';
                noResults.classList.remove('hidden');
                return;
            } else {
                noResults.classList.add('hidden');
            }

            // Render Cards
            cardsView.innerHTML = filtered.map(item => `
                <div class="glass-card rounded-2xl p-6 flex flex-col justify-between relative overflow-hidden group">
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            ${getCategoryBadge(item.category)}
                            <span class="inline-flex items-center gap-1 text-[11px] font-bold px-2.5 py-0.5 rounded-full badge-warranty">
                                <i class="fa-solid fa-shield text-[10px]"></i> Garansi 2 Bulan
                            </span>
                        </div>
                        <h3 class="text-xl font-extrabold text-white group-hover:text-zinc-200 transition-colors mb-4">${item.model}</h3>

                        <div class="space-y-3 mb-6">
                            <div class="p-3 rounded-xl bg-zinc-900/80 border border-zinc-800/80 flex items-center justify-between">
                                <div class="flex items-center space-x-2.5">
                                    <div class="w-8 h-8 rounded-lg bg-zinc-800 text-white flex items-center justify-center text-xs">
                                        <i class="fa-solid fa-battery-full"></i>
                                    </div>
                                    <div>
                                        <div class="text-xs font-semibold text-zinc-300">Ganti Baterai</div>
                                        <div class="text-[10px] text-zinc-500">Pengerjaan ~30 mnt</div>
                                    </div>
                                </div>
                                <div class="text-right">
                                    <div class="text-sm font-bold text-white">Rp ${item.battery}</div>
                                    <button onclick="openModal('${item.category}', '${item.model}', 'Baterai', 'Rp ${item.battery}')" class="text-[11px] text-zinc-400 hover:text-white underline">Pesan</button>
                                </div>
                            </div>

                            <div class="p-3 rounded-xl bg-zinc-900/80 border border-zinc-800/80 flex items-center justify-between">
                                <div class="flex items-center space-x-2.5">
                                    <div class="w-8 h-8 rounded-lg bg-zinc-800 text-white flex items-center justify-center text-xs">
                                        <i class="fa-solid fa-mobile"></i>
                                    </div>
                                    <div>
                                        <div class="text-xs font-semibold text-zinc-300">LCD High Quality</div>
                                        <div class="text-[10px] text-zinc-500">Presisi & Jernih</div>
                                    </div>
                                </div>
                                <div class="text-right">
                                    <div class="text-sm font-bold text-white">Rp ${item.lcdOem}</div>
                                    <button onclick="openModal('${item.category}', '${item.model}', 'LCD High Quality', 'Rp ${item.lcdOem}')" class="text-[11px] text-zinc-400 hover:text-white underline">Pesan</button>
                                </div>
                            </div>

                            <div class="p-3 rounded-xl bg-zinc-900/80 border border-zinc-800/80 flex items-center justify-between">
                                <div class="flex items-center space-x-2.5">
                                    <div class="w-8 h-8 rounded-lg bg-white text-black flex items-center justify-center text-xs font-bold">
                                        <i class="fa-brands fa-apple"></i>
                                    </div>
                                    <div>
                                        <div class="text-xs font-semibold text-white">LCD Original Apple</div>
                                        <div class="text-[10px] text-zinc-400">Kualitas Pabrikan</div>
                                    </div>
                                </div>
                                <div class="text-right">
                                    <div class="text-sm font-bold text-white">Rp ${item.lcdOri}</div>
                                    <button onclick="openModal('${item.category}', '${item.model}', 'LCD Original Apple', 'Rp ${item.lcdOri}')" class="text-[11px] text-zinc-400 hover:text-white underline">Pesan</button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <button onclick="openModal('${item.category}', '${item.model}', 'Konsultasi Perbaikan', 'Sesuai Pilihan')" 
                            class="w-full py-2.5 bg-zinc-900 hover:bg-white hover:text-black border border-zinc-700 text-white text-xs font-bold rounded-xl transition-all duration-200 flex items-center justify-center space-x-2">
                        <i class="fa-solid fa-screwdriver-wrench"></i>
                        <span>Pilih & Booking Service</span>
                    </button>
                </div>
            `).join('');

            // Render Table Rows
            tableBody.innerHTML = filtered.map(item => `
                <tr class="hover:bg-zinc-900/50 transition-colors">
                    <td class="px-6 py-4 font-bold text-white">${item.model}</td>
                    <td class="px-6 py-4">${getCategoryBadge(item.category)}</td>
                    <td class="px-6 py-4 font-medium text-zinc-200">Rp ${item.battery}</td>
                    <td class="px-6 py-4">
                        <div class="text-xs font-medium text-zinc-300">HQ: <span class="font-bold text-white">Rp ${item.lcdOem}</span></div>
                        <div class="text-xs font-medium text-zinc-300">Ori: <span class="font-bold text-white">Rp ${item.lcdOri}</span></div>
                    </td>
                    <td class="px-6 py-4">
                        <span class="inline-flex items-center gap-1 text-[11px] font-bold px-2 py-0.5 rounded bg-white text-black">
                            <i class="fa-solid fa-shield text-[9px]"></i> 2 Bulan
                        </span>
                    </td>
                    <td class="px-6 py-4 text-right">
                        <button onclick="openModal('${item.category}', '${item.model}', 'Pemeriksaan Umum', 'Mulai dari Rp ' + '${item.battery}')" 
                                class="px-3 py-1.5 bg-white text-black hover:bg-zinc-200 font-semibold rounded-lg text-xs transition-all">
                            Pesan
                        </button>
                    </td>
                </tr>
            `).join('');
        }

        // Modal Functionality
        function openModal(cat, model, service, price) {
            document.getElementById('modalDeviceType').textContent = cat.toUpperCase();
            document.getElementById('modalDeviceTitle').textContent = model;
            document.getElementById('modalServiceType').textContent = service;
            document.getElementById('modalPrice').textContent = price;

            const message = encodeURIComponent(`Halo iMake Gadget, saya ingin booking/tanya service:\nDevice: ${model}\nLayanan: ${service}\nEstimasi: ${price}\nGaransi: 2 Bulan`);
            document.getElementById('modalWaBtn').href = `https://wa.me/6281234567890?text=${message}`;

            document.getElementById('serviceModal').classList.remove('hidden');
        }

        function closeModal() {
            document.getElementById('serviceModal').classList.add('hidden');
        }

        document.getElementById('serviceModal').addEventListener('click', function(e) {
            if (e.target === this) closeModal();
        });

        window.onload = function() {
            initApp();
        };
    </script>
</body>
</html>