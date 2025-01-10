<script>
    /*variavel dos botões*/
     let themes = ["Default", "Harry Potter", "Super heroes"];
    </script>
  
<style src="./pageplay.css"></style>
  
  <main>
    <div class="container">
      <div class="title">
        <span>MEMORY MATCH</span>
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
  </main>
  