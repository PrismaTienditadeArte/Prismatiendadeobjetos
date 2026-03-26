<!DOCTYPE html><html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Galería de Arte</title>
<style>
  body {
    margin: 0;
    background: #f4efe9;
    font-family: sans-serif;
  }.galeria { position: relative; max-width: 900px; margin: 40px auto; }

.fondo { width: 100%; border-radius: 12px; }

.objeto { position: absolute; cursor: pointer; transition: transform 0.2s ease, filter 0.2s ease; }

.objeto:hover { transform: scale(1.1); filter: brightness(1.1); }

.popup { display: none; position: fixed; top: 50%; left: 50%; transform: translate(-50%, -50%); background: #fff8f0; padding: 20px; border-radius: 12px; box-shadow: 0 10px 30px rgba(0,0,0,0.2); width: 280px; text-align: center; }

.popup h3 { margin-top: 0; }

.cerrar { margin-top: 10px; padding: 8px 12px; border: none; background: #d6bfa9; cursor: pointer; border-radius: 6px; } </style>

</head>
<body><div class="galeria">
  <img src="fondo-galeria.jpg" class="fondo">  <!-- OBJETO 1 --><img src="objeto1.png" class="objeto" 
style="top:60%; left:40%; width:90px;"
onclick="abrirPopup('Vasija Terracota', '$18.000', 'Pieza única hecha a mano')">

  <!-- OBJETO 2 --><img src="objeto2.png" class="objeto" 
style="top:55%; left:60%; width:70px;"
onclick="abrirPopup('Escultura Minimalista', '$25.000', 'Diseño moderno en piedra')">

</div><div id="popup" class="popup">
  <h3 id="titulo"></h3>
  <p id="descripcion"></p>
  <p id="precio"></p>
  <button class="cerrar" onclick="cerrarPopup()">Cerrar</button>
</div><script>
function abrirPopup(titulo, precio, descripcion) {
  document.getElementById('titulo').innerText = titulo;
  document.getElementById('precio').innerText = precio;
  document.getElementById('descripcion').innerText = descripcion;
  document.getElementById('popup').style.display = 'block';
}

function cerrarPopup() {
  document.getElementById('popup').style.display = 'none';
}
</script></body>
</html>
.galeria {
  position: relative;
  width: 100%;
  height: 100vh;
  margin: 0;

  background-image: url('fachada2.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
