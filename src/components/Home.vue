<template>
<div id="home">
  <slider></slider>
  <section class="section-padding">
    <div class="container">

      <div class="text-center mb-80">
        <h2 class="section-title text-uppercase">Our Functions</h2>
        <!-- <p class="section-sub">.</p> -->
      </div>

      <div class="row no-gutter">
        <div v-for="ourfunction of functions" :class="ourfunction.col">
          <div class="featured-box border-right text-center hover brand-hover">
            <div class="featured-wrapper">
              <div class="intro-header offset">
                <i class="material-icons brand-icon">{{ourfunction.icon}}</i>
                <h2>{{ourfunction.title}}</h2>
              </div>

              <div class="content offset">
                <p>{{ourfunction.detail}}</p>
              </div>
            </div>
            <!-- /.featured-wrapper -->
          </div>
          <!-- /.featured-box  -->
        </div>
        <!-- /.col-md-3 -->

      </div>
      <!-- /.row -->
    </div>
    <!-- /.container -->
  </section>

  <section class="section-padding gray-bg">
    <div class="container">
      <div class="text-center mb-80">
        <h2 class="section-title">COMMISSIONS</h2>
        <!-- <p>materialize has 8 unique tab style</p> -->
      </div>

      <div class="row">
        <div class="col-md-12">

          <div class="icon-tab">

            <!-- Nav tabs -->
            <div class="text-center">
              <ul class="nav nav-pills" role="tablist">
                <li v-for="ci in commissions" role="presentation" :class="ci.class">
                  <a :href="ci.link" class="waves-effect waves-light" role="tab" data-toggle="tab" :title="ci.title"> <i class="material-icons">{{ci.icon}}</i></a>
                </li>
              </ul>
            </div>

            <!-- Tab panes -->
            <div class="panel-body mt-40">
              <div class="tab-content">
                <div v-for="ct in commissions" role="tabpanel" :class="ct.tabclass" :id="ct.id">

                  <div class="row">
                    <div v-for="cm in ct.member" class="col-md-3 col-sm-6">
                      <div class="team-wrapper text-center">
                        <div class="team-img">
                          <a><img :src="cm.image" class="img-responsive" :alt="cm.name"></a>
                        </div>
                        <!-- /.team-img -->

                        <div class="team-title">
                          <h3><a>{{cm.name}} [{{cm.major}} {{cm.batch}}]</a></h3>
                          <span>{{cm.position}}</span>
                          {{cm}}
                        </div>
                        <!-- /.team-title -->

                        <ul class="team-social-links list-inline">
                          <li><a :href="'mailto:' + cm.email"><i class="fa fa-envelope-o"></i></a></li>
                        </ul>

                      </div>
                      <!-- /.team-wrapper -->
                    </div>
                    <!-- /.col-md-3 -->
                  </div>
                </div>
              </div>
            </div>

          </div>
          <!-- /.icon-tab -->

        </div>
        <!-- /.col-md-12 -->
      </div>
      <!-- /.row -->
    </div>
    <!-- /.container -->
  </section>


  <section class="section-padding banner-6 bg-fixed parallax-bg overlay light-9" data-stellar-background-ratio="0.5">
    <div class="container">

      <div class="text-center mb-80">
        <h2 class="section-title">ADVISORS</h2>
        <!-- <p class="section-sub"></p> -->
      </div>

      <div class="row">
        <div v-for="advisor in advisors" class="col-md-3 col-sm-6">
          <div class="team-wrapper text-center">
            <div class="team-img">
              <a><img :src="advisor.image" class="img-responsive" :alt="advisor.name"></a>
            </div>
            <!-- /.team-img -->

            <div class="team-title">
              <h3><a>{{advisor.name}}</a></h3>
              <span>{{advisor.position}}</span>
            </div>
            <!-- /.team-title -->
          </div>
          <!-- /.team-wrapper -->
        </div>
        <!-- /.col-md-3 -->
      </div>
      <!-- /.row -->

    </div>
    <!-- /.container -->
  </section>

  <section class="section-padding grid-news-hover grid-blog gray-bg">
    <div class="container">

      <div class="text-center mb-80">
        <h2 class="section-title">Latest Articles</h2>
        <!-- <p class="section-sub">Quisque non erat mi. Etiam congue et augue sed tempus. Aenean sed ipsum luctus, scelerisque ipsum nec, iaculis justo. Sed at vestibulum purus, sit amet viverra diam nulla ac nisi rhoncus.</p> -->
      </div>


      <div class="row">
        <div id="blogGrid">
          <div v-for="article in articles" class="col-xs-12 col-sm-6 col-md-4 blog-grid-item">
            <article class="post-wrapper">

              <div class="thumb-wrapper thumb-cut waves-effect waves-block waves-light">
                <router-link :to="'/articles/'+article.slugtitle"><img :src="'https://pusc.or.id/v2/docs/'+article.image" class="img-cut img-responsive" :alt="article.title"></router-link>
              </div>
              <!-- .post-thumb -->

              <div class="blog-content">

                <div class="hover-overlay blue darken-2"></div>

                <header class="entry-header-wrapper">
                  <div class="entry-header">
                    <h2 class="entry-title">
                                <router-link :to="'/articles/'+article.slugtitle">{{article.title}}</router-link>
                              </h2>

                    <div class="entry-meta">
                      <ul class="list-inline">
                        <li>
                          <i class="fa fa-user"></i> <a>PUSC</a>
                        </li>
                        <li>
                          <i class="fa fa-clock-o"></i> <a>{{article.created_at}}</a>
                        </li>
                      </ul>
                    </div>
                    <!-- .entry-meta -->
                  </div>
                  <!-- /.entry-header -->
                </header>
                <!-- /.entry-header-wrapper -->

                <div class="entry-content">
                  <p>{{article.highlight}} <router-link :to="'/articles/'+article.slugtitle">Read More <i class="fa fa-long-arrow-right"></i></router-link></p>
                </div>
                <!-- .entry-content -->
              </div>

            </article>
            <!-- /.post-wrapper -->
          </div>
          <!-- /.col-md-6 -->
        </div>
      </div>
      <!-- /.row -->

    </div>
    <!-- /.container -->
  </section>
