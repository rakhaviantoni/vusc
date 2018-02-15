<template>
<div id="navbar">
  <!-- Top bar -->
  <div class="top-bar blue darken-4 visible-md visible-lg">
    <div class="container">
      <div class="row">
        <!-- Social Icon -->
        <div class="col-md-6">
          <!-- Social Icon -->
          <ul class="list-inline social-top tt-animate btt">
            <li><a href="https://twitter.com/pusc_presuniv"><i class="fa fa-twitter"></i></a></li>
            <li><a href="https://www.instagram.com/pusc_presuniv/"><i class="fa fa-instagram"></i></a></li>
            <li><a href="https://www.youtube.com/channel/UCNVSuH31ovsNPAgWlzegbNQ"><i class="fa fa-youtube"></i></a></li>
            <li>
              <div class="line-it-button" data-lang="en" data-type="friend" data-lineid="@uhk9253i" data-home="true" style="display: none;"></div>
            </li>
          </ul>
        </div>

        <div class="col-md-6 text-right">
          <ul class="topbar-cta no-margin">
            <li class="mr-20">
              <a><i class="material-icons mr-10">&#xE0B9;</i>pusc@president.ac.id</a>
            </li>
          </ul>
        </div>
      </div>
      <!-- /.row -->
    </div>
    <!-- /.container -->
  </div>
  <!-- /.top-bar -->

  <!--header start-->
  <header id="header" class="tt-nav nav-border-bottom">

    <div class="header-sticky light-header ">

      <div class="container">


        <div id="materialize-menu" class="menuzord">

          <!--logo start-->
          <a href="/" class="logo-brand">
            <img src="https://pusc.or.id/assets/img/pusc.png" alt="PUSC" title="PUSC" />
          </a>
          <!--logo end-->

          <ul class="menuzord-menu pull-right">

            <router-link :to="'/'" tag="li" exact><a>Home</a></router-link>

            <router-link :to="'/about'" tag="li"><a>About</a></router-link>

            <router-link :to="'/commissions'" tag="li"><a>Commissions</a></router-link>

            <!-- <router-link :to="'/programs'" tag="li"><a>Programs</a></router-link> -->

            <router-link :to="'/articles'" tag="li"><a>Articles</a></router-link>

            <router-link :to="'/downloads'" tag="li"><a>Downloads</a></router-link>

            <router-link :to="'/partners'" tag="li"><a>Student Organizations</a></router-link>

            <router-link :to="'/contact'" tag="li"><a>Contact</a></router-link>

          </ul>

        </div>
      </div>
    </div>

  </header>
  <!--header end-->
</div>
</template>

<script>
export default {
  name: 'navbar',
  data() {
    return {
      title: 'PUSC'
    }
  },
  created() {
    let lineit = document.createElement('script');
    lineit.setAttribute('src', "https://d.line-scdn.net/r/web/social-plugin/js/thirdparty/loader.min.js");
    document.head.appendChild(lineit);
  }
}
</script>

<style>

</style>
