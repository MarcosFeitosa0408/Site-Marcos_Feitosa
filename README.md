<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Marcos Feitosa - Dados & ETL</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <style>
    /* Reset básico */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: url('grafico-fundo.jpg') no-repeat center center/cover;
      color: #333;
      line-height: 1.6;
    }

    header {
      background: linear-gradient(to right, #2563eb, white);
      padding: 15px;
      text-align: center;
    }

    header h1 {
      font-size: 24px;
      color: gold;
    }

    nav {
      margin-top: 10px;
    }

    nav a {
      display: inline-block;
      margin: 10px;
      color: #1d4ed8;
      text-decoration: none;
      font-weight: bold;
      font-size: 18px;
    }

    nav a:hover {
      color: gold;
    }

    .hero {
      text-align: center;
      padding: 40px 20px;
    }

    .hero img {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      border: 3px solid gold;
      object-fit: cover;
      margin-bottom: 20px;
    }

    .hero h2 {
      font-size: 28px;
      color: #2563eb;
    }

    .buttons {
      margin-top: 20px;
    }

    .buttons a button {
      margin: 8px;
      padding: 12px 20px;
      border: none;
      border-radius: 30px;
      font-size: 16px;
      font-weight: bold;
      cursor: pointer;
      transition: 0.3s;
      width: 80%;
      max-width: 300px;
    }

    .btn-gold {
      background: gold;
      color: white;
    }

    .btn-gold:hover {
      background: #e6b800;
      transform: scale(1.05);
    }

    .btn-blue {
      background: #2563eb;
      color: white;
    }

    .btn-blue:hover {
      background: #1d4ed8;
      transform: scale(1.05);
    }

    section {
      padding: 40px 20px;
      text-align: center;
    }

    section h3 {
      font-size: 24px;
      color: gold;
      margin-bottom: 20px;
    }

    .sobre p {
      background: rgba(0, 0, 0, 0.5);
      padding: 20px;
      color: #fff;
      border-radius: 10px;
      font-size: 18px;
      max-width: 700px;
      margin: 0 auto;
    }

    .cards {
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin-top: 30px;
      align-items: center;
    }

    .card {
      background: white;
      padding: 20px;
      border-radius: 15px;
      width: 90%;
      max-width: 300px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      text-align: center;
    }

    .card button {
      margin-top: 10px;
      padding: 10px 15px;
      font-size: 16px;
    }

    .chart-container {
      background: rgba(255, 215, 0, 0.2);
      padding: 30px;
      border-radius: 15px;
      max-width: 700px;
      margin: 0 auto;
    }

    footer {
      background: #2563eb;
      color: white;
      padding: 20px;
      text-align: center;
      margin-top: 50px;
    }

    /* Para telas maiores */
    @media (min-width: 768px) {
      nav a {
        font-size: 20px;
      }
      .cards {
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: center;
      }
      .card {
        width: 250px;
      }
    }
    .sobre-container {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 20px;
  margin-top: 30px;
}

.perfil-foto {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  object-fit: cover;
  box-shadow: 0 4px 10px rgba(0,0,0,0.2);
}

.sobre-container p {
  max-width: 500px;
  font-size: 18px;
  text-align: left;
}

  </style>
</head>

<body>

  <header>
    <h1>Marcos Feitosa</h1>
    <nav>
      <a href="#inicio">Início</a>
      <a href="#sobre">Sobre</a>
      <a href="#projetos">Projetos</a>
      <a href="#contato">Contato</a>
    </nav>
  </header>

  <section id="inicio" class="hero">
    <img src="images/perfil.png" alt="Foto de Marcos Feitosa" class="perfil-foto">
    <h2>Especialista em ETL e Dados</h2>
    <div class="buttons">
      <a href="curriculo/MarcosAFeitosa.pdf" target="_blank">

        <button class="btn-gold">Baixar Currículo</button>
      </a>
      <a href="https://wa.me/5511952247141" target="_blank">
        <button class="btn-blue">Falar por WhatsApp</button>
      </a>
    </div>
  </section>

  <section id="sobre" class="sobre">
    <h3>Sobre Mim</h3>
    <p>Sou Marcos, estudante de Análise de Dados em constante evolução. Apaixonado por transformar dados em insights valiosos, estou sempre em busca de novos conhecimentos e desafios. Neste espaço, compartilho minhas descobertas, projetos e aprendizados na jornada pelo universo dos dados.</p>
  </section>

  <section id="projetos">
    <h3>Projetos</h3>
    <div class="cards">
      <div class="card">
        <h4>Marketing</h4>
        <button class="btn-blue">Ver Projeto</button>
      </div>
      <div class="card">
        <h4>Slides</h4>
        <button class="btn-blue">Apresentação</button>
      </div>
      <div class="card">
        <h4>Planilha Excel</h4>
        <button class="btn-blue">Download</button>
      </div>
      <div class="card">
        <h4>Power BI</h4>
        <button class="btn-blue">Dashboard</button>
      </div>
    </div>
  </section>

  <section id="contato">
    <h3>Gráficos em Destaque</h3>
    <div class="chart-container">
      <canvas id="graficoProjetos"></canvas>
    </div>
    <p style="margin-top: 20px;">
      <a href="https://www.linkedin.com/in/marcos-feitosa-472197193/" target="_blank" style="color:#2563eb; text-decoration:underline;">Meu LinkedIn</a> | 
      <a href="https://www.facebook.com/profile.php?id=61575199814242" target="_blank" style="color:#2563eb; text-decoration:underline;">Meu Facebook</a>
    </p>
  </section>

  <footer>
    © 2025 Marcos Feitosa. Todos os direitos reservados.
  </footer>

  <script>
    const ctx = document.getElementById('graficoProjetos').getContext('2d');
    new Chart(ctx, {
      type: 'bar',
      data: {
        labels: ['Marketing', 'Slides', 'Excel', 'Power BI', 'Inteligência Artificial'],
        datasets: [{
          label: 'Projetos',
          data: [5, 8, 12, 7, 9],
          backgroundColor: ['gold', '#3b82f6', '#3b82f6', 'gold', '#ffd700'],
          borderRadius: 8
        }]
      },
      options: {
        scales: {
          y: { beginAtZero: true }
        },
        plugins: {
          legend: {
            labels: {
              color: '#2563eb',
              font: {
                weight: 'bold'
              }
            }
          }
        }
      }
    });
  </script>

</body>
</html>
