<template>

  <div>
    <div class="container-liquid">

      <div class="row">
        <div class="container my-5">

          <div class="row justify-content-md-end ">
            <div class="col col-5">
              <div class="card">
                <h5 class="card-header qliq-card-header">
                    Sign in to your account
                </h5>
                <div class="card-body">

                  <!-- <button onclick="doLogin(this)" class="btn btn-primary" id="loginConfirm">Login with google</button> -->
                  <div class="g-signin2" data-onsuccess="onSignIn"></div>

                </div>
              </div>
            </div>
          </div>

        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
    }
  }
}

function onSignIn(googleUser) {
  var profile = googleUser.getBasicProfile();
  console.log('ID: ' + profile.getId()); // Do not send to your backend! Use an ID token instead.
  console.log('Name: ' + profile.getName());
  console.log('Image URL: ' + profile.getImageUrl());
  console.log('Email: ' + profile.getEmail()); // This is null if the 'email' scope is not present.
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
