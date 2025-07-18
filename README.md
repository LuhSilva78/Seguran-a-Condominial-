# Segurança-a-Condominial-
Controle de Segurança para Condominio 
index.html
<link rel="stylesheet" href="style.css">


  <div class="container">
    <h1>🏠 Sistema de Segurança do Condomínio</h1>
    
    <section class="gate-control">
      <h2>🔓 Controle de Portão</h2>
      <button onclick="abrirPortao()">Abrir Portão</button>
      <p id="statusPortao"></p>
    </section>

    <section class="notifications">
      <h2>📦 Notificações de Encomendas</h2>
      <input type="text" id="inputNotificacao" placeholder="Digite a notificação...">
      <button onclick="enviarNotificacao()">Enviar Notificação</button>
      <ul id="listaNotificacoes"></ul>
    </section>
  </div>

  <script src="script.js"></script>

  style.css

body {
  font-family: Arial, sans-serif;
  background-color: #f0f2f5;
  margin: 0;
  padding: 0;
}

.container {
  max-width: 600px;
  margin: 30px auto;
  padding: 20px;
  background: white;
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

h1 {
  text-align: center;
  margin-bottom: 30px;
}

section {
  margin-bottom: 30px;
}

button {
  background-color: #4CAF50;
  color: white;
  border: none;
  padding: 12px 20px;
  margin-top: 10px;
  border-radius: 8px;
  cursor: pointer;
}

button:hover {
  background-color: #45a049;
}

input[type="text"] {
  width: 100%;
  padding: 10px;
  margin-top: 10px;
  border-radius: 8px;
  border: 1px solid #ccc;
}

#listaNotificacoes {
  list-style-type: none;
  padding: 0;
  margin-top: 15px;
}

#listaNotificacoes li {
  background: #eee;
  padding: 10px;
  margin-bottom: 5px;
  border-radius: 6px;
}

JavaScript
function abrirPortao() {
  const status = document.getElementById("statusPortao");
  status.textContent = "⏳ Abrindo portão...";
  
  setTimeout(() => {
    status.textContent = "✅ Portão aberto com sucesso!";
  }, 2000);
}

function enviarNotificacao() {
  const input = document.getElementById("inputNotificacao");
  const lista = document.getElementById("listaNotificacoes");

  if (input.value.trim() === "") {
    alert("Digite uma mensagem para enviar!");
    return;
  }

  const item = document.createElement("li");
  item.textContent = "📢 " + input.value;
  lista.appendChild(item);
  input.value = "";
}
  
