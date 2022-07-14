<template>
  <div>
    <video-pop-up />
    <drawer @toggleSidebar="toggleSidebar" :sidebar="sidebar" />
    <header-one image="logo-2.png" @toggleSidebar="toggleSidebar" />
    <single-play-post />
    <video-news />
    <trending-news />
    <features />
    <post-gallery class="pt-50" />
    <home-one-post-area class="pt-5" />
    <footer-one />
    <back-to-top />
  </div>
</template>

<script>
import Drawer from "../../Mobile/Drawer.vue";
import VideoPopUp from "../../Utility/VideoPopUp.vue";
import HeaderOne from "../../Utility/Header/index";
import BackToTop from "../../Helpers/BackToTop.vue";
import SinglePlayPost from "../SinglePlayPost.vue";
import VideoNews from "../VideoNews.vue";
import TrendingNews from "../TrendingNews.vue";
import Features from "../Features.vue";
import PostGallery from "../PostGallery.vue";
import HomeOnePostArea from "../../_Containers/HomeOnePostArea.vue";
import FooterOne from "../../Utility/Footer/FooterOne.vue";
export default {
  components: {
    VideoPopUp,
    Drawer,
    HeaderOne,
    BackToTop,
    SinglePlayPost,
    VideoNews,
    TrendingNews,
    Features,
    PostGallery,
    HomeOnePostArea,
    FooterOne,
  },
  data: () => ({
    sidebar: false,
  }),
  methods: {
    toggleSidebar() {
      this.sidebar = !this.sidebar;
    },
  },
};
</script>

<style>
/* play post */
.single-play-post-area .single-play-box {
  padding: 23px 12px !important;
}
</style>