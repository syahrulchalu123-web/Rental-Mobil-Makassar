<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rental Mobil Makassar - Sewa Mobil Terbaik</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f8fafc;
        }
        
        .hero-section {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1537005081207-04f90e3ba640?ixlib=rb-4.0.3&auto=format&fit=crop&w=1674&q=80');
            background-size: cover;
            background-position: center;
            padding: 120px 0;
        }
        
        .car-card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border-radius: 12px;
            overflow: hidden;
        }
        
        .car-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
        
        .btn-primary {
            background: linear-gradient(135deg, #2563eb 0%, #1d4ed8 100%);
            transition: all 0.3s ease;
        }
        
        .btn-primary:hover {
            background: linear-gradient(135deg, #1d4ed8 0%, #1e40af 100%);
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }
        
        .feature-icon {
            background-color: #dbeafe;
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
        }
        
        .testimonial-card {
            background: white;
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
        }
        
        .nav-link {
            position: relative;
        }
        
        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: #2563eb;
            transition: width 0.3s ease;
        }
        
        .nav-link:hover::after {
            width: 100%;
        }
        
        .logo-text {
            font-weight: 700;
            font-size: 24px;
            color: #2563eb;
        }
        
        .footer {
            background: linear-gradient(135deg, #1e293b 0%, #0f172a 100%);
            color: white;
        }

        .booking-modal {
            transition: all 0.3s ease;
        }
    </style>
</head>
<body class="antialiased">
    <!-- Header & Navigation -->
    <header class="bg-white shadow-md fixed w-full z-50">
        <div class="container mx-auto px-4 py-4">
            <div class="flex justify-between items-center">
                <div class="flex items-center space-x-2">
                    <i class="fas fa-car text-blue-600 text-3xl"></i>
                    <span class="logo-text">RentalMakassar</span>
                </div>
                
                <nav class="hidden md:flex space-x-10">
                    <a href="#beranda" class="nav-link text-gray-700 font-medium">Beranda</a>
                    <a href="#mobil" class="nav-link text-gray-700 font-medium">Mobil</a>
                    <a href="#layanan" class="nav-link text-gray-700 font-medium">Layanan</a>
                    <a href="#testimoni" class="nav-link text-gray-700 font-medium">Testimoni</a>
                    <a href="#kontak" class="nav-link text-gray-700 font-medium">Kontak</a>
                </nav>
                
                <div class="flex items-center space-x-4">
                    <button onclick="openBookingModal()" class="bg-blue-600 text-white py-2 px-6 rounded-full font-medium hover:bg-blue-700 transition">
                        <i class="fas fa-calendar-check mr-2"></i> Booking Sekarang
                    </button>
                    
                    <button class="md:hidden text-gray-700" id="mobile-menu-btn">
                        <i class="fas fa-bars text-2xl"></i>
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Mobile Menu -->
    <div id="mobile-menu" class="hidden fixed inset-0 bg-white z-40 flex flex-col items-center justify-center space-y-8">
        <button id="close-menu" class="absolute top-4 right-4 text-2xl text-gray-700">
            <i class="fas fa-times"></i>
        </button>
        <a href="#beranda" class="text-2xl font-medium">Beranda</a>
        <a href="#mobil" class="text-2xl font-medium">Mobil</a>
        <a href="#layanan" class="text-2xl font-medium">Layanan</a>
        <a href="#testimoni" class="text-2xl font-medium">Testimoni</a>
        <a href="#kontak" class="text-2xl font-medium">Kontak</a>
    </div>

    <!-- Hero Section -->
    <section id="beranda" class="hero-section text-white mt-20">
        <div class="container mx-auto px-4 text-center">
            <h1 class="text-4xl md:text-5xl font-bold mb-6">Sewa Mobil Terbaik di Makassar</h1>
            <p class="text-xl mb-10 max-w-3xl mx-auto">Nikmati perjalanan Anda dengan kenyamanan dan keamanan terjamin bersama layanan rental mobil terpercaya di Makassar</p>
            
            <div class="flex flex-col sm:flex-row justify-center space-y-4 sm:space-y-0 sm:space-x-4">
                <a href="#mobil" class="btn-primary py-3 px-8 rounded-full text-lg font-semibold inline-block">
                    Lihat Mobil <i class="fas fa-arrow-right ml-2"></i>
                </a>
                <button onclick="openBookingModal()" class="bg-white text-blue-600 py-3 px-8 rounded-full text-lg font-semibold">
                    <i class="fas fa-calendar-check mr-2"></i> Booking Sekarang
                </button>
            </div>
        </div>
    </section>

    <!-- Features Section -->
    <section id="layanan" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-16">Mengapa Memilih Kami?</h2>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-10">
                <div class="text-center">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-shield-alt text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">Terjamin dan Terpercaya</h3>
                    <p class="text-gray-600">Layanan rental mobil dengan jaminan keamanan dan kenyamanan selama perjalanan Anda</p>
                </div>
                
                <div class="text-center">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-tag text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">Harga Terjangkau</h3>
                    <p class="text-gray-600">Dapatkan penawaran terbaik dengan harga kompetitif dan berbagai pilihan paket</p>
                </div>
                
                <div class="text-center">
                    <div class="feature-icon mx-auto">
                        <i class="fas fa-headset text-blue-600 text-2xl"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-4">Layanan 24/7</h3>
                    <p class="text-gray-600">Kami siap melayani Anda kapan saja dengan customer service yang ramah</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Cars Section -->
    <section id="mobil" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-4">Pilihan Mobil Kami</h2>
            <p class="text-gray-600 text-center mb-12">Berbagai jenis mobil tersedia untuk kebutuhan perjalanan Anda</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Car 1 -->
                <div class="car-card bg-white rounded-lg overflow-hidden shadow-md">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1549317661-bd32c8ce0db2?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" 
                             alt="Toyota Avanza warna silver dengan latar belakang jalan raya" class="w-full h-56 object-cover">
                        <span class="bg-blue-600 text-white py-1 px-3 text-sm absolute top-4 left-4 rounded-full">POPULER</span>
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Toyota Avanza</h3>
                        <div class="flex items-center mb-4">
                            <div class="flex text-yellow-400 mr-2">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                            <span class="text-gray-600">4.5 (120 reviews)</span>
                        </div>
                        <div class="flex justify-between mb-4">
                            <div>
                                <p class="text-gray-600"><i class="fas fa-users text-blue-600 mr-2"></i> 7 Kursi</p>
                            </div>
                            <div>
                                <p class="text-gray-600"><i class="fas fa-gas-pump text-blue-600 mr-2"></i> Bensin</p>
                            </div>
                            <div>
                                <p class="text-gray-600"><i class="fas fa-cogs text-blue-600 mr-2"></i> Manual</p>
                            </div>
                        </div>
                        <div class="flex justify-between items-center mt-6">
                            <div>
                                <p class="text-2xl font-bold text-blue-600">Rp 350.000<span class="text-sm font-normal text-gray-600">/hari</span></p>
                            </div>
                            <button onclick="openBookingModal('Toyota Avanza')" class="bg-blue-600 text-white py-2 px-4 rounded-lg font-medium hover:bg-blue-700 transition">
                                Sewa Sekarang
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Car 2 -->
                <div class="car-card bg-white rounded-lg overflow-hidden shadow-md">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1541899481282-d53bffe3c35d?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" 
                             alt="Honda Civic warna hitam dengan desain sporty dan modern" class="w-full h-56 object-cover">
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Honda Civic</h3>
                        <div class="flex items-center mb-4">
                            <div class="flex text-yellow-400 mr-2">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                            </div>
                            <span class="text-gray-600">4.8 (95 reviews)</span>
                        </div>
                        <div class="flex justify-between mb-4">
                            <div>
                                <p class="text-gray-600"><i class="fas fa-users text-blue-600 mr-2"></i> 5 Kursi</p>
                            </div>
                            <div>
                                <p class="text-gray-600"><i class="fas fa-gas-pump text-blue-600 mr-2"></i> Bensin</p>
                            </div>
                            <div>
                                <p class="text-gray-600"><i class="fas fa-cogs text-blue-600 mr-2"></i> Matic</p>
                            </div>
                        </div>
                        <div class="flex justify-between items-center mt-6">
                            <div>
                                <p class="text-2xl font-bold text-blue-600">Rp 500.000<span class="text-sm font-normal text-gray-600">/hari</span></p>
                            </div>
                            <button onclick="openBookingModal('Honda Civic')" class="bg-blue-600 text-white py-2 px-4 rounded-lg font-medium hover:bg-blue-700 transition">
                                Sewa Sekarang
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- Car 3 -->
                <div class="car-card bg-white rounded-lg overflow-hidden shadow-md">
                    <div class="relative">
                        <img src="https://images.unsplash.com/photo-1544829099-b9a0c07fad1a?ixlib=rb-4.0.3&auto=format&fit=crop&w=900&q=80" 
                             alt="Toyota Hiace warna putih dengan bodong panjang untuk penumpang" class="w-full h-56 object-cover">
                    </div>
                    <div class="p-6">
                        <h3 class="text-xl font-bold mb-2">Toyota Hiace</h3>
                        <div class="flex items-center mb-4">
                            <div class="flex text-yellow-400 mr-2">
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star"></i>
                                <i class="fas fa-star-half-alt"></i>
                            </div>
                            <span class="text-gray-600">4.6 (87 reviews)</span>
                        </div>
                        <div class="flex justify-between mb-4">
                            <div>
                                <p class="text-gray-600"><i class="fas fa-users text-blue-600 mr-2"></i> 15 Kursi</p>
                            </div>
                            <div>
                                <p class="text-gray-600"><i class="fas fa-gas-pump text-blue-600 mr-2"></i> Diesel</p>
                            </div>
                            <div>
                                <p class="text-gray-600"><i class="fas fa-cogs text-blue-600 mr-2"></i> Manual</p>
                            </div>
                        </div>
                        <div class="flex justify-between items-center mt-6">
                            <div>
                                <p class="text-2xl font-bold text-blue-600">Rp 750.000<span class="text-sm font-normal text-gray-600">/hari</span></p>
                            </div>
                            <button onclick="openBookingModal('Toyota Hiace')" class="bg-blue-600 text-white py-2 px-4 rounded-lg font-medium hover:bg-blue-700 transition">
                                Sewa Sekarang
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Booking Modal -->
    <div id="booking-modal" class="fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50 hidden booking-modal">
        <div class="bg-white rounded-lg p-6 w-11/12 md:w-2/3 lg:w-1/2 max-h-screen overflow-y-auto">
            <div class="flex justify-between items-center mb-6">
                <h3 class="text-2xl font-bold">Form Pemesanan Mobil</h3>
                <button onclick="closeBookingModal()" class="text-gray-500 hover:text-gray-700">
                    <i class="fas fa-times text-xl"></i>
                </button>
            </div>
            
            <form id="booking-form" onsubmit="submitBooking(event)">
                <input type="hidden" id="selected-car" value="">
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                    <div>
                        <label for="name" class="block mb-1 font-medium">Nama Lengkap *</label>
                        <input type="text" id="name" required class="w-full border border-gray-300 rounded px-3 py-2">
                    </div>
                    <div>
                        <label for="phone" class="block mb-1 font-medium">No. WhatsApp *</label>
                        <input type="tel" id="phone" required class="w-full border border-gray-300 rounded px-3 py-2">
                    </div>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                    <div>
                        <label for="email" class="block mb-1 font-medium">Email</label>
                        <input type="email" id="email" class="w-full border border-gray-300 rounded px-3 py-2">
                    </div>
                    <div>
                        <label for="address" class="block mb-1 font-medium">Alamat</label>
                        <input type="text" id="address" class="w-full border border-gray-300 rounded px-3 py-2">
                    </div>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                    <div>
                        <label for="pickup-date" class="block mb-1 font-medium">Tanggal Ambil *</label>
                        <input type="date" id="pickup-date" required class="w-full border border-gray-300 rounded px-3 py-2">
                    </div>
                    <div>
                        <label for="return-date" class="block mb-1 font-medium">Tanggal Kembali *</label>
                        <input type="date" id="return-date" required class="w-full border border-gray-300 rounded px-3 py-2">
                    </div>
                </div>
                
                <div class="mb-4">
                    <label for="pickup-location" class="block mb-1 font-medium">Lokasi Pengambilan *</label>
                    <input type="text" id="pickup-location" required class="w-full border border-gray-300 rounded px-3 py-2" placeholder="Alamat lengkap pengambilan mobil">
                </div>
                
                <div class="mb-4">
                    <label for="notes" class="block mb-1 font-medium">Catatan Tambahan</label>
                    <textarea id="notes" rows="3" class="w-full border border-gray-300 rounded px-3 py-2"></textarea>
                </div>
                
                <button type="submit" class="w-full bg-blue-600 text-white py-3 rounded-lg font-semibold hover:bg-blue-700 transition">
                    Kirim Pemesanan ke WhatsApp
                </button>
            </form>
        </div>
    </div>

    <!-- Testimonials -->
    <section id="testimoni" class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-4">Apa Kata Pelanggan Kami?</h2>
            <p class="text-gray-600 text-center mb-12">Testimoni dari pelanggan yang telah menggunakan layanan kami</p>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="testimonial-card">
                    <div class="flex text-yellow-400 mb-4">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-600 mb-6">"Pelayanan sangat memuaskan, mobil bersih dan nyaman. Sopirnya juga ramah dan berpengalaman. Recommended banget!"</p>
                    <div class="flex items-center">
                        <div class="bg-gray-200 w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-user text-gray-600"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold">Ahmad Rizky</h4>
                            <p class="text-gray-500">Pengusaha</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card">
                    <div class="flex text-yellow-400 mb-4">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-600 mb-6">"Sewa mobil untuk liburan keluarga, harganya terjangkau dan prosesnya cepat. Mobilnya juga dalam kondisi sangat baik."</p>
                    <div class="flex items-center">
                        <div class="bg-gray-200 w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-user text-gray-600"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold">Dewi Lestari</h4>
                            <p class="text-gray-500">Ibu Rumah Tangga</p>
                        </div>
                    </div>
                </div>
                
                <div class="testimonial-card">
                    <div class="flex text-yellow-400 mb-4">
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                        <i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-600 mb-6">"Sering sewa mobil untuk keperluan dinas. Pelayanan profesiona dan mobil selalu dalam kondisi prima. Tidak pernah mengecewakan!"</p>
                    <div class="flex items-center">
                        <div class="bg-gray-200 w-12 h-12 rounded-full flex items-center justify-center mr-4">
                            <i class="fas fa-user text-gray-600"></i>
                        </div>
                        <div>
                            <h4 class="font-semibold">Budi Santoso</h4>
                            <p class="text-gray-500">Karyawan Swasta</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="kontak" class="py-16 bg-gray-50">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-4">Hubungi Kami</h2>
            <p class="text-gray-600 text-center mb-12">Silakan hubungi kami untuk informasi lebih lanjut</p>
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <h3 class="text-xl font-semibold mb-4">Informasi Kontak</h3>
                    <div class="space-y-4">
                        <div class="flex items-center">
                            <div class="bg-blue-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-map-marker-alt text-blue-600"></i>
                            </div>
                            <div>
                                <p class="font-medium">Alamat</p>
                                <p class="text-gray-600">Jl. Perintis Kemerdekaan No. 45, Makassar</p>
                            </div>
                        </div>
                        
                        <div class="flex items-center">
                            <div class="bg-blue-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-phone-alt text-blue-600"></i>
                            </div>
                            <div>
                                <p class="font-medium">Telepon</p>
                                <p class="text-gray-600">082192227779</p>
                            </div>
                        </div>
                        
                        <div class="flex items-center">
                            <div class="bg-blue-100 w-10 h-10 rounded-full flex items-center justify-center mr-4">
                                <i class="fas fa-envelope text-blue-600"></i>
                            </div>
                            <div>
                                <p class="font-medium">Email</p>
                                <p class="text-gray-600">info@rentalmakassar.com</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="bg-white p-6 rounded-lg shadow-md">
                    <h3 class="text-xl font-semibold mb-4">Jam Operasional</h3>
                    <div class="space-y-3">
                        <div class="flex justify-between">
                            <p class="font-medium">Senin - Jumat</p>
                            <p class="text-gray-600">08:00 - 20:00</p>
                        </div>
                        <div class="flex justify-between">
                            <p class="font-medium">Sabtu</p>
                            <p class="text-gray-600">08:00 - 18:00</p>
                        </div>
                        <div class="flex justify-between">
                            <p class="font-medium">Minggu</p>
                            <p class="text-gray-600">09:00 - 16:00</p>
                        </div>
                    </div>
                    
                    <div class="mt-6">
                        <h3 class="text-xl font-semibold mb-4">Ikuti Kami</h3>
                        <div class="flex space-x-4">
                            <a href="#" class="bg-blue-100 w-10 h-10 rounded-full flex items-center justify-center text-blue-600 hover:bg-blue-600 hover:text-white">
                                <i class="fab fa-facebook-f"></i>
                            </a>
                            <a href="#" class="bg-blue-100 w-10 h-10 rounded-full flex items-center justify-center text-blue-600 hover:bg-blue-600 hover:text-white">
                                <i class="fab fa-instagram"></i>
                            </a>
                            <a href="#" class="bg-blue-100 w-10 h-10 rounded-full flex items-center justify-center text-blue-600 hover:bg-blue-600 hover:text-white">
                                <i class="fab fa-twitter"></i>
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="footer py-12">
        <div class="container mx-auto px-4">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
                <div>
                    <h3 class="text-xl font-semibold mb-4">RentalMakassar</h3>
                    <p class="text-gray-300">Layanan rental mobil terpercaya di Makassar dengan armada terbaik dan harga kompetitif.</p>
                </div>
                
                <div>
                    <h3 class="text-xl font-semibold mb-4">Tautan Cepat</h3>
                    <ul class="space-y-2">
                        <li><a href="#beranda" class="text-gray-300 hover:text-white">Beranda</a></li>
                        <li><a href="#mobil" class="text-gray-300 hover:text-white">Mobil</a></li>
                        <li><a href="#layanan" class="text-gray-300 hover:text-white">Layanan</a></li>
                        <li><a href="#testimoni" class="text-gray-300 hover:text-white">Testimoni</a></li>
                        <li><a href="#kontak" class="text-gray-300 hover:text-white">Kontak</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-xl font-semibold mb-4">Layanan</h3>
                    <ul class="space-y-2">
                        <li><a href="#" class="text-gray-300 hover:text-white">Sewa Harian</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Sewa Mingguan</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Sewa Bulanan</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Dengan Sopir</a></li>
                        <li><a href="#" class="text-gray-300 hover:text-white">Lepas Kunci</a></li>
                    </ul>
                </div>
                
                <div>
                    <h3 class="text-xl font-semibold mb-4">Kontak</h3>
                    <ul class="space-y-2">
                        <li class="flex items-center">
                            <i class="fas fa-map-marker-alt text-gray-300 mr-2"></i>
                            <span class="text-gray-300">Jl. Perintis Kemerdekaan No. 45, Makassar</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-phone-alt text-gray-300 mr-2"></i>
                            <span class="text-gray-300">082192227779</span>
                        </li>
                        <li class="flex items-center">
                            <i class="fas fa-envelope text-gray-300 mr-2"></i>
                            <span class="text-gray-300">info@rentalmakassar.com</span>
                        </li>
                    </ul>
                </div>
            </div>
            
            <div class="border-t border-gray-700 mt-8 pt-8 text-center">
                <p class="text-gray-300">© 2023 RentalMakassar. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile menu functionality
        const mobileMenuBtn = document.getElementById('mobile-menu-btn');
        const closeMenuBtn = document.getElementById('close-menu');
        const mobileMenu = document.getElementById('mobile-menu');
        
        mobileMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.remove('hidden');
        });
        
        closeMenuBtn.addEventListener('click', () => {
            mobileMenu.classList.add('hidden');
        });
        
        // Booking modal functionality
        function openBookingModal(carType = '') {
            const modal = document.getElementById('booking-modal');
            const selectedCarInput = document.getElementById('selected-car');
            
            if (carType) {
                selectedCarInput.value = carType;
            }
            
            modal.classList.remove('hidden');
            document.body.style.overflow = 'hidden';
        }
        
        function closeBookingModal() {
            const modal = document.getElementById('booking-modal');
            modal.classList.add('hidden');
            document.body.style.overflow = 'auto';
        }
        
        // Form submission to WhatsApp
        function submitBooking(event) {
            event.preventDefault();
            
            // Get form values
            const name = document.getElementById('name').value;
            const phone = document.getElementById('phone').value;
            const email = document.getElementById('email').value;
            const address = document.getElementById('address').value;
            const pickupDate = document.getElementById('pickup-date').value;
            const returnDate = document.getElementById('return-date').value;
            const pickupLocation = document.getElementById('pickup-location').value;
            const notes = document.getElementById('notes').value;
            const carType = document.getElementById('selected-car').value || 'Tidak ditentukan';
            
            // Format dates
            const formattedPickupDate = new Date(pickupDate).toLocaleDateString('id-ID');
            const formattedReturnDate = new Date(returnDate).toLocaleDateString('id-ID');
            
            // Create WhatsApp message
            const message = `Halo, saya ingin memesan mobil dengan detail sebagai berikut:
            
Nama: ${name}
No. WhatsApp: ${phone}
Email: ${email}
Alamat: ${address}
Mobil yang dipesan: ${carType}
Tanggal Ambil: ${formattedPickupDate}
Tanggal Kembali: ${formattedReturnDate}
Lokasi Pengambilan: ${pickupLocation}
Catatan: ${notes || 'Tidak ada catatan'}

Terima kasih.`;
            
            // Encode message for URL
            const encodedMessage = encodeURIComponent(message);
            
            // Your WhatsApp number
            const whatsappNumber = '082192227779';
            
            // Create WhatsApp URL
            const whatsappURL = `https://wa.me/${whatsappNumber}?text=${encodedMessage}`;
            
            // Open WhatsApp
            window.open(whatsappURL, '_blank');
            
            // Close modal
            closeBookingModal();
            
            // Reset form
            document.getElementById('booking-form').reset();
        }
        
        // Close modal when clicking outside
        document.getElementById('booking-modal').addEventListener('click', (e) => {
            if (e.target.id === 'booking-modal') {
                closeBookingModal();
            }
        });
    </script>
</body>
</html>
