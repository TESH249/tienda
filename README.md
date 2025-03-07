<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>La Clínica Dental</title>
    <link rel="stylesheet" href="styles.css">
    <script src="https://www.paypal.com/sdk/js?client-id=TU_CLIENT_ID"></script>
</head>
<body>
    <header>
        <h1>La Clínica Dental</h1>
        <nav>
            <ul>
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#tratamientos">Tratamientos</a></li>
                <li><a href="#contacto">Contacto</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="inicio">
        <h2>Bienvenido a La Clínica Dental</h2>
        <p>Tu salud dental es nuestra prioridad.</p>
    </section>
    
    <section id="chat">
        <h3>Chat en línea</h3>
        <div id="chat-box">
            <p><strong>Operador:</strong> ¡Bienvenido! ¿En qué podemos ayudarle?</p>
        </div>
        <input type="text" id="user-message" placeholder="Escribe tu mensaje...">
        <button onclick="sendMessage()">Enviar</button>
    </section>
    
    <section id="pago">
        <h3>Paga tu cita en línea</h3>
        <div id="paypal-button-container"></div>
    </section>
    
    <footer>
        <p>Contacto: contacto@laclinica.mx</p>
    </footer>
    
    <script>
        function sendMessage() {
            let message = document.getElementById("user-message").value;
            if (message) {
                let chatBox = document.getElementById("chat-box");
                chatBox.innerHTML += `<p><strong>Tú:</strong> ${message}</p>`;
                document.getElementById("user-message").value = "";
            }
        }
        
        paypal.Buttons({
            createOrder: function(data, actions) {
                return actions.order.create({
                    purchase_units: [{
                        amount: { value: '50.00' } // Precio de la cita
                    }]
                });
            },
            onApprove: function(data, actions) {
                return actions.order.capture().then(function(details) {
                    alert('Pago completado por ' + details.payer.name.given_name);
                });
            }
        }).render('#paypal-button-container');
    </script>
</body>
</html>
