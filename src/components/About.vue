<template>
<div id="about">
  <!--page title start-->
  <section class="page-title ptb-50">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>About Us</h2>
          <ol class="breadcrumb">
            <li>
              <router-link :to="'/'">Home</router-link>
            </li>
            <li class="active">About Us</li>
          </ol>
        </div>
      </div>
    </div>
  </section>
  <!--page title end-->

  <section class="section-padding">
    <div class="container">

      <div class="text-center mb-80">
        <h2 class="section-title">About Us</h2>
      </div>

      <h2 class="text-medium mb-30">Description</h2>
      <div class="row">
        <div class="col-md-12">

          <p>President University Student Council is the student legislative body at university level of President University. PUSC is under coordination of Student Affairs Department, which is under Vice Rector III (Vice Rector for Student and Alumni Affairs).</p>

          <p>PUSC consists of
            <router-link :to="'/commissions#bod'">Board of Directors</router-link>,
            <router-link :to="'/commissions#commission'">Members of Commissions</router-link>, and
            <router-link :to="'/commissions#prm'">Members of Internal Bureau</router-link>.
            <br>Board of Directors of PUSC consists of Chairperson and Vice Chairperson, Secretary and Treasurer, Head of Commission I to IV and Head of Internal Bureau.</p>

          <h2 class="text-medium mb-30">Functions</h2>
          <p>President University Student Council has 5 functions:</p>

          <div class="row no-gutter mb-30">
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

          <h2 class="text-medium mb-30">Projects</h2>
          <ol>
            <li>
              <p>President University Student Union Presidential Election (PUSU PE)</br>
                PUSU PE is the annual election of President and Vice President of PUSU. It consists of Socialization, Open Registration and Verification, Interview, Campaign Week, and General Election. It involves all active President University as voters.</p>
            </li>
            <li>
              <p>Grand Inauguration</br>
                Grand Inauguration is the inauguration of PUSC, PUSU and PUMAs official members that marks the transition to a new working period.</p>
            </li>
          </ol>

          <h2 class="text-medium mb-30">Former Chairpersons</h2>
          <ol>
            <li>Period of 2010: Lukas Adi Prakoso</li>
            <li>Period of 2011: Immanuel Edo Adita Satria (CIT 2009)</li>
            <li>Period of 2012: Haryanto (CIT 2010)</li>
            <li>Period of 2013: Ayu Yunia Harsari (IRE 2011)</li>
            <li>Period of 2014: Grace Debora Christina (IRE 2012)</li>
            <li>Period of 2015: James Tedy (IEN 2013)</li>
            <li>Period of 2016: Paulina (MGT 2014)</li>
          </ol>

        </div>
        <!-- /.col-md-12 -->
      </div>
      <!-- /.row -->
    </div>
    <!-- /.container -->
  </section>

  <section class="padding-top-80 padding-bottom-80">
    <div class="container">
      <div class="row">

        <div class="col-md-6" id="visionandmissions">
          <h2 class="text-medium mb-30">What Do We Do?</h2>
          <div class="panel-group feature-accordion brand-accordion icon angle-icon" id="accordion-one">
            <div class="panel panel-default">
              <div class="panel-heading">
                <h3 class="panel-title">
                          <a data-toggle="collapse" data-parent="#accordion-one" href="#collapse-one">
                            Vision
                          </a>
                        </h3>
              </div>
              <div id="collapse-one" class="panel-collapse collapse in">
                <div class="panel-body">
                  Become the reliable mediator for students, student organizations, and management of President Univeristy to create progressive change for President University.
                </div>
              </div>
            </div>
            <div class="panel panel-default">
              <div class="panel-heading">
                <h3 class="panel-title">
                          <a data-toggle="collapse" data-parent="#accordion-one" href="#collapse-two">
                            Missions
                          </a>
                        </h3>
              </div>
              <div id="collapse-two" class="panel-collapse collapse in">
                <div class="panel-body">
                  <ol>
                    <li>Strengthen the internal relations through synergy and deliberation.</li>
                    <li>Collaborate with the Management of President University to create conducive environment for student activities.</li>
                    <li>Bring continuous improvements through aspiration for students' welfare.</li>
                    <li>Foster mutual growth and complementary relations with student organizations.</li>
                    <li>Enhance the quality of student events and activities through accountability, trust, and constructive criticism.</li>
                    <li>Keep peace, maintain justice and promote sustainability through law and order.</li>
                  </ol>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- /.col-md-6 -->


        <div class="col-md-6">
          <h2 class="text-medium mb-30">History</h2>
          <div id="history" class="carousel slide carousel-testimonial text-center gray-bg" data-ride="carousel">

            <!-- Wrapper for slides -->
            <div class="carousel-inner" role="listbox">
              <div class="item active">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="History">
                </div>
                <div class="content">
                  <p>President University Student Union (PUSU) was established as the student executive organization which concerns on non-academic activities.</p>

                  <div class="testimonial-meta red-text darken-2">
                    August 28th 2008
                  </div>
                </div>
              </div>

              <div class="item">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="History">
                </div>
                <div class="content">
                  <p>President University Student Council (PUSC) was established as the student legislative organization.</p>

                  <div class="testimonial-meta red-text darken-2">
                    November 1st 2008
                  </div>
                </div>
              </div>

              <div class="item">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="History">
                </div>
                <div class="content">
                  <p>President University Major Association (PUMA) was established which concerns on academic activities at study programs level. PUMA was under coordination of PUSC and Vice Rector III.</p>

                  <div class="testimonial-meta red-text darken-2">
                    2010
                  </div>
                </div>
              </div>

              <div class="item">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="History">
                </div>
                <div class="content">
                  <p>The structural position of PUMA was moved under Vice Rector I and there is coordinative relation with PUSC.</p>

                  <div class="testimonial-meta red-text darken-2">
                    2013
                  </div>
                </div>
              </div>

              <div class="item">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="History">
                </div>
                <div class="content">
                  <p>Commission IV of PUSC which concerns on supervision and evaluation of PUSU's events and activities was established.</p>

                  <div class="testimonial-meta red-text darken-2">
                    2014
                  </div>
                </div>
              </div>

            </div>

            <!-- Controls -->
            <a class="left carousel-control" href="#history" role="button" data-slide="prev">
              <span class="material-icons" aria-hidden="true">&#xE5C4;</span>
              <span class="sr-only">Previous</span>
            </a>
            <a class="right carousel-control" href="#history" role="button" data-slide="next">
              <span class="material-icons" aria-hidden="true">&#xE5C8;</span>
              <span class="sr-only">Next</span>
            </a>
          </div>
        </div>
        <!-- /.col-md-6 -->

      </div>
      <!-- /.row -->

    </div>
    <!-- /.container -->
  </section>
</div>
</template>

<script>
export default {
  name: 'about',
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
      }]
    }
  }
}
</script>

<style>

</style>
