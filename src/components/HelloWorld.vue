<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{msg2}}</h2>


    <div class="bloc">
    <b-card title="Movies"
          img-src="https://picsum.photos/600/300/?image=25" img-alt="Image" img-top tag="movies" style="max-width: 20rem;" class="mb-2">
    <p class="card-text">
      Every movie you've wanted to see
    </p>
    <div slot="footer">
      <router-link :to="{ name: 'DetailList', params: { state: 'movies' }}">Go</router-link>
    </div>
  </b-card>

  <b-card title="Series"
          img-src="https://picsum.photos/600/300/?image=1002"
          img-alt="Image"
          img-top
          tag="series"
          style="max-width: 20rem;"
          class="mb-2">
    <p class="card-text">
      All of the series you want to watch, are watching or paused.
    </p>
    <div slot="footer">
      <router-link :to="{ name: 'DetailList', params: { state: 'series' }}">Go</router-link>
    </div>  
  </b-card>

  <b-card title="Gifts"
          img-src="https://picsum.photos/600/300/?image=938"
          img-alt="Image"
          img-top
          tag="gifts"
          style="max-width: 20rem;"
          class="mb-2">
    <p class="card-text">
      Gifts you think would be perfect for that special someone which you're enclined to forget
    </p>
    <div slot="footer">
      <router-link :to="{ name: 'DetailList', params: { state: 'gifts' }}">Go</router-link>
    </div>
    
  </b-card>

  <b-card title="Groceries"
          img-src="https://picsum.photos/600/300/?image=935"
          img-alt="Image"
          img-top
          tag="groceries"
          style="max-width: 20rem;"
          class="mb-2">
    <p class="card-text">
      What to shop and at what place.
    </p>
    <div slot="footer">
      <!-- <b-button href="#" variant="primary">Go somewhere</b-button> -->
      <router-link :to="{ name: 'DetailList', params: { state: 'groceries' }}">Go</router-link>
    </div>
  </b-card>
</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Listed',
      msg2: 'Accéder à votre liste'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.bloc{
  display: inline-flex;
  width: 80%;
  height: 100%;
}

</style>
