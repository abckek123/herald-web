<template lang='pug'>
  .tab
    dashboard(v-if='user' :user='user')
    login(v-else)
    .todo(v-if='user')
      toutiao
      exam(v-if='/^21/.test(user.cardnum)')
      curriculum
      experiment(v-if='/^21/.test(user.cardnum)')
</template>

<script>
  import exam from '@/components/Exam.vue'
  import login from '@/components/Login.vue'
  import dashboard from '@/components/Dashboard.vue'
  import curriculum from '@/components/Curriculum.vue'
  import experiment from '@/components/Experiment.vue'
  import toutiao from '@/components/TouTiao.vue'
  import api from '@/api'

  export default {
    props: ['user'],
    components: {
      login, dashboard, curriculum, experiment, exam, toutiao
    }
  }
</script>