
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Consultorio Dental</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
    <style>
        body { font-family: Arial, sans-serif; }
        .hero { background: url('https://source.unsplash.com/1600x900/?university') center/cover; height: 60vh; color: white; display: flex; align-items: center; justify-content: center; text-align: center; }
        .hero h1 { font-size: 3rem; }
    </style>
</head>
<body>
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#">Consultorio Dental</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav ms-auto">
                    <li class="nav-item"><a class="nav-link" href="#about">Sobre Nosotros</a></li>
                    <li class="nav-item"><a class="nav-link" href="#services">Servicios</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contact">Contacto</a></li>
                </ul>
            </div>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <section class="hero">
        <h1>Bienvenido al Consultorio</h1>
    </section>
    
    <!-- Sobre Nosotros -->
    <section id="about" class="container py-5">
        <h2 class="text-center">Sobre Nosotros</h2>
        <p class="text-center">Somos un consultorio dental de excelencia con más de 10 años de experiencia.</p>
    </section>
    
    <!-- Servicios -->
    <section id="services" class="bg-light py-5">
        <div class="container">
            <h2 class="text-center">Nuestros Servicios</h2>
            <div class="row">
                <div class="col-md-4 text-center">
                    <h4>Educación de Calidad</h4>
                    <p>Contamos con los mejores tratamientos dentales.</p>
                </div>
                <div class="col-md-4 text-center">
                    <h4>Resinas</h4>
                    <p>Las resinas de alta estética es una solución para corregir: pequeñas imperfecciones, fracturas menores, caries, alteraciones de color, formas inadecuadas, dientes pequeños, etc.</p>
                </div>
                <div class="col-md-4 text-center">
                    <h4>Dentistas</h4>
                    <p>En La Clínica Dental disponemos de un equipo profesional de dentistas altamente calificados, comprometidos en ofrecerte un servicio de calidad con tecnología de avanzada.</p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Contacto -->
    <section id="contact" class="container py-5">
        <h2 class="text-center">Contacto</h2>
        <form id="contactForm">
            <div class="mb-3">
                <label class="form-label">Nombre</label>
                <input type="text" class="form-control" required>
            </div>
            <div class="mb-3">
                <label class="form-label">Correo Electrónico</label>
                <input type="email" class="form-control" required>
            </div>
            <div class="mb-3">
                <label class="form-label">Mensaje</label>
                <textarea class="form-control" rows="4" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary">Enviar</button>
        </form>
    </section>
    
    <!-- Footer -->
    <footer class="bg-dark text-white text-center py-3">
        <p>&copy; 2025 Clinica Dental. Todos los derechos reservados.</p>
    </footer>
    
    <script>
        document.getElementById("contactForm").addEventListener("submit", function(event) {
            event.preventDefault();
            alert("Formulario enviado correctamente");
        });
    </script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
