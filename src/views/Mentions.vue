<template>
  <div id="mentions">
    <div id="mentions-heading">
      <img class="background-home" src="@/assets/img/picture/E-Perischool10Nov20TIML0150.jpg"
           alt="">
      <div id="black-filter"></div>
      <h1>Mentions légales</h1>
    </div>
    <p>Cette page décrit les mentions légales qui s'appliquent à tout internaute visitant ce site. En le consultant vous
      vous engagez sans réserve à les respecter. Les mentions légales pouvant être modifiées à tout moment et sans
      préavis, nous vous engageons à les consulter régulièrement.</p>
    <h1>Responsable éditorial et responsable légal</h1>
    <p>SEM Numerica
      Représenté(e) par : SEM Numerica
      Adresse : Cours Louis Leprince Ringuet 25200 Montbéliard
      Tél. : +33 0381312680
      E-mail : contact@numericabfc.com
      Siret / N°TVA : 50327982000016 R.C.S. : Montbéliard
    </p>
    <h1>Éditeur du site</h1>
    <p>Département des Métiers du Multimédia & de l'Internet (Montbéliard)
      Représenté(e) par les étudiants : Julien Ferre, Floran Marchal, Raphaël Lemoine
      Adresse du centre de formation : 4 Place Tharradin, 25200 Montbéliard
      E-mail : E-peri-school@gmail.com
      Tuteur légal des étudiants : Jean-Marie Fino, Camille Bataille-Barbier
    </p>
    <h1>Hébergeur</h1>
    <p>SEM Numerica
      Représenté(e) par : SEM Numerica
      Adresse : Cours Louis Leprince Ringuet 25200 Montbéliard
      E-mail : contact@numericabfc.com
      Siret / N°TVA : 50327982000016 R.C.S. : Montbéliard
    </p>
    <h1>Conditions d'utilisation</h1>
    <p>Conformément à la loi Informatique et Libertés du 6 janvier 1978, vous disposez d'un droit d'accès et de
      rectification aux données vous concernant par simple demande mail, écrite ou téléphonique. Le centre de formation
      (DUT MMI montbéliard) et les étudiants en charge du projet (Floran Marchal, Julien Ferre et Raphaël Lemoine) ne
      peuvent être tenus responsable du contenu du site. Ce site est exploité par E-peri&school. La présentation et
      chacun des éléments, y compris les marques, logos et noms de domaine, apparaissant sur le site
      https://e-peri-school.raph-lem.com/ sont protégés par les lois en vigueur sur la propriété intellectuelle, et
      appartiennent à E-peri&school, ou font l'objet d'une autorisation d'utilisation. Aucun élément composant le site
      ne peut être copié, reproduit, modifié, réédité, chargé, dénaturé, transmis ou distribué de quelque manière que ce
      soit, sous quelque support que ce soit, de façon partielle ou intégrale, sans l'autorisation écrite et préalable
      de E-peri&school à l'exception d'une stricte utilisation pour les besoins de la presse et sous réserve du respect
      des droits de propriété intellectuelle et de tout autre droit de propriété dont il est fait mention. Seule la
      copie à usage privé est autorisée pour votre usage personnel, privé et non-commercial, sur votre ordinateur
      personnel. Toute utilisation autorisée des éléments composant ou figurant dans le site doit se faire sans
      dénaturation, modification ou altération de quelque manière que ce soit. E-peri&school se réserve le droit de
      poursuivre tout acte de contrefaçon de ses droits de propriété intellectuelle. Le présent Contrat est soumis au
      droit Français. Le présent Contrat s'applique dans le monde entier, et seule sa version en langue française fait
      foi en vue de son interprétation.</p>
    <h1>Graphisme,photos et illustrations</h1>
    <p>Le graphisme (incluant le webdesign et excluant le logo) a été réalisé par Floran Marchal.
      Les photographies ont été réalisé par Tim Platt. Les illustrations et visuels ont téléchargés sur les banques
      d’images libres de droits Freepik, Unsplash, Flaticon etc.
    </p>
    <h1>Déclaration à la CNIL</h1>
    <p>Conformément à la loi 78-17 du 6 janvier 1978 (modifiée par la loi 2004-801 du 6 août 2004 relative à la
      protection des personnes physiques à l’égard des traitements de données à caractère personnel) relative à
      l’informatique, aux fichiers et aux libertés, ce site n’a pas fait l’objet d’une déclaration auprès de la
      Commission nationale de l’informatique et des libertés (www.cnil.fr). Pour plus d’informations sur le traitement
      de nos données sensibles, veuillez consulter notre Politique de Confidentialité</p>
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
          <li v-b-modal.modal-prevent-closing>
            <p class="lien">Nous Contacter</p>
          </li>
        </ul>
      </div>
    </footer>
  </div>

</template>

<script>
export default {
  name: "Mentions"
}
</script>

<style scoped>

</style>