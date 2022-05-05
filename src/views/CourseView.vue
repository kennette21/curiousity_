<script>
  export default {
    data() {
      return {
        courseId: '',
        password: '',
        error: ''
      }
    },

    methods: {
      enter() {
        // check if id and pass work, othwerwise display an error
        switch (this.courseId) {
          case "abc":
            if (this.password === '123') {
              this.$router.push('/course/abc');
            } else {
              this.error = "Invalid Password";
            }
            break;
          default:
            this.error = "Unkown Course ID";
        }
      }
    }
  }
</script>

<template>
  <main class="flex justify-center flex-col gap-2">
    <div class="text-3xl font-bold self-center">Sign to course</div>
    <input class="border w-44 self-center rounded-md" v-model="courseId" placeholder="course id">
    <input class="border w-44 self-center rounded-md" v-model="password" type="password" placeholder="password">
    <button class="border w-44 self-center rounded-md bg-purple-200" @click="enter">Enter</button>
    <div class="text-2xl text-red-500 self-center" v-if="error !== ''">{{error}}</div>
  </main>
</template>