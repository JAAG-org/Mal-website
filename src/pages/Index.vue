<template>
  <Layout>
    <h1 class="brand-name">MAL</h1>
    <div class="text-content">
      <p class="content">Mal [is] a tattoo shop and artist studio</p>
    </div>
    <div class="images">
      <g-image
        width="400"
        height="400"
        fit="cover"
        src="~/images/pic1.jpeg"
        class="image1"
      />
      <g-image class="image2" width="400" height="400" fit="cover" src="~/images/pic2.jpeg" />
      <g-image class="image3" width="400" height="400" fit="cover" src="~/images/pic3.jpeg" />
      <g-image class="image4" width="400" height="400" fit="cover" src="~/images/pic4.jpeg" />
      <g-image class="image5" width="400" height="400" fit="cover" src="~/images/pic5.jpeg" />
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Mal'
  },
  data: function() {
    return {
      imageQuality: '5',
      images: [
        'pic1.jpeg',
        'pic2.jpeg',
        'pic3.jpeg',
        'pic4.jpeg',
        'pic5.jpeg'
      ]
    }
  },
  methods: {
    onMouseHover: function() {
      console.log('works!')
      this.imageQuality = '5'
    },
    onMouseLeave: function() {
      this.imageQuality = '100'
    }
  },
}
</script>

<style scoped>
.home-links a {
  margin-right: 1rem;
}

.brand-name {
  font-size: 10rem;
  letter-spacing: 5px;
  margin-left: -10px;
  margin-top: 10px;
  position: absolute;
  z-index: 900;
  font-weight: 800;
  color: #ffffff;
  text-shadow: 0 0 5px #ffffff
    , 0 0 10px #ffffff
    , 0 0 15px #ffffff
    , 0 0 20px #ff0000
    , 0 0 30px #ff1e1e
    , 0 0 40px #ff1e1e
    , 0 0 55px rgb(255, 37, 37)
    , 0 0 75px rgb(255, 22, 22);
}

ul {
  list-style-type: none;
}

.text-content {
  position: absolute;
  top: 130px;
  left: calc(50% - 200px);
  text-align: center;
}

.content {
  font-size: 30px;
  padding: 10px;
  color: rgb(17, 0, 255);
  margin-top: 250px;
  position: absolute;
  width: 550px;
  z-index: 1000;
  font-family: 'Comic Sans MS';
}
.content:hover {
  font-style: italic;
  text-decoration: underline;
}

.images {
  position: relative;
}
.image1 {
  position: absolute;
  top: 0px;
  left: 10px;
}
.image2 {
  position: absolute;
  top: 100px;
  right: 100px;
}
.image3 {
  position: absolute;
  top: 400px;
  right: 300px;
}
.image4 {
  position: absolute;
  top: 500px;
  left: 20px;
}
.image5 {
  position: absolute;
  top: 800px;
  left: 100px;
}
</style>
