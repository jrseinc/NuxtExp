<template>
  <div class="artist-container">
    <template v-for="artist in artists">
      <Card :artist="artist" :key="artist.name"></Card>
    </template>
  </div>
</template>

<script>
import Card from "~/components/card";

export default {
  components: {
    Card
  },
  data() {
    return {
      artists: [
        {
          id: 1,
          name: "Michael Jackson",
          img:
            "https://www.desktopbackground.org/download/3840x2400/2011/06/13/218287_michael-jackson-wallpapers-hd-images_4297x2974_h.jpg",
          handle: "@michaelJackson",
          bio:
            "Michael Joseph Jackson was an American singer, songwriter, and dancer. Dubbed the 'King of Pop', he is regarded as one of the most significant cultural figures of the 20th century."
        },
        {
          id: 2,
          name: "Adele",
          img:
            "https://wallsdesk.com/wp-content/uploads/2016/02/Adele-Wallpapers-HD.jpg",
          handle: "@adele",
          bio:
            "Adele Laurie Blue Adkins MBE, is an English singer-songwriter. After graduating from the BRIT School in 2006, Adele signed a recording contract with XL Recordings. In 2007, she received the Brit Awards  "
        },
        {
          id: 3,
          name: "Queen",
          img:
            "https://c4.wallpaperflare.com/wallpaper/485/318/506/rock-music-queen-freddie-mercury-wallpaper-preview.jpg",
          handle: "queen",
          bio:
            "Queen are a British rock band formed in London in 1970. Their classic line-up was Freddie Mercury, Brian May, Roger Taylor and John Deacon."
        }
      ]
    };
  },

  head() {
    return {
      title: "Artists",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Artists Discription"
        }
      ]
    };
  }
};
</script>

<style scoped>
.artist-container {
  padding-top: 100px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
