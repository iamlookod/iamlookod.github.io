<template>
  <div class="home">
    <app-banner></app-banner>
    <v-container>
      <v-layout wrap >
        <v-flex xs12 id="about">
          <div class="display-1 font-weight-bold" id="about">About me</div>
        </v-flex>
        <v-flex xs12 mt-5>
          <div class="body-1">{{ aboutMe }}</div>
        </v-flex>
      </v-layout>
      
      <v-layout wrap my-16>
        <v-flex xs12 id="skill">
          <div class="display-1 font-weight-bold" id="portfolio">Language Skills</div>
        </v-flex>
        <v-flex xs12 class="mt-5">
          <v-layout wrap>
            <template v-for="(languageSkill, i) in languageSkills">
              <v-flex :key="i" xs12 sm6 md4>
                <app-skill-card :data="languageSkill" />
              </v-flex>
            </template>
          </v-layout>
        </v-flex>
      </v-layout>

    </v-container>
  </div>
</template>

<script>
import AppBanner from "@/components/AppBanner.vue";
import AppSkillCard from '../components/AppSkillCard.vue';

export default {
  components: { AppBanner, AppSkillCard },
  data: () => ({
    aboutMe:
      "I love coding and develop web and apps. I enjoy learning and Try new technology for develope software in my free time. I just curious to see how things work. I quick learnning when i love it. Love to encourage my friend that they can do it too !",
    languageSkills: [
      { name: 'Javacsript', logo: 'javascript.png' },
      { name: 'Typescript', logo: 'typescript.png' },
      { name: 'Node Js', logo: 'nodejs.png' },
      { name: 'PHP', logo: 'php.png' },
      { name: 'Python', logo: 'python.png' },
      { name: 'Go', logo: 'go.png' },
      { name: 'Dart', logo: 'dart.png' },
      { name: 'Html5', logo: 'html.png' },
      { name: 'Css3', logo: 'css.png' },
      { name: 'Sass', logo: 'sass.png' },
      { name: 'Less', logo: 'less.png' },
      { name: 'Json', logo: 'json.png' },
      { name: 'Yaml', logo: 'yml.png' },
      { name: 'Xml', logo: 'xml.png' },
    ]
  }),
};
</script>
