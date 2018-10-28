<template>
  <body>
    <div class="uitleg" align="center">
    <h5>Over het gebruik van deze pagina:</h5>
    <p> Aan de linkerzijde van het scherm kunt u de informatie over nieuwe films toevoegen. Voer voor een nieuwe film
      de titel in en een samenvatting. als de film op meerdere tijden speel kun je na het invoeren van elke tijd, volgende
      indrukken om nog een tijd toe te voegen. Dit geldt ook voor zaalnummers. als u alle informatie heeft ingevoerd kunt
      u op opslaan drukken om alle informatie te bewaren.<br><br> Aan de rechter zijde van het scherm kunt u een film
      kiezen uit alle bestaande films, en vervolgens informatie over deze film aanpassen of de hele film, en alle informatie
      hierover verwijderen. Kies een bestande tijd, die verschijnt nadat u een film kiest om deze te verwijderen als u op
      opslaan drukt. Voer een tijd in het tekstvak in om deze toe te voegen als u op opslaan drukt </p>
    </div>
    <div class="toevoegen">
      <div id="inTV">
        <h5>Film Toevoegen</h5>
        <label>Titel      </label><input type="text"><br><br>
        <label>Samenvatting </label><input type="text"><br><br>
        <label>Speel tijden </label><input type="text"><button>Volgende 1</button><br><br>
        <label>Zaal nummer  </label><input type="text"><button>Volgende 2</button><br><br>
        <br><button>Opslaan</button><br><br>
      </div>
    </div>
    <div class="wijzigen">
        <h5>Film wijzigen</h5>
        <select v-model="selected">
          <option disabled value="">selecteer een film</option>
          <option>A</option>
          <option>B</option>
          <option>C</option>
        </select><span>gekozen: {{ selected }}</span>
      <ul>
      <li v-for="user in users"> <input type="checkbox" class="toggle" v-model="user.gemaild">
        <span :class="{gemaild: user.gemaild}">
        {{user.name}}:{{user.email}}

        </span>
      </li>
      </ul>

      <br><br>
        <label>Tijd toevoegen </label><input type="text"><br><br>
        <button id="opslaan2">Opslaan</button><br><br>
        <button id="verwijder">geselecteerde film verwijderen</button><br><br>
       <!-- <button v-on:click="verwijderGebruiker(user)">x</button> -->
    </div>
  <br><br>

  </body>
</template>

<script>
    export default {
        name: "Beheer",
      data() {
        return {
          selected: ''
        }

      }
    }

</script>

<style scoped>
  .toevoegen{
    float: left;
  }
  .wijzigen{
    float: right;
  }
  #opslaan2{
    float: right;
  }
  #verwijder{
    float: right;
  }
  #inTV{
    float: left;
  }
  .gemaild{
    text-decoration: line-through;
  }


</style>
