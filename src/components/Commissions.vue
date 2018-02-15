<template>
<div id="commissions">
  <!--page title start-->
  <section class="page-title ptb-50">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>Commissions</h2>
          <ol class="breadcrumb">
            <li><router-link :to="'/'">Home</router-link></li>
            <li class="active">Commissions</li>
          </ol>
        </div>
      </div>
    </div>
  </section>
  <!--page title end-->

  <section v-for="com in commission" class="section-padding" :id="com.id">
    <div class="container">
      <div class="text-center mb-80">
        <h2 class="section-title">{{com.title}}</h2>
      </div>

      <div class="row">
        <div v-for="cm in com.member" class="col-md-3 col-sm-6">
          <div class="team-wrapper text-center">
            <div class="team-img">
              <a><img :src="cm.image" class="img-responsive" :alt="cm.name"></a>
            </div>
            <!-- /.team-img -->

            <div class="team-title">
              <h3><a>{{cm.name}} [{{cm.major}} {{cm.batch}}]</a></h3>
              <span>{{cm.position}}</span>
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
  </section>
</div>
</template>

<script>
export default {
  name: 'commissions',
  data() {
    return {
      commission: [{
        title: 'Board of Directors',
        id: 'bod',
        class: 'active',
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
        id: 'commissioni',
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
        id: 'commissionii',
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
        id: 'commissioniii',
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
        id: 'commissioniv',
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
      }]
    }
  }
}
</script>

<style>

</style>
