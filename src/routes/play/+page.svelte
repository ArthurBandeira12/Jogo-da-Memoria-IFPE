<script>
  /* Importa o estilo */
  import "./pageplay.css";
  
  // Função para voltar à página anterior
  function handleBack() {
    window.history.back();
  }

  // Lista de temas e suas rotas
  const themes = [
    { name: "Default", route: "/defaultgame" },
     { name: "Harry Potter", route: "/harrypottergame" },
      { name: "Super Heroes", route: "/superheroesgame" }, ];

  // Função para escolher um tema aleatório
  function handleRandomTheme() {
    const randomIndex = Math.floor(Math.random() * themes.length); // Seleciona índice aleatório
    const randomTheme = themes[randomIndex]; // Obtém o tema correspondente

    // Redireciona para a página do tema escolhido
    window.location.href = randomTheme.route;
  }
</script>

<main>
  <div class="container">
    <!-- Título e Ícone -->
    <div class="header">
      <div class="title">
        <span>MEMORY <br />MATCH</span>
        <img src="/brain.png" alt="Brain Icon" />
      </div>
    </div>

    <!-- Texto: "Select a theme" -->
    <p class="subtitle">Select a theme:</p>

    <!-- Exibe as cartas temáticas -->
    <!-- svelte-ignore a11y_click_events_have_key_events -->
    <div class="card-container">
      <div class="card-wrapper">
        <a href="/memorygame" class="card">
          <img src="/Img-teste-2.png" alt="Default Theme" class="card-image" />
        </a>
        <span class="card-name">Default</span>
      </div>
      
      <div class="card-wrapper">
        <a href="/memorygame" class="card">
          <img src="/HarryPotterIcon.jpeg" alt="Harry Potter Theme" class="card-image" />
        </a>
        <span class="card-name">Harry Potter</span>
      </div>
      
      <div class="card-wrapper">
        <a href="/memorygame" class="card">
          <img src="/Img-teste-0.png" alt="Super Heroes Theme" class="card-image" />
           </a>
        <span class="card-name">Super Heroes</span>
      </div>
     
      <!-- Botão aleatório -->
      <!-- svelte-ignore a11y_click_events_have_key_events -->
      <!-- svelte-ignore a11y_no_static_element_interactions -->
      <div class="card-wrapper random" on:click={handleRandomTheme}>
       <!-- svelte-ignore a11y_missing_attribute -->
       <a class="card">
        <img src="/Img-teste-1.png" alt="Random Theme" class="card-image" />
         </a>
        <span class="card-name">Random Theme</span>
       </div>
     </div>
    
       <!-- Botão voltar -->
     <div id="back-container">
      <button on:click={handleBack} class="back-button">← </button>
    </div>
     
     <!-- Botão help -->
     <div id="help-container">
      <button class="icon-button" aria-label="Ajuda">
       <i class="fa-regular fa-circle-question fa-3x" style="color: #ffffff;"></i>
      </button>
    </div>
</main>
