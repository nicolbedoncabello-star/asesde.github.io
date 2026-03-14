Generando página web con:




### FILE: changelog.md
``` md
Description: Create a modern, professional, and visually appealing website for the ASOCIACIÓN DE ESTUDIANTES DE DERECHO DEL PERÚ (ASESDE PERÚ).
Files:
- index.html: Main entry point for the website containing the complete HTML structure. Refs: Tailwind CSS, GSAP, Lucide Icons, Google Fonts.
- styles.css: Custom CSS for specific typography, smooth scrolling, and minor stylistic overrides.
- main.js: Logic for initializing icons, handling mobile menu, and creating scroll-based GSAP animations.
```

### FILE: index.html
``` html
<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ASESDE Perú - Asociación de Estudiantes de Derecho del Perú</title>
    <meta name="description" content="Organización que une a estudiantes de Derecho de todo el Perú y promueve el desarrollo académico, el liderazgo jurídico y el impacto social.">
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        navy: {
                            900: '#0B132B',
                            800: '#1C2541',
                        },
                        gold: {
                            500: '#D4AF37',
                            600: '#AA8C2C',
                        }
                    },
                    fontFamily: {
                        serif:['"Playfair Display"', 'serif'],
                        sans: ['"Inter"', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="styles.css">
    <script src="https://unpkg.com/lucide@latest"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>
</head>
<body class="font-sans bg-gray-50 text-gray-800 antialiased selection:bg-gold-500 selection:text-white">

    <nav class="fixed w-full z-50 transition-all duration-300 bg-navy-900/95 backdrop-blur-md border-b border-white/10 text-white" id="navbar">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-20">
                <div class="flex-shrink-0 flex items-center gap-3">
                    <i data-lucide="scale" class="w-8 h-8 text-gold-500"></i>
                    <span class="font-serif font-bold text-xl tracking-wider">ASESDE PERÚ</span>
                </div>
                <div class="hidden md:flex space-x-8">
                    <a href="#inicio" class="text-sm font-medium hover:text-gold-500 transition-colors">Inicio</a>
                    <a href="#nosotros" class="text-sm font-medium hover:text-gold-500 transition-colors">Nosotros</a>
                    <a href="#proyecto" class="text-sm font-medium hover:text-gold-500 transition-colors">Proyecto Social</a>
                    <a href="#comunidad" class="text-sm font-medium hover:text-gold-500 transition-colors">Comunidad</a>
                    <a href="#contacto" class="text-sm font-medium hover:text-gold-500 transition-colors">Contacto</a>
                </div>
            </div>
        </div>
    </nav>

    <section id="inicio" class="relative min-h-screen flex items-center pt-20 overflow-hidden bg-navy-900">
        <div class="absolute inset-0 z-0 opacity-40">
            <img src="https://images.unsplash.com/photo-1589829085413-56de8ae18c73?auto=format&fit=crop&q=80" alt="Fondo jurídico" class="w-full h-full object-cover">
            <div class="absolute inset-0 bg-gradient-to-r from-navy-900 via-navy-900/80 to-transparent"></div>
        </div>
        
        <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full">
            <div class="max-w-3xl gs-reveal">
                <h1 class="text-5xl md:text-7xl font-serif font-bold text-white leading-tight mb-6">
                    Unificando a los estudiantes de <span class="text-gold-500">Derecho del Perú</span>
                </h1>
                <p class="text-xl md:text-2xl text-gray-300 mb-10 font-light leading-relaxed">
                    Formación académica, liderazgo jurídico y compromiso social desde el 2005.
                </p>
                <div class="flex flex-col sm:flex-row gap-4">
                    <a href="#nosotros" class="inline-flex justify-center items-center px-8 py-4 bg-gold-500 text-white font-medium rounded-sm hover:bg-gold-600 transition-colors duration-300">
                        Conócenos
                    </a>
                    <a href="#comunidad" class="inline-flex justify-center items-center px-8 py-4 bg-transparent border border-white text-white font-medium rounded-sm hover:bg-white hover:text-navy-900 transition-colors duration-300">
                        Únete a la comunidad
                    </a>
                </div>
            </div>
        </div>
    </section>

    <section id="nosotros" class="py-24 bg-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-16 items-center">
                <div class="gs-reveal">
                    <h2 class="text-sm font-bold tracking-widest text-gold-500 uppercase mb-3">Nuestra Historia</h2>
                    <h3 class="text-4xl font-serif font-bold text-navy-900 mb-6">Sobre ASESDE Perú</h3>
                    <div class="w-20 h-1 bg-gold-500 mb-8"></div>
                    <p class="text-lg text-gray-600 leading-relaxed">
                        La Asociación de Estudiantes de Derecho del Perú fue fundada el 24 de septiembre del 2005 con la finalidad de unificar a todos los estudiantes de Derecho del país. El espíritu de su creación es de ámbito académico y social, contribuyendo activamente con la comunidad jurídica y la ciudadanía.
                    </p>
                </div>
                <div class="relative gs-reveal delay-200">
                    <img src="https://images.unsplash.com/photo-1505664173615-04f18947b0cc?auto=format&fit=crop&q=80" alt="Institucional" class="w-full rounded-sm shadow-2xl">
                    <div class="absolute -bottom-8 -left-8 bg-navy-900 text-white p-8 rounded-sm shadow-xl">
                        <span class="block text-4xl font-bold text-gold-500 mb-1">18+</span>
                        <span class="text-sm uppercase tracking-wider">Años de trayectoria</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="py-24 bg-gray-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="bg-white p-10 rounded-sm shadow-sm border border-gray-100 gs-reveal hover:-translate-y-2 transition-transform duration-300">
                    <div class="w-14 h-14 bg-navy-900 text-gold-500 rounded-sm flex items-center justify-center mb-6">
                        <i data-lucide="target" class="w-7 h-7"></i>
                    </div>
                    <h4 class="text-2xl font-serif font-bold text-navy-900 mb-4">Misión</h4>
                    <p class="text-gray-600 leading-relaxed">Fomentar un complemento de calidad en la formación académica y humana para cada uno de los estudiantes de Derecho a nivel nacional.</p>
                </div>
                <div class="bg-white p-10 rounded-sm shadow-sm border border-gray-100 gs-reveal delay-100 hover:-translate-y-2 transition-transform duration-300">
                    <div class="w-14 h-14 bg-navy-900 text-gold-500 rounded-sm flex items-center justify-center mb-6">
                        <i data-lucide="eye" class="w-7 h-7"></i>
                    </div>
                    <h4 class="text-2xl font-serif font-bold text-navy-900 mb-4">Visión</h4>
                    <p class="text-gray-600 leading-relaxed">Buscar una mejora continua en el desarrollo de proyectos innovadores fundamentales para la formación académica de la comunidad jurídica, ampliando oportunidades para nuestra sociedad.</p>
                </div>
                <div class="bg-white p-10 rounded-sm shadow-sm border border-gray-100 gs-reveal delay-200 hover:-translate-y-2 transition-transform duration-300">
                    <div class="w-14 h-14 bg-navy-900 text-gold-500 rounded-sm flex items-center justify-center mb-6">
                        <i data-lucide="compass" class="w-7 h-7"></i>
                    </div>
                    <h4 class="text-2xl font-serif font-bold text-navy-900 mb-4">Objetivo</h4>
                    <p class="text-gray-600 leading-relaxed">Contribuir con el desarrollo del país a través de programas sociales y académicos.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="proyecto" class="py-24 bg-navy-900 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex flex-col lg:flex-row gap-16 items-center">
                <div class="lg:w-1/2 gs-reveal">
                    <div class="grid grid-cols-2 gap-4">
                        <img src="https://images.unsplash.com/photo-1488521787991-ed7bbaae773c?auto=format&fit=crop&q=80" alt="Educación niños" class="rounded-sm w-full h-64 object-cover mt-8">
                        <img src="https://images.unsplash.com/photo-1577896851231-70ef18881754?auto=format&fit=crop&q=80" alt="Voluntariado" class="rounded-sm w-full h-64 object-cover">
                    </div>
                </div>
                <div class="lg:w-1/2 gs-reveal delay-200">
                    <h2 class="text-sm font-bold tracking-widest text-gold-500 uppercase mb-3">Impacto</h2>
                    <h3 class="text-4xl font-serif font-bold mb-6">Proyecto Social: Sonrisas con Educación</h3>
                    <div class="w-20 h-1 bg-gold-500 mb-8"></div>
                    <p class="text-lg text-gray-300 leading-relaxed mb-8">
                        Este proyecto educativo apoya actualmente a cerca de 500 niños que viven en situación de pobreza extrema en el Perú, brindándoles educación y oportunidades para un mejor futuro.
                    </p>
                    <div class="flex items-center gap-4">
                        <div class="w-12 h-12 rounded-full bg-gold-500 flex items-center justify-center">
                            <i data-lucide="heart" class="w-6 h-6 text-white"></i>
                        </div>
                        <div>
                            <span class="block text-2xl font-bold">500+</span>
                            <span class="text-sm text-gray-400">Niños beneficiados</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="comunidad" class="py-24 bg-white overflow-hidden">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="text-center max-w-3xl mx-auto mb-16 gs-reveal">
                <h2 class="text-sm font-bold tracking-widest text-gold-500 uppercase mb-3">Conexión Nacional</h2>
                <h3 class="text-4xl font-serif font-bold text-navy-900 mb-6">Nuestra Comunidad</h3>
                <div class="w-20 h-1 bg-gold-500 mx-auto mb-8"></div>
            </div>
            
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8 mb-16">
                <div class="text-center gs-reveal">
                    <div class="mx-auto w-16 h-16 bg-gray-50 rounded-full flex items-center justify-center mb-4 text-navy-900">
                        <i data-lucide="users" class="w-8 h-8"></i>
                    </div>
                    <h4 class="text-3xl font-bold text-navy-900 mb-2">17,000+</h4>
                    <p class="text-gray-600">Seguidores en redes</p>
                </div>
                <div class="text-center gs-reveal delay-100">
                    <div class="mx-auto w-16 h-16 bg-gray-50 rounded-full flex items-center justify-center mb-4 text-navy-900">
                        <i data-lucide="map-pin" class="w-8 h-8"></i>
                    </div>
                    <h4 class="text-3xl font-bold text-navy-900 mb-2">Red Nacional</h4>
                    <p class="text-gray-600">Estudiantes de todo el país</p>
                </div>
                <div class="text-center gs-reveal delay-200">
                    <div class="mx-auto w-16 h-16 bg-gray-50 rounded-full flex items-center justify-center mb-4 text-navy-900">
                        <i data-lucide="calendar" class="w-8 h-8"></i>
                    </div>
                    <h4 class="text-3xl font-bold text-navy-900 mb-2">Eventos</h4>
                    <p class="text-gray-600">Actividades académicas continuas</p>
                </div>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-4 gap-4 gs-reveal">
                <img src="https://images.unsplash.com/photo-1521737604893-d14cc237f11d?auto=format&fit=crop&q=80" alt="Estudiantes" class="w-full h-48 object-cover rounded-sm">
                <img src="https://images.unsplash.com/photo-1589391886645-d51941baf7fb?auto=format&fit=crop&q=80" alt="Auditorio" class="w-full h-48 object-cover rounded-sm">
                <img src="https://images.unsplash.com/photo-1434030216411-0b793f4b4173?auto=format&fit=crop&q=80" alt="Estudio" class="w-full h-48 object-cover rounded-sm">
                <img src="https://images.unsplash.com/photo-1541339907198-e08756dedf3f?auto=format&fit=crop&q=80" alt="Universidad" class="w-full h-48 object-cover rounded-sm">
            </div>
        </div>
    </section>

    <section class="py-24 bg-gold-500 text-white text-center">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 gs-reveal">
            <h2 class="text-4xl md:text-5xl font-serif font-bold mb-8 leading-tight">Forma parte de la red de estudiantes de Derecho más grande del Perú</h2>
            <div class="flex flex-col sm:flex-row justify-center gap-4 mt-10">
                <a href="#" class="inline-flex justify-center items-center px-8 py-4 bg-navy-900 text-white font-medium rounded-sm hover:bg-navy-800 transition-colors duration-300">
                    Postular
                </a>
                <a href="#contacto" class="inline-flex justify-center items-center px-8 py-4 bg-transparent border border-white text-white font-medium rounded-sm hover:bg-white hover:text-gold-500 transition-colors duration-300">
                    Contactar
                </a>
            </div>
        </div>
    </section>

    <footer id="contacto" class="bg-navy-900 text-gray-300 pt-20 pb-10 border-t border-white/10">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16">
                <div>
                    <div class="flex items-center gap-3 mb-6">
                        <i data-lucide="scale" class="w-8 h-8 text-gold-500"></i>
                        <span class="font-serif font-bold text-xl text-white tracking-wider">ASESDE PERÚ</span>
                    </div>
                    <p class="text-sm leading-relaxed mb-6">Promoviendo el desarrollo académico, el liderazgo jurídico y el impacto social desde el 2005.</p>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-6 tracking-wider uppercase text-sm">Enlaces Rápidos</h4>
                    <ul class="space-y-3 text-sm">
                        <li><a href="#inicio" class="hover:text-gold-500 transition-colors">Inicio</a></li>
                        <li><a href="#nosotros" class="hover:text-gold-500 transition-colors">Sobre Nosotros</a></li>
                        <li><a href="#proyecto" class="hover:text-gold-500 transition-colors">Proyecto Social</a></li>
                        <li><a href="#comunidad" class="hover:text-gold-500 transition-colors">Comunidad</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-6 tracking-wider uppercase text-sm">Contacto</h4>
                    <ul class="space-y-4 text-sm">
                        <li class="flex items-start gap-3">
                            <i data-lucide="mail" class="w-5 h-5 text-gold-500 shrink-0"></i>
                            <a href="mailto:asesde.peru@gmail.com" class="hover:text-white transition-colors">asesde.peru@gmail.com</a>
                        </li>
                        <li class="flex items-start gap-3">
                            <i data-lucide="phone" class="w-5 h-5 text-gold-500 shrink-0"></i>
                            <a href="tel:+51972564532" class="hover:text-white transition-colors">+51 972 564 532</a>
                        </li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold mb-6 tracking-wider uppercase text-sm">Síguenos</h4>
                    <div class="flex space-x-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-white/5 flex items-center justify-center hover:bg-gold-500 hover:text-white transition-all duration-300">
                            <i data-lucide="instagram" class="w-5 h-5"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-white/5 flex items-center justify-center hover:bg-gold-500 hover:text-white transition-all duration-300">
                            <i data-lucide="facebook" class="w-5 h-5"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-white/5 flex items-center justify-center hover:bg-gold-500 hover:text-white transition-all duration-300">
                            <i data-lucide="video" class="w-5 h-5"></i>
                        </a>
                    </div>
                </div>
            </div>
            
            <div class="pt-8 border-t border-white/10 text-center text-sm">
                <p>&copy; 2026 Asociación de Estudiantes de Derecho del Perú. Todos los derechos reservados.</p>
            </div>
        </div>
    </footer>

    <script type="module" src="main.js"></script>
</body>
</html>
```

