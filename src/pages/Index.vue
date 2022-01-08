<template>
  <Layout>
    <h1 class="brand-name noselect">MAL</h1>
    <div class="text-content">
      <p class="content-description noselect">Mal [is] a tattoo shop and artist studios</p>
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
    <footer class="footer">
      <p class="address">
        🏘 &nbsp;&nbsp;&nbsp; 29 Sukhumvit 31, Klongtoey-Nua, Watthana, Bangkok 10110
      </p>
      <a class="address" target="_blank" href="https://www.instagram.com/malstudiobkk/">
        📷 &nbsp;&nbsp;&nbsp; Mal Studio BKK
      </a>
    </footer>
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
  font-family: 'Gruppo';
  letter-spacing: 5px;
  margin-left: 10px;
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
.brand-name:hover {
  cursor: cell;
}

ul {
  list-style-type: none;
}

.content-description {
  font-size: 28px;
  padding: 10px;
  color: #ff1e1e;
  top: 300px;
  left: 500px;
  position: absolute;
  width: 550px;
  z-index: 1000;
  font-family: 'Gruppo';
}
.content-description:hover {
  font-style: italic;
  cursor: cell;
}

.text-content {
  position: relative;
}

.images {
  position: relative;
  width: 100%;
  height: 1300px;
}

.image1 {
  position: absolute;
  top: 0px;
  left: 30px;
  box-shadow: 5px 10px #c4c4c4;
}
.image2 {
  position: absolute;
  top: 100px;
  right: 100px;
  box-shadow: 5px 10px #c4c4c4;
}
.image3 {
  position: absolute;
  top: 400px;
  right: 300px;
  box-shadow: 5px 10px #c4c4c4;
}
.image4 {
  position: absolute;
  top: 500px;
  left: 70px;
  box-shadow: 5px 10px #c4c4c4;
}
.image5 {
  position: absolute;
  top: 800px;
  left: 300px;
  box-shadow: 5px 10px #c4c4c4;
}

.footer {
  padding-top: 20px;
  position: relative;
  width: 100%;
  height: 150px;
  left: 0;
  margin-bottom: 25px;
}
.address {
  color: rgb(0, 0, 0);
  margin-left: 30px;
  margin-top: 15px;
  margin-bottom: 10px;
  letter-spacing: 1px;
  font-family: 'Gruppo';
  font-weight: 800;
  font-size: 18px;
}
.spotify-playlist-container {
  position: relative;
  width: 100%;
  height: 400px;
  margin-top: -400px;
}
.spotify-playlist {
  position: absolute;
  right: 10%;
}
</style>
