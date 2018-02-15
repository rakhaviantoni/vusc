<template>
<div id="partners">
  <!--page title start-->
  <section class="page-title ptb-50">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>Student Organizations</h2>
          <ol class="breadcrumb">
            <li><router-link :to="'/'">Home</router-link></li>
            <li class="active">Student Organizations</li>
          </ol>
        </div>
      </div>
    </div>
  </section>
  <!--page title end-->

  <section class="section-padding list-news">
    <div class="container">

      <div class="text-center mb-80">
        <h2 class="section-title">Student Organizations</h2>
        <!-- <p class="section-sub">Quisque non erat mi. Etiam congue et augue sed tempus. Aenean sed ipsum luctus, scelerisque ipsum nec, iaculis justo. Sed at vestibulum purus, sit amet viverra diam nulla ac nisi rhoncus.</p> -->
      </div>


      <div class="clients-grid grid-gutter">
        <div class="row">

          <div v-for="partner in partners" class="col-md-3 col-sm-6">
            <div class="border-box">
              <a :href="partner.link" target="_blank">
                <img :src="partner.image" :alt="partner.name" :title="partner.name">
              </a>
            </div>
            <!-- /.border-box -->
          </div>
          <!-- /.col-md-3 -->

        </div>
        <!-- /.row -->
      </div>
      <!-- /.clients-grid -->

    </div>
    <!-- /.container -->
  </section>
</div>
</template>

<script>
export default {
  name: 'partners',
  data() {
    return {
      partners: [{
        name: 'President University Student Union',
        link: 'http://pusu.or.id',
        image: 'https://pusc.or.id/assets/img/partners/pusu-compressor.png'
      }, {
        name: 'President University Major Association of Accounting',
        link: 'http://acc.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/acc-compressor.png'
      }, {
        name: 'President University Major Association of Bussiness Administration',
        link: 'http://ba.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/bus-compressor.png'
      }, {
        name: 'President University Major Association of Communication',
        link: 'http://com.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/comm-compressor.png'
      }, {
        name: 'President University Major Association of Computing',
        link: 'https://pucomputing.org/',
        image: 'https://pusc.or.id/assets/img/partners/comp-compressor.png'
      }, {
        name: 'President University Major Association of Electrical Engineering',
        link: 'http://ee.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/een-compressor.png'
      }, {
        name: 'President University Major Association of Environmental Engineering',
        link: 'http://env.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/env-compressor.png'
      }, {
        name: 'President University Major Association of Industrial Engineering',
        link: 'http://ie.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/ien-compressor.png'
      }, {
        name: 'President University Major Association of International Relations',
        link: 'http:/irpresuniv.org/',
        image: 'https://pusc.or.id/assets/img/partners/ir-compressor.png'
      }, {
        name: 'President University Major Association of Law',
        link: 'http://law.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/law-compressor.png'
      }, {
        name: 'President University Major Association of Mechanical Engineering',
        link: 'http://me.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/men-compressor.png'
      }, {
        name: 'President University Major Association of Management',
        link: 'http://mgt.president.ac.id/',
        image: 'https://pusc.or.id/assets/img/partners/mgt-compressor.png'
      }]
    }
  }
}
</script>

<style>

</style>
