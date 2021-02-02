<template>
  <app-section id="about" :styleclass="styleclass">
    <div class="section-title-wrapper">
      <h1 class="section-title">About</h1>
      <div class="title-underline"></div>
    </div>
    <div class="about-top-section">

        <div class="headshot-container">
        <img src="https://i.imgur.com/io5PKEg.jpg?1" title="headshot" />
        </div>

      <div class="about-content-container"> 
        <div class="about-content">Howdy! My name's Kristen Burgess, and I'm a fourth generation cowgirl/rancher and first generation software engineer. I live and work on my family's cattle ranches in the Sandhills of Nebraska. 
        </div>
        <!-- <div class="about-content"> I am entrepreneurial, self-motivated, a quick learner, highly personable, and an exceptional communicator. I work well both independently and collaboratively. I thrive on challenges and am constantly striving to improve and grow.
        </div> -->
        <br>
        <div class="about-content"> Professionally, I am most passionate about bringing creative tech solutions to underserved markets- particularly the agricultural industry.
        </div>
        <br> 
        <div class="about-content"> Personally, I am most passionate about world travel, live music, a good [grass-fed Angus] steak, buttery pastries, speedy horses, and a well crafted Old Fashioned. 
        </div>
      </div>
    </div>
    <br>
    <div class="about-icon-container">
      <div class="icon-content">
        <svg class="about-icon" version="1.1" xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80">
          <title>School</title>
          <path d="M40 10l36.719 20v26.719h-6.719v-23.125l-30 16.406-36.719-20zM16.719 43.906l23.281 12.813 23.281-12.813v13.438l-23.281 12.656-23.281-12.656v-13.438z"></path>
        </svg>

        <div>I attended a small liberal arts college where I obtained degrees in Political Science and English. My study abroad experiences in Germany and Africa were the most impactful parts of my undergraduate education. My deep interest in software engineering came from one of my first jobs after college, which led me to Turing School of Software and Design.  </div>
      </div>
      <div class="icon-content">
        <svg class="about-icon" version="1.1" xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80">
          <title>Work</title>
          <path d="M46.719 20v-6.719h-13.438v6.719h13.438zM66.719 20c3.75 0 6.563 2.969 6.563 6.719v36.563c0 3.75-2.813 6.719-6.563 6.719h-53.438c-3.75 0-6.563-2.969-6.563-6.719v-36.563c0-3.75 2.813-6.719 6.563-6.719h13.438v-6.719c0-3.75 2.813-6.563 6.563-6.563h13.438c3.75 0 6.563 2.813 6.563 6.563v6.719h13.438z"></path>
        </svg>

        <div> Prior to working in the tech industry, I was a paralegal. In tech, I have worked for a number of startups and have filled a wide variety of roles- sales, marketing, product management, project management, development, tech lead. I have a very diverse set of skills, and I pride myself on my ability to wear many hats. 
        <br>
        <a id="resume-link" href="https://resume.creddle.io/resume/e2ocwahn9w" target="_blank"> <h3> Résumé </h3> </a>
        </div>
      </div>
      <div class="icon-content">
        <svg class="about-icon" version="1.1" xmlns="http://www.w3.org/2000/svg" width="80" height="80" viewBox="0 0 80 80">
          <title>Code</title>
          <path d="M48.594 55.313l15.469-15.313-15.469-15.313 4.688-4.688 20 20-20 20zM31.406 55.313l-4.688 4.688-20-20 20-20 4.688 4.688-15.469 15.313z"></path>
        </svg>
   
        <div>I strive to create code that is readable, testable, maintainable, and accessible. I try to always be considerate of other developers- and my future self- who will have to work with my code. While primary focus is on all things front end, I enjoy exploring all areas of the stack. I am most fond of VueJS, but am perfectly comfortable with React and Angular. </div>
      </div>
    </div>
  </app-section>
</template>

<script>
import Section from './Section.vue';
export default {
  name: 'Timeline',
  components: {
    'app-section': Section,
  },
  data () {
    return {
      styleclass: 'timeline-tile'
    }
  }
}
</script>

<style lang="css">

.about-content {
  width: 90%;
  text-align: left;
  margin: auto 10px;
}

.about-top-section {
  display: flex;
  justify-content: space-around;
  width: 90%;
  /* background: white; */
  color: white;
  background: #2a0845;  /* fallback for old browsers */
  background: -webkit-linear-gradient(140deg, #2a0845, #a044ff); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(140deg, #2a0845, #a044ff);
  padding: 20px;
  border-radius: 0.5rem;
}

.headshot-container {
  margin: auto 10px;
}

img {
  width: 200px;
  /* border-radius: 0.5rem; */
}


h3 {
  color:#a044ff;
  border-radius: 0.5rem;
}

h3:hover {
  color: white;
  background-color: #a044ff;
  cursor: pointer;
}

.cool {
  height: 100rem;
}
.timeline-tile {
  text-align: center;
  line-height: 1.5;
}

.text-break {
  display: none;
}

.about-icon-container {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  margin: 2rem 0;
  max-width: 80vw;
  width: 100%;
}

.icon-content {
  align-items: center;
  display: flex;
  flex: 1;
  flex-direction: column;
  margin: 2rem 0;
  text-align: center;
}

.icon-content:first-child {
  margin-top: 0;
}

.icon-content:last-child {
  margin-bottom: 0;
}

.about-icon {
  height: 5rem;
  fill: #a044ff;
  width: 5rem;
}

@media (max-width: 650px) {
  .headshot-container {
    margin: 10px auto;  
  }
  
  .about-top-section {
    display: flex;
    flex-direction: column;
  }

  .about-content {
    margin: 10px auto;
    text-align: center;
  }
}

@media screen and (min-width: 48rem) {
  .text-break {
    display: initial;
  }
  .about-icon-container {
    margin: 4rem 0 1rem;
    flex-direction: row;
  }

  .icon-content {
    margin: 0 2rem;
  }

  .icon-content:first-child {
    margin-left: 0;
  }

  .icon-content:last-child {
    margin-right: 0;
  }
}

</style>
