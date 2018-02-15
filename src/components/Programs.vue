<template>
<div id="programs">
  <!--page title start-->
  <section class="page-title ptb-50">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>Programs</h2>
          <ol class="breadcrumb">
            <li><router-link :to="'/'">Home</router-link></li>
            <li class="active">Programs</li>
          </ol>
        </div>
      </div>
    </div>
  </section>
  <!--page title end-->

  <section class="section-padding">
    <div class="container">

      <h2 class="section-title">Description</h2>
      <div class="row">
        <div class="col-md-12">

          <p>PUSC stands for President University Student Council which is the highest legal organization and legislative body in President University.</p>

          <p>PUSC serves as the mediator between students and President University management by receiving students' aspiration and delivering them to the management, as well as helping the management in disseminating information related to President University.</p>
        </div>
        <!-- /.col-md-7 -->
      </div>
      <!-- /.row -->
    </div>
    <!-- /.container -->
  </section>

  <section class="padding-top-80 padding-bottom-80">
    <div class="container">
      <div class="row">

        <div class="col-md-6">
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
                  Become the reliable liaison for students and management by upholding the integrity among PUSC members and creating great impact for President University.
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
                    <li>Build strong relation amongst internal, legal organizations and Management to improve positive coordination and collaboration.</li>
                    <li>Create the power of attaining the goals or vision by focus on group discussion.</li>
                    <li>Enhance the law supremacy and certainty for every issues by being accountable and transparent.</li>
                    <li>Deliver students aspiration to the management with responsibility.</li>
                    <li>Encourage the innovation and creativity in solving the problems.</li>
                  </ol>
                </div>
              </div>
            </div>
          </div>
        </div>
        <!-- /.col-md-6 -->


        <div class="col-md-6">
          <h2 class="text-medium mb-30">History</h2>
          <div id="client-testimonial" class="carousel slide carousel-testimonial text-center gray-bg" data-ride="carousel">

            <!-- Wrapper for slides -->
            <div class="carousel-inner" role="listbox">
              <div class="item active">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="Customer Thumb">
                </div>
                <div class="content">
                  <p>President University Student Union (PUSU) was established as the executive organization which concerns on non-academic activities.</p>

                  <div class="testimonial-meta red-text darken-2">
                    August 28th 2008
                  </div>
                </div>
              </div>

              <div class="item">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="Customer Thumb">
                </div>
                <div class="content">
                  <p>President University Student Council (PUSC) was established as the legislative organization.</p>

                  <div class="testimonial-meta red-text darken-2">
                    November 1st 2008
                  </div>
                </div>
              </div>

              <div class="item">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="Customer Thumb">
                </div>
                <div class="content">
                  <p>The Establishment of President University Major Association (PUMA) which concerns on academic activities and the scope is its own major only. In the initiation, PUMAs were under the supervision of Vice Rector I and PUSC.</p>

                  <div class="testimonial-meta red-text darken-2">
                    2010
                  </div>
                </div>
              </div>

              <div class="item">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="Customer Thumb">
                </div>
                <div class="content">
                  <p>PUMAs were under the supervision of Vice Rector I and this emphasizes the indirect relationship with PUSC and PUSU.</p>

                  <div class="testimonial-meta red-text darken-2">
                    2013
                  </div>
                </div>
              </div>

              <div class="item">
                <div class="avatar">
                  <img src="https://www.materialui.co/materialIcons/action/history_grey_192x192.png" alt="Customer Thumb">
                </div>
                <div class="content">
                  <p>The establishment of Commission IV: Events and Activities which the main function is supervising all events and activities of PUSU.</p>

                  <div class="testimonial-meta red-text darken-2">
                    2014
                  </div>
                </div>
              </div>

            </div>

            <!-- Controls -->
            <a class="left carousel-control" href="#client-testimonial" role="button" data-slide="prev">
              <span class="material-icons" aria-hidden="true">&#xE5C4;</span>
              <span class="sr-only">Previous</span>
            </a>
            <a class="right carousel-control" href="#client-testimonial" role="button" data-slide="next">
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
  name: 'programs',
  data() {
    return {
      title: 'PUSC'
    }
  }
}
</script>

<style>

</style>
