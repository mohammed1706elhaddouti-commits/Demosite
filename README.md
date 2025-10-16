<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mij's Magical Emporium</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/feather-icons"></script>
    <script src="https://cdn.jsdelivr.net/npm/feather-icons/dist/feather.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r134/three.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/vanta@latest/dist/vanta.net.min.js"></script>
    <style>
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        .fade-in {
            animation: fadeIn 1.5s ease-in-out;
        }
        .vanta-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
        }
    </style>
</head>
<body class="bg-gradient-to-br from-purple-900 to-indigo-800 text-white">
    <!-- Vanta.js Animation Container -->
    <div id="vanta-animation" class="vanta-container"></div>

    <!-- Loading Screen -->
    <div id="loading-screen" class="fixed inset-0 bg-black bg-opacity-90 flex flex-col items-center justify-center z-50 transition-opacity duration-1000">
        <div class="text-center">
            <h1 class="text-5xl md:text-7xl font-bold mb-6 tracking-wider">MIJ'S</h1>
            <div class="w-64 h-1 bg-gradient-to-r from-purple-400 to-pink-500 rounded-full mx-auto mb-8"></div>
            <h2 class="text-3xl md:text-5xl font-light tracking-widest">MAGICAL EMPORIUM</h2>
            <p class="mt-12 text-purple-300 animate-pulse">Entering our wonderland...</p>
        </div>
    </div>

    <!-- Main Content -->
    <div id="main-content" class="opacity-0 min-h-screen flex flex-col">
        <!-- Header -->
        <header class="py-6 px-4 md:px-8 lg:px-16 backdrop-blur-sm bg-black bg-opacity-30 shadow-lg">
            <div class="container mx-auto flex justify-between items-center">
                <a href="#" class="text-3xl font-bold flex items-center">
                    <i data-feather="shopping-bag" class="mr-2 text-pink-400"></i>
                    <span class="bg-clip-text text-transparent bg-gradient-to-r from-pink-400 to-purple-500">MIJ</span>
                </a>
                <nav class="hidden md:block">
                    <ul class="flex space-x-8">
                        <li><a href="#" class="hover:text-pink-300 transition">Home</a></li>
                        <li><a href="#" class="hover:text-pink-300 transition">Shop</a></li>
                        <li><a href="#" class="hover:text-pink-300 transition">About</a></li>
                        <li><a href="#" class="hover:text-pink-300 transition">Contact</a></li>
                    </ul>
                </nav>
                <div class="flex items-center space-x-4">
                    <button class="p-2 hover:bg-purple-700 rounded-full transition">
                        <i data-feather="search"></i>
                    </button>
                    <button class="p-2 hover:bg-purple-700 rounded-full transition">
                        <i data-feather="shopping-cart"></i>
                    </button>
                    <button class="md:hidden p-2 hover:bg-purple-700 rounded-full transition">
                        <i data-feather="menu"></i>
                    </button>
                </div>
            </div>
        </header>

        <!-- Hero Section -->
        <section class="flex-grow flex items-center py-16 px-4 md:px-8 lg:px-16">
            <div class="container mx-auto">
                <div class="max-w-2xl backdrop-blur-sm bg-black bg-opacity-30 p-8 rounded-xl shadow-2xl">
                    <h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
                        Discover <span class="bg-clip-text text-transparent bg-gradient-to-r from-pink-400 to-purple-500">Magical Finds</span> at Mij's
                    </h1>
                    <p class="text-lg md:text-xl mb-8 text-purple-100">
                        Where every item tells a story and every purchase feels like magic. Explore our curated collection of unique treasures.
                    </p>
                    <div class="flex flex-wrap gap-4">
                        <button class="px-8 py-3 bg-gradient-to-r from-pink-500 to-purple-600 rounded-full font-bold hover:from-pink-600 hover:to-purple-700 transition transform hover:scale-105 shadow-lg">
                            Shop Now
                        </button>
                        <button class="px-8 py-3 border-2 border-purple-400 rounded-full font-bold hover:bg-purple-900 transition transform hover:scale-105">
                            Learn More
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="py-8 px-4 md:px-8 lg:px-16 backdrop-blur-sm bg-black bg-opacity-30">
            <div class="container mx-auto">
                <div class="flex flex-col md:flex-row justify-between items-center">
                    <div class="mb-6 md:mb-0">
                        <h3 class="text-2xl font-bold flex items-center">
                            <i data-feather="shopping-bag" class="mr-2 text-pink-400"></i>
                            <span class="bg-clip-text text-transparent bg-gradient-to-r from-pink-400 to-purple-500">MIJ</span>
                        </h3>
                        <p class="mt-2 text-purple-200">Magical finds for magical people</p>
                    </div>
                    <div class="flex space-x-6">
                        <a href="#" class="hover:text-pink-300 transition">
                            <i data-feather="instagram"></i>
                        </a>
                        <a href="#" class="hover:text-pink-300 transition">
                            <i data-feather="facebook"></i>
                        </a>
                        <a href="#" class="hover:text-pink-300 transition">
                            <i data-feather="twitter"></i>
                        </a>
                        <a href="#" class="hover:text-pink-300 transition">
                            <i data-feather="mail"></i>
                        </a>
                    </div>
                </div>
                <div class="mt-8 pt-6 border-t border-purple-800 text-center text-purple-300">
                    <p>© 2023 Mij's Magical Emporium. All rights reserved.</p>
                </div>
            </div>
        </footer>
    </div>

    <script>
        // Initialize Vanta.js net animation
        VANTA.NET({
            el: "#vanta-animation",
            mouseControls: true,
            touchControls: true,
            gyroControls: false,
            minHeight: 200.00,
            minWidth: 200.00,
            scale: 1.00,
            scaleMobile: 1.00,
            color: 0x7d4aff,
            backgroundColor: 0x0,
            points: 10.00,
            maxDistance: 22.00,
            spacing: 18.00
        });

        // Loading animation sequence
        document.addEventListener('DOMContentLoaded', () => {
            feather.replace();
            
            setTimeout(() => {
                const loadingScreen = document.getElementById('loading-screen');
                const mainContent = document.getElementById('main-content');
                
                // Fade out loading screen
                loadingScreen.style.opacity = '0';
                
                // Remove loading screen after fade out
                setTimeout(() => {
                    loadingScreen.style.display = 'none';
                    mainContent.classList.remove('opacity-0');
                    mainContent.classList.add('fade-in');
                }, 1000);
            }, 2500);
        });
    </script>
</body>
</html>
