<template>
  <q-page class="row">

    <!-- LEFT SIDE -->
    <div class="col-12 col-md-6 flex flex-center q-pa-xl">

      <div style="width: 100%; max-width: 400px;">

        <div class="text-h3 text-weight-bold q-mb-sm">
          Welcome back
        </div>

        <div class="text-grey-7 q-mb-xl">
          Please enter your details
        </div>

        <q-input
          v-model="email"
          outlined
          label="Email address"
          class="q-mb-md"
        />

        <q-input
          v-model="password"
          outlined
          type="password"
          label="Password"
          class="q-mb-md"
        />

        <div class="row items-center justify-between q-mb-lg">

          <q-checkbox
            v-model="rememberMe"
            label="Remember for 30 days"
          />

          <a href="#" class="text-purple">
            Forgot password?
          </a>

        </div>

        <q-btn
          label="Sign in"
          color="deep-purple"
          unelevated
          no-caps
          class="full-width q-py-sm q-mb-md"
          @click="login"
        />

        <q-btn
          outline
          no-caps
          class="full-width q-py-sm"
          @click="googleLogin"
        >
          <img
            src="https://www.svgrepo.com/show/475656/google-color.svg"
            width="22"
            class="q-mr-sm"
          >

          Sign in with Google
        </q-btn>

        <div class="text-center q-mt-lg text-grey-7">
          Don't have an account?
          <a href="#" class="text-purple">
            Sign up
          </a>
        </div>

      </div>

    </div>


    <!-- RIGHT SIDE -->
    <div
      class="col-md-6 gt-sm flex flex-center bg-deep-purple-2 q-pa-xl"
    >

      <img
        src="/login-illustration.jpg"
        style="width: 85%; max-width: 550px;"
      >

    </div>

  </q-page>
</template>


<script>
export default {
  name: 'IndexPage',

  data () {
    return {
      email: '',
      password: '',
      rememberMe: false
    }
  },

  methods: {
    login () {
      console.log(this.email)
      console.log(this.password)
    },

    googleLogin () {
      console.log('Google login')
    }
  }
}
</script>