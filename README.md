<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Acerca de mí</title>
  <!-- Bootstrap 5  -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    body {
      background-color: #c9c9c9f1;
      font-family: 'Poppins', sans-serif;
    }
    h1 {
      margin-bottom: 30px;
      color: #007BFF;
      font-weight: 700;
    }
    .card {
      border: none;
      border-radius: 15px;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .card:hover {
      transform: translateY(-10px);
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    }
    .btn-custom {
      background-color: #007BFF;
      border: none;
      color: white;
      transition: background-color 0.3s;
    }
    .btn-custom:hover {
      background-color: #0056b3;
    }
    .img-fluid {
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <div class="container py-5">
    <h1 class="text-center">Acerca de mí</h1>
    <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-4">
      <div class="col">
        <div class="card h-100">
          <div class="card-body">
            <h5 class="card-title">Persona a quien admiro</h5>
            <p class="card-text" id="personaTexto">Haz click para saber más...</p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card h-100">
          <div class="card-body">
            <h5 class="card-title">Meta que quiero lograr</h5>
            <p class="card-text">Seguir aprendiendo y creciendo en el mundo de los sistemas y las redes.</p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card h-100">
          <div class="card-body">
            <h5 class="card-title">Género musical favorito</h5>
            <p class="card-text" id="musicaTexto">Haz doble click para descubrir...</p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card h-100">
          <div class="card-body">
            <h5 class="card-title">Algo sin lo que no podría vivir</h5>
            <p class="card-text" id="esencialTexto">Haz click para saber más...</p>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card h-100">
          <div class="card-body">
            <h5 class="card-title">Un talento que poseo</h5>
            <button class="btn btn-custom" id="mostrarTalento">Descubre mi talento</button>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card h-100">
          <div class="card-body text-center">
            <h5 class="card-title">Mi animal favorito</h5>
            <button class="btn btn-primary" id="mostrarModal">Haz clic para ver</button>
          </div>
        </div>
      </div>
    </div>
  </div>

 
  <div class="modal fade" id="modalAnimal" tabindex="-1" aria-labelledby="modalAnimalLabel" aria-hidden="true">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="modalAnimalLabel">Mi animal favorito son los perros.</h5>
          <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
        </div>
        <div class="modal-body text-center">
          <img src="perritos.jpg" alt="Animal favorito" class="img-fluid">
        </div>
      </div>
    </div>
  </div>


  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
  <script>
    document.getElementById("mostrarModal").addEventListener("click", function() {
      const modal = new bootstrap.Modal(document.getElementById("modalAnimal"));
      modal.show();
    });

    document.querySelector("#personaTexto").addEventListener("click", function() {
      this.textContent = "Admiro a mi madre por su perseverancia y dedicación.";
    });

    document.querySelector("#musicaTexto").addEventListener("dblclick", function() {
      this.textContent = "¡Mi género favorito es el Pop!";
    });

    document.querySelector("#esencialTexto").addEventListener("click", function() {
      this.textContent = "No puedo vivir sin oxígeno… aunque lo he intentado.";
    });

    document.querySelector("#mostrarTalento").addEventListener("click", function() {
      alert("Mi talento está en proceso de actualización… ¡pronto lo sabré!");
    });
  </script>
</body>
</html>
