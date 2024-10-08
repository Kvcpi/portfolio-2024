<template>
  <main class="about-page">
    <section class="intro">
      <h1>À propos de moi</h1>
      <p>Passionné de web design</p>
    </section>

    <section class="about-content">
      <div class="about-text">
        <h2>Mon parcours</h2>
        <p>Je suis Kacper Szymanski, un étudiant en Web Design passionné par la création d'expériences numériques uniques et engageantes. Mon parcours dans le monde du design a commencé il y a 2 ans, et depuis, je n'ai cessé d'apprendre et de grandir dans ce domaine en constante évolution.</p>
        <p>Ma formation en Web Design m'a donné une base solide en design graphique et en programmation, que j'ai constamment enrichie par des projets personnels et des collaborations diverses.</p>
      </div>
      <div class="about-skills">
        <h2>Mes compétences</h2>
        <ul>
          <li>HTML5 / CSS3 / JavaScript</li>
          <li>Responsive Web Design</li>
          <li>UI/UX Design</li>
          <li>Adobe Creative Suite</li>
          <li>WordPress & WooCommerce</li>
          <li>SEO & Web Analytics</li>
        </ul>
      </div>
    </section>

    <section class="cta">
      <h2>Envie de travailler ensemble ?</h2>
      <RouterLink to="/contact" class="btn">Contactez-moi</RouterLink>
    </section>
  </main>
</template>

<style scoped>
.about-page {
  padding-top: 80px;
}

.about-content {
  display: flex;
  justify-content: space-between;
  padding: 80px 20px;
  background-color: var(--secondary-color);
}

.about-text, .about-skills {
  flex: 1;
  padding: 0 20px;
}

.about-text h2, .about-skills h2 {
  font-size: 2em;
  margin-bottom: 20px;
  color: var(--primary-color);
}

.about-skills ul {
  list-style-type: none;
  padding: 0;
}

.about-skills li {
  margin-bottom: 10px;
  padding: 10px;
  background-color: var(--background-color);
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.cta {
  text-align: center;
  padding: 60px 20px;
  background-color: var(--primary-color);
  color: var(--background-color);
}

.cta h2 {
  font-size: 2.5em;
  margin-bottom: 20px;
}

@media screen and (max-width: 768px) {
  .about-content {
    flex-direction: column;
  }

  .about-text, .about-skills {
    padding: 20px 0;
  }
}
</style>