### FILE: styles.css
``` css
html {
    scroll-behavior: smooth;
}

body {
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

.gs-reveal {
    opacity: 0;
    visibility: hidden;
}

::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-track {
    background: #f1f1f1;
}

::-webkit-scrollbar-thumb {
    background: #D4AF37;
    border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
    background: #AA8C2C;
}
```

### FILE: main.js
``` javascript
lucide.createIcons();

gsap.registerPlugin(ScrollTrigger);

document.addEventListener("DOMContentLoaded", () => {
    
    const reveals = document.querySelectorAll(".gs-reveal");

    reveals.forEach((elem) => {
        gsap.fromTo(elem, {
            autoAlpha: 0,
            y: 30
        }, {
            duration: 1,
            autoAlpha: 1,
            y: 0,
            ease: "power2.out",
            scrollTrigger: {
                trigger: elem,
                start: "top 85%",
                toggleActions: "play none none none"
            }
        });
    });

    const navbar = document.getElementById('navbar');
    window.addEventListener('scroll', () => {
        if (window.scrollY > 50) {
            navbar.classList.add('shadow-lg');
            navbar.classList.replace('bg-navy-900/95', 'bg-navy-900/100');
        } else {
            navbar.classList.remove('shadow-lg');
            navbar.classList.replace('bg-navy-900/100', 'bg-navy-900/95');
        }
    });

    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const targetId = this.getAttribute('href').substring(1);
            const targetElement = document.getElementById(targetId);
            
            if (targetElement) {
                window.scrollTo({
                    top: targetElement.offsetTop - 80,
                    behavior: 'smooth'
                });
            }
        });
    });
});
```<fbd4a_OUTPUT_COMPLETED>
