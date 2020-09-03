<template>
  <div class="resume-block" id="resume">
    <h1 class="resume-block__title">Resume</h1>
    <p class="resume-block__p1">My Formal Resume</p>
    <div class="resume-block__line-decor">
      <hr class="resume-block__line-decor__normal" />
      <hr class="resume-block__line-decor__bold" />
    </div>
    <div class="resume-block__content">
      <div class="resume-block__content__left">
        <div class="resume-block__content__left__icons">
          <span v-for="(icon, i) in icons" :key="i" class="material-icons resume-block__content__left__icons__icon">{{icon}}</span>
        </div>
        <div class="resume-block__content__left__content">
          <div class="resume-block__content__left__content__block" v-for="(val, i) in resumeData" :key="i">
            <span class="resume-block__content__left__content__block__cirkle">s5</span>
            <span class="resume-block__content__left__content__block__text">{{val}}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icons: ["school", "history", "computer", "palette", "insights"],
      resumeData: [ 'Educations', 'Work History', 'Programming Skills', 'Designer Skills', 'SEO Skills']
    };
  },
};
</script>