</div>
</template>

<script>
import Slider from './Slider.vue'

export default {
  name: 'home',
  components: {
    Slider
  },
  data() {
    return {
      functions: [{
        title: 'Research',
        icon: 'find_in_page',
        detail: 'Conduct research regarding student prosperity and present it to the management of President University.',
        col: 'col-md-2 col-sm-6 col-md-offset-1'
      }, {
        title: 'Aspiration',
        icon: 'lightbulb_outline',
        detail: 'Collect, process and deliver the students\' aspiration regarding student prosperity at university level.',
        col: 'col-md-2 col-sm-6'
      }, {
        title: 'Mediation',
        icon: 'pan_tool',
        detail: 'Become mediator between students, student organizations, and management of President University.',
        col: 'col-md-2 col-sm-6'
      }, {
        title: 'Legislation',
        icon: 'gavel',
        detail: 'Establish laws and regulations for student organizations.',
        col: 'col-md-2 col-sm-6'
      }, {
        title: 'Supervision',
        icon: 'visibility',
        detail: 'Supervise and evaluate the performance of the student executive body at university level of President University.',
        col: 'col-md-2 col-sm-6'
      }],
      commissions: [{
        title: 'Board of Directors',
        class: 'active',
        link: '#bod',
        icon: 'people',
        tabclass: 'tab-pane fade active in',
        id: 'bod',
        member: [{
          name: 'Bryan Johanes Rengkung',
          major: 'CIT',
          batch: '2015',
          position: 'Chairperson',
          image: 'https://pusc.or.id/assets/img/commissions/bryan.jpg',
          email: 'bryanrengkung@gmail.com'
        }, {
          name: 'Novela Permata Sari',
          major: 'IRE',
          batch: '2015',
          position: 'Vice Chairperson',
          image: 'https://pusc.or.id/assets/img/commissions/novela.jpg',
          email: 'novelapermata88@gmail.com'
        }, {
          name: 'Fitriani Sinthanuartyana',
          major: 'COM',
          batch: '2016',
          position: 'Secretary',
          image: 'https://pusc.or.id/assets/img/commissions/fifi.jpg',
          email: 'fitrianisintha22@gmail.com'
        }, {
          name: 'Restu Ayu Adyesti',
          major: 'IEN',
          batch: '2015',
          position: 'Treasurer',
          image: 'https://pusc.or.id/assets/img/commissions/restu.jpg',
          email: 'restuadyesti@gmail.com'
        }]
      }, {
        title: 'Commission I : Academics',
        class: '',
        link: '#com1',
        icon: 'school',
        tabclass: 'tab-pane fade',
        id: 'com1',
        member: [{
          name: 'Gustav Arkady Kadarusman',
          major: 'CIS',
          batch: '2015',
          position: 'Head of Commission I',
          image: 'https://pusc.or.id/assets/img/commissions/gustav.jpg',
          email: 'gkadarusman@gmail.com'
        }, {
          name: 'Angelika Julian Wijaya',
          major: 'IRE',
          batch: '2016',
          position: 'Comparative Study Researcher',
          image: 'https://pusc.or.id/assets/img/commissions/angelika.jpg',
          email: 'msangelikajw@yahoo.com'
        }, {
          name: 'Elsandra Faustina M. Hogo',
          major: 'BUS',
          batch: '2016',
          position: 'Management Relations Officer',
          image: 'https://pusc.or.id/assets/img/commissions/elsa.jpg',
          email: 'elsandrahogo@gmail.com'
        }, {
          name: 'Hendra Kurniawan',
          major: 'BUS',
          batch: '2015',
          position: 'Organizational Relations Officer',
          image: 'https://pusc.or.id/assets/img/commissions/hendra.jpg',
          email: 'pratamahendra38@yahoo.co.id'
        }, {
          name: 'Theodora Owena Putri Chanry',
          major: 'IEN',
          batch: '2016',
          position: 'Qualitative and Quantitative Researcher',
          image: 'https://pusc.or.id/assets/img/commissions/owena.jpg',
          email: 't_owena@gmail.com'
        }]
      }, {
        title: 'Commission II : Campus Facilities',
        class: '',
        link: '#com2',
        icon: 'location_city',
        tabclass: 'tab-pane fade',
        id: 'com2',
        member: [{
          name: 'Fernando Van Wis Lee',
          major: 'MGT',
          batch: '2015',
          position: 'Head of Commission II',
          image: 'https://pusc.or.id/assets/img/commissions/nando.jpg',
          email: 'fernandovwl@gmail.com'
        }, {
          name: 'Kelvin',
          major: 'IEN',
          batch: '2015',
          position: 'Classroom Supervisor',
          image: 'https://pusc.or.id/assets/img/commissions/kelvin.jpg',
          email: 'kelvinchristian25@yahoo.co.id'
        }, {
          name: 'Emmanuella G. M. Huang',
          major: 'IRE',
          batch: '2016',
          position: 'Equipment Supervisor',
          image: 'https://pusc.or.id/assets/img/commissions/emma.jpg',
          email: 'emmanuellahuang@yahoo.com'
        }, {
          name: 'Andrean Winata',
          major: 'MGT',
          batch: '2016',
          position: 'Venue Supervisor',
          image: 'https://pusc.or.id/assets/img/commissions/AW.jpg',
          email: 'andreanana91@gmail.com'
        }, {
          name: 'Putu Andika Wira Bangsawan',
          major: 'MGT',
          batch: '2016',
          position: 'Qualitative and Quantitative Researcher',
          image: 'https://pusc.or.id/assets/img/commissions/andika.jpg',
          email: 'andikawirabangsawan.awb@gmail.com'
        }]
      }, {
        title: 'Commission III : Dormitory Life',
        class: '',
        link: '#com3',
        icon: 'domain',
        tabclass: 'tab-pane fade',
        id: 'com3',
        member: [{
          name: 'Ni Made Maylananda M. W.',
          major: 'MGT',
          batch: '2015',
          position: 'Head of Commission III',
          image: 'https://pusc.or.id/assets/img/commissions/mayla.jpg',
          email: 'maylanandamaharani@gmail.com'
        }, {
          name: 'Amelia Frian',
          major: 'ACC',
          batch: '2015',
          position: 'Public Facilities Coordinator',
          image: 'https://pusc.or.id/assets/img/commissions/amel.jpg',
          email: 'ameliafrian@yahoo.com'
        }, {
          name: 'Varen Vierlita',
          major: 'IRE',
          batch: '2016',
          position: 'Student Activities Coordinator',
          image: 'https://pusc.or.id/assets/img/commissions/varen.jpg',
          email: 'vvierlita@gmail.com'
        }, {
          name: 'Putu Ayudia Maharani Sita',
          major: 'LAW',
          batch: '2016',
          position: 'Female Dormitory Coordinator',
          image: 'https://pusc.or.id/assets/img/commissions/sita.jpg',
          email: 'aranisita@gmail.com'
        }, {
          name: 'Yosua Yonatan',
          major: 'ACC',
          batch: '2016',
          position: 'Male Dormitory Coordinator',
          image: 'https://pusc.or.id/assets/img/commissions/yosua.jpg',
          email: 'yosua.yonatan200198@gmail.com'
        }]
      }, {
        title: 'Commission IV : Events & Activities',
        class: '',
        link: '#com4',
        icon: 'event',
        tabclass: 'tab-pane fade',
        id: 'com4',
        member: [{
          name: 'Kevin Marcelius Prasetio',
          major: 'BUS',
          batch: '2015',
          position: 'Head of Commission IV',
          image: 'https://pusc.or.id/assets/img/commissions/kevin.jpg',
          email: 'kevinmarcelius13@gmail.com'
        }, {
          name: 'Tresno Wicaksono',
          major: 'IRE',
          batch: '2015',
          position: 'Events Supervisor',
          image: 'https://pusc.or.id/assets/img/commissions/tresno.jpg',
          email: 'tresnowicaksono@gmail.com'
        }, {
          name: 'Delsi Ulfayani',
          major: 'BUS',
          batch: '2015',
          position: 'Events Supervisor',
          image: 'https://pusc.or.id/assets/img/commissions/delsi.jpg',
          email: 'delsiulfayani@gmail.com'
        }, {
          name: 'Selly Marcelina',
          major: 'LAW',
          batch: '2015',
          position: 'Events Supervisor',
          image: 'https://pusc.or.id/assets/img/commissions/selly.jpg',
          email: 'sellybuubuu@gmail.com'
        }, {
          name: 'Febby Leonita Kusumawijaya',
          major: 'BUS',
          batch: '2015',
          position: 'Events Supervisor',
          image: 'https://pusc.or.id/assets/img/commissions/febby.jpg',
          email: 'klaudiafebby@yahoo.co.id'
        }]
      }, {
        title: 'Public Relation & Multimedia Division',
        class: '',
        link: '#prm',
        icon: 'phone',
        tabclass: 'tab-pane fade',
        id: 'prm',
        member: [{
          name: 'Putu Prisca Lusiani',
          major: 'IRE',
          batch: '2015',
          position: 'Head of PRM Division',
          image: 'https://pusc.or.id/assets/img/commissions/prisca.jpg',
          email: 'prisca_lusiani@yahoo.co.id'
        }, {
          name: 'Norbertus Krisna A. Utomo',
          major: 'MEN',
          batch: '2015',
          position: 'Designer I',
          image: 'https://pusc.or.id/assets/img/commissions/krisna.jpg',
          email: 'norbertus_krisna@yahoo.co.id'
        }, {
          name: 'Raudhah Azzahra Zein',
          major: 'VCD',
          batch: '2015',
          position: 'Designer II',
          image: 'https://pusc.or.id/assets/img/commissions/zahra.jpg',
          email: 'r.azzahrazein@gmail.com'
        }, {
          name: 'Zilfa Hendarin',
          major: 'VCD',
          batch: '2015',
          position: 'Multimedia Coordinator',
          image: 'https://pusc.or.id/assets/img/commissions/jilpa.jpg',
          email: 'zilfa.hendarin09@gmail.com'
        }, {
          name: 'Naufal Taufiq Ammar',
          major: 'BUS',
          batch: '2015',
          position: 'External Relations Officer',
          image: 'https://pusc.or.id/assets/img/commissions/ammar.jpg',
          email: 'naufaltaufik97@gmail.com'
        }, {
          name: 'Christy Raina S. Mamesah',
          major: 'COM',
          batch: '2016',
          position: 'Public Relations Officer',
          image: 'https://pusc.or.id/assets/img/commissions/cisty.jpg',
          email: 'christyraina@yahoo.com'
        }, {
          name: 'Rakha Viantoni Prastya',
          major: 'CIT',
          batch: '2015',
          position: 'Web Developer',
          image: 'https://pusc.or.id/assets/img/commissions/rakha.jpg',
          email: 'rakha.rvp@gmail.com'
        }]
      }],
      advisors: [{
        name: 'Dr. Agus H. Canny, M.A., M.Sc.',
        position: 'Vice Rector for Student and Alumni Affairs',
        image: 'https://pusc.or.id/assets/img/advisors/pakagus.jpg'
      }, {
        name: 'Purwanto, S.T., M.M.',
        position: 'Head of Student Affairs, Alumni and Counseling Bureau',
        image: 'https://pusc.or.id/assets/img/advisors/pakpurwanto.jpg'
      }, {
        name: 'Susilo, S.Kom.',
        position: 'Head of Student Activities',
        image: 'https://pusc.or.id/assets/img/pusclogo.png'
      }, {
        name: 'Hernawati W. Retno Wiratih, S.Pd, M.Sc.',
        position: 'PUSC & PUSU Adviser',
        image: 'https://pusc.or.id/assets/img/pusclogo.png'
      }, ],
      articles: []
    }
  },
  created() {
    this.$http.get('api/show3articles')
      .then(response => {
        this.articles = response.body
      })
  }
}
</script>

<style>
div.thumb-cut {
  position: relative;
  width: 300px;
  height: 300px;
  overflow: hidden;
}
img.img-cut {
  position: absolute;
  width: 600px;
  height: 300px;
  margin: auto;
}
</style>
