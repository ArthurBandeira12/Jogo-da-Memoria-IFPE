<script>
    /*variavel dos botões*/
     let themes = ["Default", "Harry Potter", "Super heroes"];
     import"./pageplay.css"
    </script>
  

  
  <main>
    <div class="container">
      <div class="title">
        <span>MEMORY <br>MATCH</span>
        
        <img src="/brain.png" alt="Brain Icon" />
      </div>
      <p class="subtitle">Select a theme:</p>
      <div class="button-container">
          <!-- Itera sobre o array 'themes' e cria um botão para cada tema. 
           O valor atual de cada iteração é representado pela variável 'theme'. -->
          {#each themes as theme}
          <button class="button">{theme}</button>
        {/each}
      </div>
    </div>
    <div id="help-container">
        <button class="icon-button" aria-label="Ajuda">
            <i class="fa-regular fa-circle-question fa-3x" style="color:#ffffff;"></i>
        </button>
    </div>
  </main>
  