<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Renova: Medicina y Bienestar Integral</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Inter font from Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* Define your custom color palette */
        :root {
            --color-renova-dark-blue: #1A2B4C; /* Azul Marino */
            --color-renova-gold: #FFD700;    /* Dorado */
            --color-renova-fuchsia: #FF007F; /* Fucsia */
            --color-renova-light-blue: #66B3FF; /* Un azul más claro para contrastes */
            --color-renova-text-dark: #333;
            --color-renova-text-light: #f0f4f8;
        }

        body {
            font-family: 'Inter', sans-serif;
            background-color: var(--color-renova-text-light);
            color: var(--color-renova-text-dark);
        }
        .text-renova-dark-blue { color: var(--color-renova-dark-blue); }
        .bg-renova-dark-blue { background-color: var(--color-renova-dark-blue); }
        .border-renova-dark-blue { border-color: var(--color-renova-dark-blue); }

        .text-renova-gold { color: var(--color-renova-gold); }
        .bg-renova-gold { background-color: var(--color-renova-gold); }
        .border-renova-gold { border-color: var(--color-renova-gold); }

        .text-renova-fuchsia { color: var(--color-renova-fuchsia); }
        .bg-renova-fuchsia { background-color: var(--color-renova-fuchsia); }
        .border-renova-fuchsia { border-color: var(--color-renova-fuchsia); }

        .btn-renova {
            background-color: var(--color-renova-fuchsia); /* Usamos fucsia para los botones principales */
            color: white;
            padding: 0.75rem 1.5rem;
            border-radius: 9999px; /* Fully rounded */
            transition: background-color 0.3s ease, transform 0.2s ease;
        }
        .btn-renova:hover {
            background-color: #CC0066; /* Un fucsia más oscuro al pasar el ratón */
            transform: translateY(-2px);
        }
        .section-title {
            position: relative;
            padding-bottom: 0.5rem;
            margin-bottom: 1.5rem;
        }
        .section-title::after {
            content: '';
            position: absolute;
            left: 0;
            bottom: 0;
            width: 70px; /* Un poco más ancho */
            height: 4px;
            background-color: var(--color-renova-fuchsia); /* Línea fucsia */
            border-radius: 2px;
        }
        .card {
            background-color: white;
            border-radius: 1rem; /* Más redondeado */
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            padding: 1.5rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15);
        }
        .nav-link {
            transition: color 0.3s ease;
        }
        .nav-link:hover {
            color: var(--color-renova-fuchsia);
        }
        .gradient-bg {
            /* Degradado usando los colores de Renova */
            background: linear-gradient(to right, var(--color-renova-dark-blue), var(--color-renova-light-blue));
        }
        .gradient-text {
            /* Texto con degradado si se desea para títulos */
            background: linear-gradient(to right, var(--color-renova-fuchsia), var(--color-renova-gold));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .gallery-item {
            overflow: hidden;
            border-radius: 1rem;
            box-shadow: 0 4px 10px rgba(0,0,0,0.1);
        }
        .gallery-item img {
            width: 100%;
            height: 250px; /* Altura fija para la galería */
            object-fit: cover; /* Asegura que la imagen cubra el área sin distorsión */
            transition: transform 0.3s ease;
        }
        .gallery-item:hover img {
            transform: scale(1.05); /* Pequeño zoom al pasar el ratón */
        }
    </style>
</head>
<body class="antialiased">

    <!-- Header / Navbar -->
    <header class="bg-white shadow-md py-4 sticky top-0 z-50">
        <nav class="container mx-auto px-6 flex justify-between items-center">
            <div class="flex items-center">
                <img src="image.png" alt="Logo Renova" class="h-10 w-auto mr-3 rounded-md"> <!-- Logo de Renova -->
                <div class="text-2xl font-bold text-renova-dark-blue">Renova</div>
            </div>
            <div class="hidden md:flex space-x-8">
                <a href="#inicio" class="nav-link text-gray-700 hover:text-renova-fuchsia font-medium">Inicio</a>
                <a href="#servicios" class="nav-link text-gray-700 hover:text-renova-fuchsia font-medium">Servicios</a>
                <a href="#equipo" class="nav-link text-gray-700 hover:text-renova-fuchsia font-medium">Nuestro Equipo</a>
                <a href="#galeria" class="nav-link text-gray-700 hover:text-renova-fuchsia font-medium">Galería</a>
                <a href="#cursos" class="nav-link text-gray-700 hover:text-renova-fuchsia font-medium">Cursos</a>
                <a href="#libros" class="nav-link text-gray-700 hover:text-renova-fuchsia font-medium">Libros</a>
                <a href="#contacto" class="nav-link text-gray-700 hover:text-renova-fuchsia font-medium">Contacto</a>
            </div>
            <!-- Mobile Menu Button -->
            <button id="mobile-menu-button" class="md:hidden text-gray-600 focus:outline-none">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </nav>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden bg-white py-4 mt-2 shadow-lg rounded-lg mx-4">
            <a href="#inicio" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Inicio</a>
            <a href="#servicios" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Servicios</a>
            <a href="#equipo" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Nuestro Equipo</a>
            <a href="#galeria" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Galería</a>
            <a href="#cursos" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Cursos</a>
            <a href="#libros" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Libros</a>
            <a href="#contacto" class="block px-4 py-2 text-gray-700 hover:bg-gray-100 rounded-md">Contacto</a>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="inicio" class="gradient-bg text-white py-20 md:py-32 rounded-b-3xl shadow-lg">
        <div class="container mx-auto px-6 text-center">
            <!-- Placeholder for Dr. Daniel's photo, consider using a professional headshot here -->
            <img src="https://placehold.co/150x150/FFD700/1A2B4C?text=Dr.D" alt="Foto del Dr. Daniel Camero" class="rounded-full w-36 h-36 mx-auto mb-6 border-4 border-renova-gold shadow-lg object-cover">
            <h1 class="text-4xl md:text-5xl font-extrabold leading-tight mb-4">Dr. Daniel Camero Caballero</h1>
            <p class="text-xl md:text-2xl mb-8 font-light">Médico Cirujano | Especialista en Bienestar y Medicina Integrativa</p>
            <p class="text-lg md:text-xl mb-10 max-w-2xl mx-auto">
                Con mi marca personal <span class="font-semibold text-renova-gold">Renova</span>, te ofrezco una visión integral de la salud, combinando la medicina tradicional con enfoques innovadores para tu bienestar total.
            </p>
            <a href="#contacto" class="btn-renova text-lg font-semibold inline-block shadow-lg hover:shadow-xl">Agenda tu Consulta</a>
        </div>
    </section>

    <!-- About Me Section -->
    <section id="sobre-mi" class="py-16 md:py-24 bg-white rounded-xl shadow-lg mx-4 md:mx-auto -mt-16 relative z-10 max-w-5xl">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-renova-dark-blue section-title mb-8">Sobre Mí</h2>
            <div class="grid md:grid-cols-2 gap-10 items-center">
                <div>
                    <p class="text-lg text-gray-700 mb-4 leading-relaxed">
                        Soy el <span class="font-semibold text-renova-dark-blue">Dr. Daniel Andrés de Jesús Camero Caballero</span>, un médico cirujano venezolano con una profunda pasión por la salud y el bienestar. Mi trayectoria profesional se ha centrado en ofrecer una atención médica de calidad, combinando mi experiencia en medicina general con una constante búsqueda de conocimientos en terapias complementarias.
                    </p>
                    <p class="text-lg text-gray-700 mb-4 leading-relaxed">
                        Como <span class="font-semibold text-renova-dark-blue">Docente Universitario</span>, comparto mi conocimiento en la Escuela de Medicina "José Francisco Torrealba" en la Universidad Nacional Experimental Rómulo Gallegos. Mi compromiso con la educación y la innovación me ha llevado a diplomarme en <span class="font-semibold text-renova-dark-blue">Sueroterapia y Medicina Orthomolecular</span>, <span class="font-semibold text-renova-dark-blue">Plasma Rico en Plaquetas</span>, y más recientemente, en <span class="font-semibold text-renova-dark-blue">Terapia Neural</span>, una técnica que busca restaurar el equilibrio del sistema nervioso para aliviar diversas afecciones.
                    </p>
                    <p class="text-lg text-gray-700 leading-relaxed">
                        Además de mi práctica médica, soy un <span class="font-semibold text-renova-dark-blue">escritor apasionado</span>. Mis libros, como "El Mito de la Vocación", exploran temas de crecimiento personal y profesional, buscando inspirar a otros a encontrar su propósito y renovar su perspectiva de vida.
                    </p>
                </div>
                <div class="flex justify-center">
                    <!-- Placeholder for Dr. Daniel's photo, consider using a professional headshot here -->
                    <img src="https://placehold.co/400x300/FFD700/1A2B4C?text=Dr.+Daniel+Camero" alt="Dr. Daniel Camero en consulta" class="rounded-2xl shadow-xl w-full max-w-md object-cover">
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="servicios" class="py-16 md:py-24 bg-gray-50">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-renova-dark-blue section-title mb-12 text-center">Nuestros Servicios Médicos Renova</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Servicio 1: Medicina General -->
                <div class="card">
                    <div class="text-renova-fuchsia text-5xl mb-4 text-center"><i class="fas fa-stethoscope"></i></div>
                    <h3 class="text-2xl font-semibold mb-3 text-center text-renova-dark-blue">Consulta de Medicina General</h3>
                    <p class="text-gray-600 text-center">
                        Diagnóstico y tratamiento de enfermedades comunes, chequeos preventivos y seguimiento de tu salud.
                    </p>
                </div>
                <!-- Servicio 2: Sueroterapia y Medicina Orthomolecular -->
                <div class="card">
                    <div class="text-renova-fuchsia text-5xl mb-4 text-center"><i class="fas fa-syringe"></i></div>
                    <h3 class="text-2xl font-semibold mb-3 text-center text-renova-dark-blue">Sueroterapia y Medicina Orthomolecular</h3>
                    <p class="text-gray-600 text-center">
                        Terapias intravenosas con vitaminas, minerales y nutrientes para optimizar tu salud, energía y bienestar.
                    </p>
                </div>
                <!-- Servicio 3: Plasma Rico en Plaquetas (PRP) -->
                <div class="card">
                    <div class="text-renova-fuchsia text-5xl mb-4 text-center"><i class="fas fa-tint"></i></div>
                    <h3 class="text-2xl font-semibold mb-3 text-center text-renova-dark-blue">Plasma Rico en Plaquetas (PRP)</h3>
                    <p class="text-gray-600 text-center">
                        Aplicaciones de PRP para regeneración de tejidos, estética y tratamientos capilares.
                    </p>
                </div>
                <!-- Servicio 4: Terapia Neural -->
                <div class="card">
                    <div class="text-renova-fuchsia text-5xl mb-4 text-center"><i class="fas fa-brain"></i></div>
                    <h3 class="text-2xl font-semibold mb-3 text-center text-renova-dark-blue">Terapia Neural</h3>
                    <p class="text-gray-600 text-center">
                        Enfoque terapéutico para aliviar el dolor y restaurar la función del sistema nervioso.
                    </p>
                </div>
                <!-- Servicio 5: Masajes Linfáticos y Estéticos -->
                <div class="card">
                    <div class="text-renova-fuchsia text-5xl mb-4 text-center"><i class="fas fa-hand-sparkles"></i></div>
                    <h3 class="text-2xl font-semibold mb-3 text-center text-renova-dark-blue">Masajes Linfáticos y Estéticos</h3>
                    <p class="text-gray-600 text-center">
                        Terapias manuales para mejorar la circulación, reducir la retención de líquidos y promover el bienestar estético.
                    </p>
                </div>
                 <!-- Servicio 6: Asesoría en Bienestar Integral -->
                <div class="card">
                    <div class="text-renova-fuchsia text-5xl mb-4 text-center"><i class="fas fa-heartbeat"></i></div>
                    <h3 class="text-2xl font-semibold mb-3 text-center text-renova-dark-blue">Asesoría en Bienestar Integral</h3>
                    <p class="text-gray-600 text-center">
                        Planes personalizados para mejorar tu estilo de vida, nutrición y salud emocional.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Team Section -->
    <section id="equipo" class="py-16 md:py-24 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-renova-dark-blue section-title mb-12 text-center">Nuestro Equipo Renova</h2>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-center">
                <!-- Team Photo -->
                <div class="flex justify-center lg:col-span-2 mb-8">
                    <img src="team_photo.png" alt="Foto del Dr. Daniel Camero y Dra. Andreina Silva" class="rounded-2xl shadow-xl w-full max-w-2xl object-cover">
                </div>

                <!-- Miembro del Equipo 1: Dr. Daniel Camero -->
                <div class="card p-6 flex flex-col items-center text-center">
                    <!-- Placeholder for Dr. Daniel's individual photo -->
                    <img src="https://placehold.co/120x120/FFD700/1A2B4C?text=Dr.D" alt="Foto del Dr. Daniel Camero" class="rounded-full w-32 h-32 mb-4 border-4 border-renova-gold object-cover">
                    <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Dr. Daniel Camero Caballero</h3>
                    <p class="text-renova-fuchsia font-medium mb-3">Médico Cirujano</p>
                    <p class="text-gray-600">
                        Fundador de Renova, especialista en medicina integrativa, sueroterapia, PRP y terapia neural. Apasionado por el bienestar y la educación.
                    </p>
                    <a href="#sobre-mi" class="mt-4 text-renova-fuchsia hover:underline font-medium">Ver perfil completo</a>
                </div>

                <!-- Miembro del Equipo 2: Dra. Andreina Silva -->
                <div class="card p-6 flex flex-col items-center text-center">
                    <!-- Placeholder for Dra. Andreina's individual photo -->
                    <img src="https://placehold.co/120x120/FFD700/1A2B4C?text=Dra.A" alt="Foto de la Dra. Andreina Silva" class="rounded-full w-32 h-32 mb-4 border-4 border-renova-gold object-cover">
                    <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Dra. Andreina Silva Arellano</h3>
                    <p class="text-renova-fuchsia font-medium mb-3">Médico Cirujano | Cosmiatra</p>
                    <p class="text-gray-600">
                        Co-fundadora de Renova, con experiencia en medicina general y especializada en cosmiatría facial y corporal, y masajes estéticos.
                    </p>
                    <a href="#sobre-andreina" class="mt-4 text-renova-fuchsia hover:underline font-medium">Ver perfil completo</a>
                </div>
            </div>
        </div>
    </section>

    <!-- About Andreina Section -->
    <section id="sobre-andreina" class="py-16 md:py-24 bg-gray-50 rounded-xl shadow-lg mx-4 md:mx-auto relative z-10 max-w-5xl">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-renova-dark-blue section-title mb-8">Sobre la Dra. Andreina Silva</h2>
            <div class="grid md:grid-cols-2 gap-10 items-center">
                <div class="flex justify-center order-2 md:order-1">
                    <!-- Image for Dra. Andreina applying capillary plasma -->
                    <img src="andreina_plasma_capilar.png" alt="Dra. Andreina Silva aplicando plasma capilar" class="rounded-2xl shadow-xl w-full max-w-md object-cover">
                </div>
                <div class="order-1 md:order-2">
                    <p class="text-lg text-gray-700 mb-4 leading-relaxed">
                        La <span class="font-semibold text-renova-dark-blue">Dra. Andreina Nazareth Silva Arellano</span> es una Médico Cirujano con una sólida formación en medicina general y una especialización en el área de la estética y el bienestar. Su enfoque se centra en la salud integral y la mejora de la calidad de vida de sus pacientes.
                    </p>
                    <p class="text-lg text-gray-700 mb-4 leading-relaxed">
                        Andreina ha complementado su formación con diplomados en <span class="font-semibold text-renova-dark-blue">Cosmiatría Facial y Corporal</span>, así como en <span class="font-semibold text-renova-dark-blue">Estética Facial y Corporal</span>. Su experiencia incluye la práctica como Masajista Estética y anti-estrés, y como Docente Universitario, compartiendo su conocimiento en la Escuela de Medicina "José Francisco Torrealba".
                    </p>
                    <p class="text-lg text-gray-700 leading-relaxed">
                        Su compromiso con Renova es ofrecer servicios que no solo traten afecciones, sino que también promuevan la belleza y el bienestar desde una perspectiva médica y holística.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Photo Gallery Section -->
    <section id="galeria" class="py-16 md:py-24 bg-white">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-renova-dark-blue section-title mb-12 text-center">Galería de Fotos Renova</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- Daniel: PRP Facial -->
                <div class="gallery-item">
                    <img src="daniel_prp_facial.png" alt="Dr. Daniel Camero aplicando PRP facial">
                    <p class="p-4 text-gray-700 text-center font-medium">Dr. Daniel Camero - Aplicación de PRP Facial</p>
                </div>
                <!-- Andreina: PRP Capilar (Otro Ángulo) -->
                <div class="gallery-item">
                    <img src="andreina_prp_capilar_2.png" alt="Dra. Andreina Silva aplicando PRP capilar">
                    <p class="p-4 text-gray-700 text-center font-medium">Dra. Andreina Silva - Sesión de PRP Capilar</p>
                </div>
                <!-- Andreina: En Consultorio -->
                <div class="gallery-item">
                    <img src="andreina_consultorio.png" alt="Dra. Andreina Silva en su consultorio">
                    <p class="p-4 text-gray-700 text-center font-medium">Dra. Andreina Silva en Consultorio</p>
                </div>
                <!-- Daniel: En Consultorio -->
                <div class="gallery-item">
                    <img src="daniel_consultorio.png" alt="Dr. Daniel Camero en su consultorio">
                    <p class="p-4 text-gray-700 text-center font-medium">Dr. Daniel Camero en Consultorio</p>
                </div>
                <!-- Daniel: Dando Clases 1 -->
                <div class="gallery-item">
                    <img src="daniel_clase_1.png" alt="Dr. Daniel Camero dando clases en la universidad">
                    <p class="p-4 text-gray-700 text-center font-medium">Dr. Daniel Camero - Docencia Universitaria</p>
                </div>
                <!-- Daniel: Dando Clases 2 -->
                <div class="gallery-item">
                    <img src="daniel_clase_2.png" alt="Dr. Daniel Camero dando clases en la universidad">
                    <p class="p-4 text-gray-700 text-center font-medium">Dr. Daniel Camero - Clases en la Universidad</p>
                </div>
                <!-- Daniel: Jornada Médica -->
                <div class="gallery-item">
                    <img src="daniel_jornada_medica.png" alt="Dr. Daniel Camero en jornada médica">
                    <p class="p-4 text-gray-700 text-center font-medium">Dr. Daniel Camero - Consulta en Jornada Médica</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Courses Section -->
    <section id="cursos" class="py-16 md:py-24 bg-gray-50">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-renova-dark-blue section-title mb-12 text-center">Cursos y Formación</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <!-- Curso Daniel: Diplomado en Sueroterapia y Medicina Orthomolecular -->
                <div class="card flex items-start p-6">
                    <div class="text-renova-fuchsia text-4xl mr-6"><i class="fas fa-graduation-cap"></i></div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Diplomado en Sueroterapia y Medicina Orthomolecular (Dr. Daniel)</h3>
                        <p class="text-gray-600 mb-2">
                            Realizado en San Juan de los Morros, Estado Guárico. Octubre 2024.
                        </p>
                        <p class="text-gray-500 text-sm">
                            Consultorio Médico Estético GAINARU.
                        </p>
                    </div>
                </div>
                <!-- Curso Daniel: Diplomado en Plasma Rico en Plaquetas -->
                <div class="card flex items-start p-6">
                    <div class="text-renova-fuchsia text-4xl mr-6"><i class="fas fa-vial"></i></div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Diplomado en Plasma Rico en Plaquetas (Dr. Daniel)</h3>
                        <p class="text-gray-600 mb-2">
                            Realizado en Maracay, Estado Aragua. Octubre 2024.
                        </p>
                        <p class="text-gray-500 text-sm">
                            Centro Médico Estético Bio-Skin.
                        </p>
                    </div>
                </div>
                <!-- Curso Daniel: Diplomado en Terapia Neural (Nuevo) -->
                <div class="card flex items-start p-6">
                    <div class="text-renova-fuchsia text-4xl mr-6"><i class="fas fa-hand-holding-medical"></i></div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Diplomado en Terapia Neural (Dr. Daniel)</h3>
                        <p class="text-gray-600 mb-2">
                            Recientemente culminado, ampliando mis conocimientos en el equilibrio del sistema nervioso.
                        </p>
                        <p class="text-gray-500 text-sm">
                            (Detalles de la institución y fecha se actualizarán pronto)
                        </p>
                    </div>
                </div>
                <!-- Curso Andreina: Diplomado Cosmiatría Facial y Corporal -->
                <div class="card flex items-start p-6">
                    <div class="text-renova-fuchsia text-4xl mr-6"><i class="fas fa-spa"></i></div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Diplomado Cosmiatría Facial y Corporal (Dra. Andreina)</h3>
                        <p class="text-gray-600 mb-2">
                            Instituto Capacítate Barquisimeto. Julio - Septiembre 2022.
                        </p>
                        <p class="text-gray-500 text-sm">
                            Especialización en tratamientos estéticos avanzados.
                        </p>
                    </div>
                </div>
                <!-- Curso Andreina: Diplomado Estética Facial y Corporal -->
                <div class="card flex items-start p-6">
                    <div class="text-renova-fuchsia text-4xl mr-6"><i class="fas fa-face-flushed"></i></div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Diplomado Estética Facial y Corporal (Dra. Andreina)</h3>
                        <p class="text-gray-600 mb-2">
                            Instituto Capacítate Barquisimeto. Julio - Septiembre 2022.
                        </p>
                        <p class="text-gray-500 text-sm">
                            Formación integral en procedimientos estéticos.
                        </p>
                    </div>
                </div>
                <!-- Curso Andreina: Diplomado Especialización en Cosmetología Facial y Corporal -->
                <div class="card flex items-start p-6">
                    <div class="text-renova-fuchsia text-4xl mr-6"><i class="fas fa-mask"></i></div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Diplomado Especialización en Cosmetología Facial y Corporal (Dra. Andreina)</h3>
                        <p class="text-gray-600 mb-2">
                            Instituto Gerardi Studio, Maracay. Julio 2022.
                        </p>
                        <p class="text-gray-500 text-sm">
                            Profundización en técnicas de cosmetología.
                        </p>
                    </div>
                </div>
                <!-- Curso General: Participación en Congresos de COVID-19 -->
                <div class="card flex items-start p-6">
                    <div class="text-renova-fuchsia text-4xl mr-6"><i class="fas fa-viruses"></i></div>
                    <div>
                        <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Congresos Internacionales de COVID-19</h3>
                        <p class="text-gray-600 mb-2">
                            Participación en múltiples sesiones sobre generalidades, vacunas, cuidados en casa y síndrome inflamatorio multisistémico pediátrico. Junio 2021.
                        </p>
                        <p class="text-gray-500 text-sm">
                            Ambos médicos participaron en estos congresos.
                        </p>
                    </div>
                </div>
                <!-- Agrega más cursos y formaciones aquí siguiendo el mismo patrón -->
            </div>
        </div>
    </section>

    <!-- Books Section -->
    <section id="libros" class="py-16 md:py-24 bg-gray-50">
        <div class="container mx-auto px-6">
            <h2 class="text-3xl md:text-4xl font-bold text-renova-dark-blue section-title mb-12 text-center">Mis Libros</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Libro 1: El Mito de la Vocación -->
                <div class="card text-center p-6">
                    <img src="el_mito_de_la_vocacion.png" alt="Portada del libro El Mito de la Vocación" class="mx-auto mb-6 rounded-lg shadow-md w-auto h-64 object-contain">
                    <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">El Mito de la Vocación</h3>
                    <p class="text-gray-600 mb-4">
                        Mi obra más reciente, donde exploro la idea de la vocación y cómo podemos encontrar nuestro camino y propósito en la vida, más allá de las expectativas.
                    </p>
                    <a href="#" class="btn-renova text-sm font-semibold inline-block">Más Información / Comprar</a>
                </div>
                <!-- Añadir más libros aquí si tienes -->
                <div class="card text-center p-6">
                    <img src="https://placehold.co/200x300/A0A0A0/FFFFFF?text=Próximamente" alt="Portada de próximo libro" class="mx-auto mb-6 rounded-lg shadow-md">
                    <h3 class="text-2xl font-semibold mb-2 text-renova-dark-blue">Próximamente...</h3>
                    <p class="text-gray-600 mb-4">
                        Estoy trabajando en nuevas ideas y proyectos literarios para seguir compartiendo conocimientos y reflexiones. ¡Mantente atento!
                    </p>
                    <a href="#" class="btn-renova text-sm font-semibold inline-block opacity-75 cursor-not-allowed">No Disponible</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto" class="py-16 md:py-24 bg-renova-dark-blue text-white rounded-t-3xl shadow-lg">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-3xl md:text-4xl font-bold section-title mb-12 text-center text-renova-gold">Contacta con Renova</h2>
            <p class="text-xl mb-8 max-w-2xl mx-auto">
                ¿Listo para renovar tu salud y bienestar? Contáctanos para agendar una consulta o para cualquier pregunta.
            </p>
            <div class="flex flex-col md:flex-row justify-center items-center gap-8">
                <div class="flex items-center text-lg">
                    <i class="fas fa-phone-alt text-3xl mr-4 text-renova-gold"></i>
                    <span>0412-4740016 | 0412-8622772</span>
                </div>
                <div class="flex items-center text-lg">
                    <i class="fas fa-envelope text-3xl mr-4 text-renova-gold"></i>
                    <span>danielcamerocd@gmail.com | andreinasilva200917@gmail.com</span>
                </div>
                <div class="flex items-center text-lg">
                    <i class="fas fa-map-marker-alt text-3xl mr-4 text-renova-gold"></i>
                    <span>Maracay, Estado Aragua, Venezuela</span>
                </div>
            </div>
            <div class="mt-12">
                <h3 class="text-2xl font-semibold mb-6 text-renova-gold">Síguenos en Redes Sociales</h3>
                <div class="flex justify-center space-x-6">
                    <a href="#" class="text-renova-gold hover:text-renova-fuchsia text-4xl transition-colors duration-300"><i class="fab fa-instagram"></i></a>
                    <a href="#" class="text-renova-gold hover:text-renova-fuchsia text-4xl transition-colors duration-300"><i class="fab fa-facebook-f"></i></a>
                    <a href="#" class="text-renova-gold hover:text-renova-fuchsia text-4xl transition-colors duration-300"><i class="fab fa-linkedin-in"></i></a>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8">
        <div class="container mx-auto px-6 text-center">
            <p>&copy; 2025 Renova. Todos los derechos reservados.</p>
            <p class="mt-2 text-sm">Diseñado con pasión por el bienestar.</p>
        </div>
    </footer>

    <script>
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Mobile menu toggle
        const mobileMenuButton = document.getElementById('mobile-menu-button');
        const mobileMenu = document.getElementById('mobile-menu');

        mobileMenuButton.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });

        // Close mobile menu when a link is clicked
        mobileMenu.querySelectorAll('a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });
    </script>
</body>
</html>
