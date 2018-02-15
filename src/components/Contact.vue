<template>
<div id="contact">
  <!--page title start-->
  <section class="page-title ptb-50">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>Contact</h2>
          <ol class="breadcrumb">
            <li>
              <router-link :to="'/'">Home</router-link>
            </li>
            <li class="active">Contact</li>
          </ol>
        </div>
      </div>
    </div>
  </section>
  <!--page title end-->

  <section class="section-padding">
    <div class="container">

      <div class="text-center mb-80">
        <h2 class="section-title">Contact Us</h2>
      </div>

      <div class="row">
        <div class="col-md-8">
          <form name="contact-form" id="contactForm" action="sendemail.php" method="POST">

            <div class="row">
              <div class="col-md-6">
                <div class="input-field">
                  <input id="name" type="text" name="name" class="validate" required>
                  <label for="name">Name (Major & Batch)</label>
                </div>

              </div>
              <!-- /.col-md-6 -->

              <div class="col-md-6">
                <div class="input-field">
                  <label class="sr-only" for="email">Email</label>
                  <input id="email" type="email" name="email" class="validate" required>
                  <label for="email" data-error="wrong" data-success="right">Email</label>
                </div>
              </div>
              <!-- /.col-md-6 -->
            </div>
            <!-- /.row -->

            <div class="row">
              <div class="col-md-6">
                <div class="input-field">
                  <input id="subject" type="text" name="subject" class="validate" required>
                  <label for="phone">Subject</label>
                </div>
              </div>
              <!-- /.col-md-6 -->

              <div class="col-md-6">
                <div class="input-field">
                  <input id="classification" type="text" name="classification" class="validate" required>
                  <label for="phone">Classification</label>
                  <!-- <select v-model="selected" v-if="loaded" id="classification" name="classification" class="validate" required />
                                  <option value="" disabled selected>Classification</option>
                                  <option v-for="option in options" v-bind:value="value">{{value}}</option>
                              </select> -->
                </div>
              </div>
              <!-- /.col-md-6 -->
            </div>
            <!-- /.row -->

            <div class="input-field">
              <textarea name="message" id="message" class="materialize-textarea"></textarea>
              <label for="message">Message</label>
            </div>

            <label for="button">* You may contact through Chatra Live Chat (Icon on the right side) for now</label>
            <button type="submit" name="submit" class="waves-effect waves-light btn submit-button red darken-2 mt-30" disabled>Send Message</button>
          </form>
        </div>
        <!-- /.col-md-8 -->

        <div class="col-md-4 contact-info">

          <address>
                        <i class="material-icons brand-color">&#xE55F;</i>
                        <div class="address">
                          President University Campus Jalan Ki Hajar Dewantara, Jababeka Education Park Cikarang, West Java 17550
                        </div>

                        <i class="material-icons brand-color">&#xE0E1;</i>
                        <div class="mail">
                          <p><a href="mailto:pusc@president.ac.id">pusc@president.ac.id</a></p>
                        </div>
                      </address>

        </div>
        <!-- /.col-md-4 -->
      </div>
      <!-- /.row -->
    </div>
    <!-- /.container -->
  </section>
  <!-- contact-form-section End -->


  <!-- map-section -->
  <!-- <div id="gmap" class="height-350"></div> -->
  <gmap class="height-350"></gmap>
  <!-- /.map-section -->
</div>
</template>

<script>
import Gmap from './Gmap.vue'

export default {
  name: 'contact',
  components: {
    Gmap
  },
  data() {
    return {
      options: [{
        value: 'Academics'
      }, {
        value: 'Campus Facilities'
      }, {
        value: 'Dormitory Life'
      }, {
        value: 'Events & Activities'
      }, {
        value: 'Other'
      }, ],
      loaded: true
    }
  }
}
</script>

<style>

</style>
