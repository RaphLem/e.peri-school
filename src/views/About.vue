<template>
  <div id="about">
    <div id="about-heading">
      <img class="background-home" src="@/assets/img/picture/E-Perischool10Nov20TIML0150.jpg"
           alt="">
      <div id="black-filter"></div>
      <h1>A propos de nous</h1>
      <h2>E.péri&school programme d'apprentissage du numérique pour les enfants</h2>
    </div>

    <div id="programme">
    <h2>Le programme pédagogique</h2>
      <p class="description">Les 10 séances s’articulent autour de deux axes d’apprentissage : la programmation et l’impression 3D.</p>
      <p class="description">Ces deux thématiques sont réparties selon le planning suivant :</p>

      <div class="container">
      <div>
        <h3>1. Présentation du programme & découverte des différents composants</h3>
        <p>Découvrir les différents composants du kit de programmation : le compteur, la led et le potentiomètre. Réalisation des premiers assemblages simples (sans programmation).</p>

        <h3>2. Programmation : découverte du
          composant de programmation</h3>
        <p>Découvrir le composant « programmation » et la plateforme (logiciel)LittleBits Code Bit qui permet de programmer les différents composants. Réaliser des programmes simples : programmer une puissance électrique en sortie, un capteur de lumière et un bouton buzzer.</p>

        <h3>3. Programmation : découverte du
          composant « moteur »</h3>
        <p>Découvrir le fonctionnement du composant « moteur ». Commencer à programmer le moteur en avant et en arrière. Réaliser un assemblage de composants plus complexes avec le potentiomètre, l’afficheur numérique, l’alarme et le détecteur de lumière (ex : si la lumière est inférieur à 50, l’alarme se déclenche).</p>
        <img src="../assets/img/picture/E-Perischool10Nov20TIML0214.jpg" alt="intervenant expliquant aux élèves comment faire"/>

        <h3>4. Conception 3D</h3>
        <p>Découvrir l’outil de modélisation Tinkercad. Concevoir des formes géométriques simples pour découvrir les différentes fonctionnalités de la plateforme.</p>

        <h3>5. Conception 3D</h3>
        <p>Concevoir de formes plus complexes à partir de formes simples. Maitriser davantage l’outil de modélisation.</p>
        <img src="../assets/img/picture/E-Perischool10Nov20TIML0232.jpg" alt="élèves travaillant sur l'ordinateur"/>
      </div>
      <div>

        <h3>6. Impression 3D</h3>
        <p>Créer et modéliser une forme encore plus complexe : créer un pot à crayons personnalisée avec perçage.</p>

        <h3>7. Impression 3D</h3>
        <p>Découvrir le fonctionnement d’une imprimante 3D. Découvrir la plateforme XYZmaker qui permet d’imprimer les éléments modélisés en amont.</p>
        <img src="../assets/img/picture/E-Perischool10Nov20TIML0352.jpg" alt="élèves contemplant l'impression 3D"/>

        <h3>8. Programmation : assemblage de
          composants avec boucles et conditions</h3>
        <p>Monter l’Autobot et programmer les moteurs par le biais de boucles et de conditions pour qu’il se déplace en avant, en arrière, et effectue des virages.</p>

        <h3>9. Programmation : assemblage de
          composants avec boucles et conditions</h3>
        <p>Programmer des parcours de l’Autobot (en O, en U et en 8).</p>
        <img src="../assets/img/picture/E-Perischool10Nov20TIML0227.jpg" alt="deux élèves parlant entre eux de leurs idées"/>
        <h3>10. Assemblage final du projet</h3>
        <p>Programmer des parcours complexes de l’autobot (ex : détection d’obstacles)</p>
      </div>
      </div>

    </div>


    <div id="acteurs">
      <h2>Les acteurs</h2>
      <p class="description">Un projet réalisé par</p>
      <div class="container">

        <div>
          <img src="../assets/img/img-acteurs/Pavillion_des_sciences.jpg" alt="photo du pavillon des sciences"/>
          <div><h3>Le pavillon des sciences</h3>
          <ul>
            <li>Formation</li>
            <li>Gestion des impressions 3D</li>
            <li>Promotion de l'action</li>
          </ul></div>
        </div>

        <div>

          <img src="../assets/img/img-acteurs/Semnumerica.jpg" alt="photo du batiment de numérica SEM"/>
          <div><h3>Numérica SEM</h3>
          <ul>
            <li>Maitrise d'ouvrage</li>
            <li>Ingénierie pédagogique</li>
            <li>Conception de l'application</li>
            <li>Formation</li>
          </ul></div>
        </div>

        <div>
          <img src="../assets/img/img-acteurs/francas_du_doubs.jpg" alt="photo de l'association Les Francas du Doubs"/>
          <div><h3>Les Francas su Doubs</h3>
          <ul>
            <li>Animation</li>
          </ul></div>
        </div>

      </div>
    </div>


    <div id="soutiens">
      <h2>Nos soutiens</h2>
      <p class="description">Sous la maitrise d'ouvrage et avec le soutien de</p>
      <div class="container">
      <img src="../assets/img/img-partenaires/grand-belfort.jpg" alt="logo grand belfort" />
      <img src="../assets/img/img-partenaires/Pays_de_Montbeliard.png" alt="Logo pays de montbéliard" />
      </div>
      <p class="description">Avec le soutien de</p>
      <div class="container">
      <img src="../assets/img/img-partenaires/banque_des_territoires.png" alt="Logo Banque des territoires" />
      <img src="../assets/img/img-partenaires/territoire.jpg" alt="Logo territoires d'innovation" />
      <img src="../assets/img/img-partenaires/Bourgogne-Franche-Comte_2016.svg.png" alt="Logo région bourgogne franche comté" />
    </div>
    </div>
  </div>

  <footer>
    <img id="logo-footer" src="@/assets/img/logos/Global-blanc.svg" alt="">
    <div id="left-block">
      <ul>
        <li>
          <router-link class="lien" to="/news">Actualités</router-link>
        </li>
        <li>
          <router-link class="lien" to="/about">À propos</router-link>
        </li>
      </ul>
    </div>
    <div id="right-block">
      <ul>
        <li>
          <router-link class="lien" to="/mentions">Mentions légales</router-link>
        </li>
        <li>
          <p class="lien">Nous Contacter</p>
        </li>
      </ul>
    </div>
  </footer>
</template>
<script>
export default {
  name: 'About',
}
</script>
