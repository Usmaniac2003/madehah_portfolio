<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&family=Roboto+Slab:wght@700&display=swap" rel="stylesheet">
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Apply custom fonts */
        body {
            font-family: 'Poppins', sans-serif;
        }

        h1, .font-heading {
            font-family: 'Roboto Slab', serif;
        }

        /* Background image and overlay styles */
        .background-container {
            position: relative;
            height: 100vh;
            background-image: url('./assets/images/bg.jpg');
            background-size: cover;
            background-position: center;
            overflow: hidden;
        }

        .overlay {
            position: absolute;
            inset: 0;
            background: rgba(0, 0, 0, 0.5);
        }

        .space-gradient {
            position: absolute;
            inset: 0;
            background: linear-gradient(135deg, rgba(0, 0, 25, 0.8), rgba(0, 0, 60, 0.6), rgba(25, 0, 60, 0.8));
            opacity: 0.8;
            z-index: 0;
        }

        .stars {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('./assets/images/stars.png');
            opacity: 0.5;
            z-index: 1;
        }

        .scroll-indicator {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 10;
            display: flex;
            flex-direction: column;
            align-items: center;
            cursor: pointer;
        }

        .scroll-indicator p {
            color: white;
            font-size: 14px;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .scroll-indicator .arrow {
            border: solid white;
            border-width: 0 3px 3px 0;
            display: inline-block;
            padding: 8px;
            transform: rotate(45deg);
            animation: bounce 2s infinite;
        }

            #next-section
        {
            position: relative;
            background-image: url('./assets/images/bg.jpg');
            background-size: cover;
            background-position: center;
            overflow: hidden;
        }


        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% {
                transform: translateY(0);
            }
            40% {
                transform: translateY(-10px);
            }
            60% {
                transform: translateY(-5px);
            }
        }

        .quote {
            margin-top: 40px;
            font-size: 1.25rem;
            font-style: italic;
            color: #d4d4d8;
            text-align: center;
            line-height: 1.6;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
        }

        .footer {
            background: #111;
            padding: 20px;
            text-align: center;
            color: white;
        }

        .footer p {
            margin: 0;
            font-size: 0.875rem;
        }

        /* Navbar styles for mobile */
        .nav-menu {
            display: none;
        }

        .nav-menu.active {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .hamburger {
            display: none;
        }

        @media (max-width: 768px) {
            .hamburger {
                display: block;
                cursor: pointer;
                font-size: 1.5rem;
                color: white;
            }

            .nav-menu {
                display: none;
                flex-direction: column;
                gap: 1rem;
            }

            .nav-menu.active {
                display: flex;
            }
        }
    </style>
    <title>Home</title>
</head>

<body class="bg-emerald-50">

    <!-- Background Container with Overlay -->
    <div class="background-container" id="home-section">
        <div class="overlay"></div>
        <div class="space-gradient"></div>
        <div class="stars"></div>

        <!-- Content Wrapper -->
        <div class="relative z-10">
            <!-- Header -->
            <header class="flex items-center justify-between mx-12 py-6 gap-4">
                <div class="name flex items-center gap-3 animate-bounce">
                    <div class="circle w-6 h-6 rounded-full bg-purple-500"></div>
                    <div class="name text-2xl font-heading w-[30ch] text-white">Usman Ghani</div>
                </div>

                <!-- Hamburger Menu -->
                <div class="hamburger" onclick="toggleMenu()">
                    &#9776;
                </div>

                <!-- Navbar -->
                <nav class="flex flex-row justify-evenly w-full text-gray-700 text-lg nav-menu">
                    <a href="./pages/career-goals.html" class="hover:text-purple-600 text-white hover:underline transition duration-300">Career</a>
                    <a href="./pages/contact.html" class="hover:text-purple-600 text-white hover:underline transition duration-300">Contact</a>
                    <a href="./pages/gallery.html" class="hover:text-purple-600 text-white hover:underline transition duration-300">Gallery</a>
                    <a href="./pages/profile.html" class="hover:text-purple-600 text-white hover:underline transition duration-300">Profile</a>
                    <a href="./pages/projects.html" class="hover:text-purple-600 text-white hover:underline transition duration-300">Projects</a>
                    <a href="./pages/skill-interests.html" class="hover:text-purple-600 text-white hover:underline transition duration-300">Skills</a>
                </nav>
            </header>

            <!-- Main Content -->
            <main class="mx-10 flex flex-col md:flex-row gap-10 items-center py-10">
                <div class="bio h-auto w-full md:w-[60vw] p-6 rounded-lg shadow-md relative animate-fadeIn backdrop-blur-lg">
                    <div class="absolute inset-0 bg-gradient-to-r from-blue-500 to-purple-400 opacity-90 rounded-lg"></div>

                    <div class="relative z-10">
                        <div class="intro text-2xl font-heading font-bold mb-4 text-white">Hello, I am Usman Ghani, a Software Engineer with 2 years of experience</div>

                        <div class="bio text-sm mb-12 text-white">
                            I’m the guy who’s passionate about coding, always exploring new technologies, and tackling challenges head-on. Aiming to become a skilled full-stack developer, constantly learning and growing in the tech world.
                        </div>

                        <div class="quote text-white ">
                            "Striving for excellence with every line of code. Innovation, growth, and a passion for tech drive me."
                        </div>

                        <div class="links flex flex-row gap-4 mt-40">
                            <div class="contactMe">
                                <a href="#" class="text-lg font-semibold text-white bg-slate-900 px-4 py-2 rounded-lg hover:bg-white hover:text-black transition duration-300">Contact Me</a>
                            </div>

                            <div class="socials flex gap-4">
                                <a href="#" class="linkedIn transform hover:scale-110 hover:rotate-12 transition duration-300">
                                    <img src="./assets/icons/linkein.png" alt="LinkedIn" class="w-8 h-8">
                                </a>

                                <a href="#" class="insta transform hover:scale-110 hover:rotate-12 transition duration-300">
                                    <img src="./assets/icons/insta.png" alt="Instagram" class="w-8 h-8">
                                </a>

                                <a href="#" class="github transform hover:scale-110 hover:rotate-12 transition duration-300">
                                    <img src="./assets/icons/github.png" alt="GitHub" class="w-8 h-8">
                                </a>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="picture w-full md:w-[30vw] flex justify-center animate-zoomIn">
                    <img src="./assets/images/me.jpg" alt="Profile Picture" class="w-64 h-64 rounded-full shadow-lg object-cover">
                </div>
            </main>

        </div>

        <!-- Scroll Indicator -->
        <div class="scroll-indicator" onclick="scrollToNextSection()">
            <p>Scroll Down</p>
            <div class="arrow"></div>
        </div>
    </div>

    <section id="next-section" class="min-h-screen  text-white py-20 px-4">
        <div class="overlay"></div>
        
        <h2 class="text-4xl font-heading text-center mb-10">Explore More</h2>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <!-- Box 1 -->
            <a href="./pages/career-goals.html" class="nav-box relative group bg-gradient-to-r from-blue-500 to-purple-500 rounded-lg overflow-hidden">
                <img src="./assets/images/career.jpeg" alt="Career" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="nav-overlay absolute inset-0 flex items-center justify-center bg-black bg-opacity-50 group-hover:bg-opacity-70 transition duration-500">
                    <span class="text-2xl font-bold text-white">Career</span>
                </div>
            </a>
            <!-- Box 2 -->
            <a href="./pages/contact.html" class="nav-box relative group bg-gradient-to-r from-blue-500 to-purple-500 rounded-lg overflow-hidden">
                <img src="./assets/images/contact.jpeg" alt="Contact" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="nav-overlay absolute inset-0 flex items-center justify-center bg-black bg-opacity-50 group-hover:bg-opacity-70 transition duration-500">
                    <span class="text-2xl font-bold text-white">Contact</span>
                </div>
            </a>
            <!-- Box 3 -->
            <a href="./pages/gallery.html" class="nav-box relative group bg-gradient-to-r from-blue-500 to-purple-500 rounded-lg overflow-hidden">
                <img src="./assets/images/gallery.jpeg" alt="Gallery" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="nav-overlay absolute inset-0 flex items-center justify-center bg-black bg-opacity-50 group-hover:bg-opacity-70 transition duration-500">
                    <span class="text-2xl font-bold text-white">Gallery</span>
                </div>
            </a>
            <!-- Box 4 -->
            <a href="./pages/profile.html" class="nav-box relative group bg-gradient-to-r from-blue-500 to-purple-500 rounded-lg overflow-hidden">
                <img src="./assets/images/profile.jpg" alt="Profile" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="nav-overlay absolute inset-0 flex items-center justify-center bg-black bg-opacity-50 group-hover:bg-opacity-70 transition duration-500">
                    <span class="text-2xl font-bold text-white">Profile</span>
                </div>
            </a>
            <!-- Box 5 -->
            <a href="./pages/projects.html" class="nav-box relative group bg-gradient-to-r from-blue-500 to-purple-500 rounded-lg overflow-hidden">
                <img src="./assets/images/projects.jpeg" alt="Projects" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="nav-overlay absolute inset-0 flex items-center justify-center bg-black bg-opacity-50 group-hover:bg-opacity-70 transition duration-500">
                    <span class="text-2xl font-bold text-white">Projects</span>
                </div>
            </a>
            <!-- Box 6 -->
            <a href="./pages/skill-interests.html" class="nav-box relative group bg-gradient-to-r from-blue-500 to-purple-500 rounded-lg overflow-hidden">
                <img src="./assets/images/skills.png" alt="Skills" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">
                <div class="nav-overlay absolute inset-0 flex items-center justify-center bg-black bg-opacity-50 group-hover:bg-opacity-70 transition duration-500">
                    <span class="text-2xl font-bold text-white">Skills</span>
                </div>
            </a>
        </div>
        </section>
    

    <!-- Footer -->
    <footer class="footer">
        <p>&copy; 2024 Usman Ghani. All rights reserved.</p>
    </footer>

    <!-- JavaScript -->
    <script>
        // Toggle the navigation menu
        function toggleMenu() {
            const navMenu = document.querySelector('.nav-menu');
            navMenu.classList.toggle('active');
        }

        // Smooth scroll to next section
        function scrollToNextSection() {
            const nextSection = document.getElementById('next-section');
            window.scrollTo({
                top: nextSection.offsetTop,
                behavior: 'smooth'
            });
        }
    </script>
</body>

</html>
