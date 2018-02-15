<template>
<div id="foot">
  <!--footer 1 start -->
  <footer class="footer footer-one">
    <div class="primary-footer blue darken-4">
      <div class="container">
        <a href="#top" class="page-scroll btn-floating btn-large red darken-2 back-top waves-effect waves-light tt-animate btt" data-section="#top">
          <i class="material-icons">&#xE316;</i>
        </a>

        <div class="row">
          <div class="col-md-3 widget clearfix">
            <h2 class="white-text">About Us</h2>
            <p class="white-text">President University Student Council is the student legislative body at university level of President University.
              PUSC is under coordination of Student Affairs Department, which is under Vice Rector III (Vice Rector for Student and Alumni Affairs).</p>

            <ul class="social-link tt-animate ltr">
              <li><a href="https://twitter.com/pusc_presuniv"><i class="fa fa-twitter"></i></a></li>
              <li><a href="https://www.instagram.com/pusc_presuniv/"><i class="fa fa-instagram"></i></a></li>
              <li><a href="https://www.youtube.com/channel/UCNVSuH31ovsNPAgWlzegbNQ"><i class="fa fa-youtube"></i></a></li>
            </ul>
          </div>
          <!-- /.col-md-3 -->

          <div class="col-md-3 widget">
            <h2 class="white-text">Twitter Feed</h2>

            <a class="twitter-timeline" href="https://twitter.com/pusc_presuniv" data-widget-id="685455494010413057" data-chrome="noheader nofooter">Tweets by @pusc_presuniv</a>
          </div>
          <!-- /.col-md-3 -->


          <div class="col-md-6 widget">
            <h2 class="white-text">Instagram Feed</h2>

            <div class="row" id="instafeed"></div>
          </div>
          <!-- /.col-md-3 -->
        </div>
        <!-- /.row -->
      </div>
      <!-- /.container -->
    </div>
    <!-- /.primary-footer -->

    <div class="secondary-footer indigo darken-4">
      <div class="container">
        <span class="white-text">Copyright &copy; 2017 <a href="#">PUSC</a> &nbsp; | &nbsp;  All Rights Reserved &nbsp; | &nbsp;  Created & Developed with &#9829 by <a href="http://rakha.arvipi.com" target="_blank">Rakha Viantoni</a></span>
      </div>
      <!-- /.container -->
    </div>
    <!-- /.secondary-footer -->
  </footer>
  <!--footer 1 end-->
</div>
</template>

<script>
export default {
  name: 'footer',
  data() {
    return {
      title: 'PUSC'
    }
  },
  created() {
    let twitterwidget = document.createElement('script');
    twitterwidget.setAttribute('src', "//platform.twitter.com/widgets.js");
    document.head.appendChild(twitterwidget);
  }
}
</script>

<style>

</style>
