<template>
<div class="container">
        <div class="row">
          <div class="col">

                <form>
                    <div class="form-group">
                        <label for="exampleInputEmail1">Email address</label>
                        <input v-model="user.email" type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
                        <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
                    </div>
                    <div class="form-group">
                        <label for="exampleInputPassword1">Password</label>
                        <input v-model.lazy="user.password" type="password" class="form-control" id="exampleInputPassword1">
                    </div>
                    <div class="form-group form-check">
                        <input type="checkbox" class="form-check-input" id="exampleCheck1">
                        <label class="form-check-label" for="exampleCheck1">Check me out</label>
                    </div>
                    <button type="submit" class="btn btn-primary">Submit</button>
                </form>

          </div>
          <div class="col">
              EMAIL -> {{ user.email }}
              <hr/>
              Password -> {{ user.password }}
          </div>
        </div>
      </div>

</template>

<script>
export default {
    name: 'Form',
    data(){
        return {
            'user': {
                'email': '',
                'password': ''
            }
        }
    }
}
</script>


<style scoped> /*scoped serve solo localmente lo stile e non lo applica a tutta la pagina*/

</style>