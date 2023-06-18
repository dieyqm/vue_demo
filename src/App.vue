<template>
  <!-- <v-app>
    <app-navbar></app-navbar>
    <hr> -->

  <body class="grid-container">
    <nav class="navbar navbar-expand-lg bg-dark border-bottom border-bottom-dark" data-bs-theme="dark">
      <div class="container-fluid">
        <!-- <button class="navbar-toggler" type="button" data-toggle="collapse" data-bs-target="#navbarToggleExternalContent"
          aria-controls="navbarToggleExternalContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button> -->
        <!-- <a class="navbar-brand" href="#">Navbar</a> -->
        <button class="navbar-toggle" type="button" data-bs-toggle="collapse" data-bs-target="#navbarColor01"
          aria-controls="navbarColor01" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarColor01">
          <ul class="navbar-nav  mb-2 mb-lg-0">
            <li class="nav-item">
              <button class="hideresponse" type="button" data-bs-toggle="collapse" data-bs-target="#navbarColor01"
                aria-controls="navbarColor01" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
              </button>
            </li>
            <li class="nav-item">
              <v-img :src="require('../src/assets/logo.png')" class="my-3 hideresponse" contain height="200" />
            </li>
          </ul>
          <div class="mx-5">
            <form class="d-flex" role="search">
              <input class="form-control ml-5 pl-5" type="search" placeholder="Search here" aria-label="Search">
              <button class="btn btn-outline" type="submit">
                <i class=""></i>
              </button>
            </form>

          </div>
        </div>
      </div>
    </nav>
    <nav aria-label="breadcrumb" class="breadcrumbs">
      <ol class="breadcrumb">
        <li class="breadcrumb-item"><a href="#">Dashboard / </a></li>
        <li class="breadcrumb-item active" aria-current="page"></li>
      </ol>
    </nav>
    <article class="main">
      <div class="container">
        <div class="row">
          <div class="col-md-6 col-sm-12">
            <div class="row">
              <div class="col-12">
                <div class="card">
                  <div class="card-title">
                    <div class="row mx-2 my-3">
                      <div class="col-6">Best Selling</div>
                      <div class="col-6">menu</div>
                    </div>
                  </div>
                  <div class="card-body">
                  </div>
                  <img :src="require('../src/assets/chart1.png')" class="card-img-bottom" alt="...">
                </div>
              </div>
              <div class="col-12 col-md-6">
                <div class="card small">
                  <div class="card-title">
                    <div class="row mx-2 my-3">
                      <div class="col-6 h5">456k Pcs</div>
                      <div class="col-6">Ticket Sold</div>
                    </div>
                  </div>
                  <img :src="require('../src/assets/chart2.png')" class="card-img-bottom" alt="...">
                </div>
              </div>
              <div class="col-12 col-md-6">
                <div class="card small">
                  <div class="card-title">
                    <div class="row mx-2 my-3">
                      <div class="col-6">451,509</div>
                      <div class="col-6">Sales</div>
                    </div>
                  </div>
                  <img :src="require('../src/assets/chart3.png')" class="card-img-bottom" alt="...">
                </div>
              </div>
              <div class="col-12 col-md-6">
                <div class="card small">
                  <div class="card-title">
                    <div class="row mx-2 my-3">
                      <div class="col-6">$456,623</div>
                      <div class="col-6">Income</div>
                    </div>
                  </div>
                  <img :src="require('../src/assets/chart4.png')" class="card-img-bottom" alt="...">
                </div>
              </div>
              <div class="col-12 col-md-6">
                <div class="card small">
                  <img :src="require('../src/assets/chart5.png')" class="card-img-bottom" alt="...">
                </div>
              </div>
            </div>
          </div>
          <div class="col-12 col-md-6">
            <div class="row">
              <div class="col-12">
                <div class="card">
                  <img :src="require('../src/assets/chart6.png')" class="card-img-top" alt="...">
                </div>
              </div>
              <div class="col-12">
                <span class="title-gallerie">Event Galleries</span>
                <div class="swiper">
                  <!-- Additional required wrapper -->
                  <div class="swiper-wrapper">
                    <!-- Slides -->
                    <div class="swiper-slide"><img :src="require('../src/assets/chart1.png')" class="card-img-top"
                        alt="..."></div>
                    <div class="swiper-slide"><img :src="require('../src/assets/chart6.png')" class="card-img-top"
                        alt="..."></div>
                    <div class="swiper-slide"><img :src="require('../src/assets/chart4.png')" class="card-img-top"
                        alt="..."></div>
                    ...
                  </div>
                  <!-- If we need pagination -->
                  <div class="swiper-pagination"></div>

                  <!-- If we need navigation buttons -->
                  <div class="swiper-button-prev"></div>
                  <div class="swiper-button-next"></div>

                  <!-- If we need scrollbar -->
                  <div class="swiper-scrollbar"></div>
                </div>
              </div>
            </div>

          </div>
        </div>
      </div>
    </article>

  </body>
  <!-- </v-app> -->
</template>

<script>

/* import AppNavbar from '@/common/layout/AppNavbar';
import AppBreadcrum from '@/common/layout/BreadCrumb.vue'; */
//const Swiper = require('swiper')
import {Swiper} from "swiper"
export default {
  name: 'App',

  components: {
    //AppNavbar, AppBreadcrum
  },

  data: () => ({
    swiper: null
  }),
  created() {
    this.swiper = new Swiper('.swiper', {
      // Optional parameters
      direction: 'vertical',
      loop: true,

      // If we need pagination
      pagination: {
        el: '.swiper-pagination',
      },

      // Navigation arrows
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },

      // And if we need scrollbar
      scrollbar: {
        el: '.swiper-scrollbar',
      },
    });
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  height: 100%;
}

body {
  font-family: 'Public Sans', sans-serif;
  font-size: 1.2rem;
  min-height: 100%;
}

img {
  padding-top: 15px;
  padding-bottom: 15px;
  padding-left: 15px;
  padding-right: 15px;
}

.card {
  margin: 15px;
  border-radius: 12px;
  border-style: none;
  background-color: #272E35;
  color: white;
  text-align: left;
  /* height: 100vh;
  width: 100vh; */
}

.small {
  background-color: #2F363D;

}

.grid-container>* {
  box-shadow: -1px 1px 7px 0px rgba(0, 0, 0, 0.75);
  text-align: center;
}


.navbar {
  grid-area: navbar;
  background-color: #24292E;
}

a {
  color: rgb(12, 172, 172);
}

.breadcrumbs {
  grid-area: breadcrumbs;
  background-color: #2D3339;
  text-align: center;
  vertical-align: middle;
  color: rgb(8, 155, 155);
}

.main {
  grid-area: main;
  background-color: #252A2F;
}


.grid-container {
  display: grid;
  grid-template-areas:
    "navbar"
    "breadcrumbs"
    "main"
  ;
}

.hideresponse {
  display: block;
}

.title-gallerie {
  text-align: left;
  color: white;
  flex-flow: nowrap;
}

@media(min-width: 600px) {
  .grid-container {
    grid-template-columns: 200px auto;
    grid-template-rows: 100px 50px auto 100px;

    grid-template:
      "navbar navbar " 100px
      "breadcrumbs breadcrumbs " 50px
      "main main" auto
  }

  .hideresponse {
    display: none;
  }
}

@media(min-width: 900px) {
  .grid-container {
    grid-template:
      "navbar navbar" 100px
      "breadcrumbs breadcrumbs" 60px
      "main main" auto
  }

  .hideresponse {
    display: block;
  }
}</style>
