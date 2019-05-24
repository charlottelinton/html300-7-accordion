<template>
  <div id="app">
    <!-- Bootstrap responsive navbar - collapses to hamburger menu -->
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="index.html">Make It Sewstainable</a>
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
        <div class="navbar-nav">
          <a class="nav-item nav-link" href="index.html">Home</a>
          <a class="nav-item nav-link" href="gallery.html">Gallery</a>
          <a class="nav-item nav-link" href="#">Blog</a>
          <a class="nav-item nav-link" href="faq.html">FAQ</a>
        </div>
      </div>
    </nav>
    <!-- Bootstrap accordion to hide and display FAQs -->
    <div class="accordion" id="accordionExample">
      <div v-for="faq in faqs" class="card">
        <div class="card-header" id="headingOne">
          <h2 class="mb-0">
            <button class="btn btn-link" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
              {{ faq.title }}
            </button>
          </h2>
        </div>
        <div id="collapseOne" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionExample">
          <div class="card-body">
            {{ faq.text }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      faqs: [
        {title: 'What is sustainable sewing?', text: 'Stuff about sustainable sewing'},
        {title: 'How can I support sustainable craft businesses?', text: 'Stuff about sustainable craft businesses'},
        {title: 'What resources are there to help me on my sustainable crafting mission?', text: 'I am on a mission'}
      ]
    }
  }
}
</script>

<style lang="scss">
#app {

}

* {
  box-sizing: border-box;
}

body, html {
  height: 100%;
  max-width: 100%;
  overflow-x: hidden;
  margin: 0;
}

.card-header {
  background-color: white;
}
</style>
