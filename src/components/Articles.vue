<template>
<div id="articles">
  <!--page title start-->
  <section class="page-title ptb-50">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>Articles</h2>
          <ol class="breadcrumb">
            <li>
              <router-link :to="'/'">Home</router-link>
            </li>
            <li class="active">Articles</li>
          </ol>
        </div>
      </div>
    </div>
  </section>
  <!--page title end-->

  <section class="section-padding grid-news-hover grid-blog">
    <div class="container">

      <div class="text-center mb-80">
        <h2 class="section-title">Articles</h2>
        <!-- <p class="section-sub">Quisque non erat mi. Etiam congue et augue sed tempus. Aenean sed ipsum luctus, scelerisque ipsum nec, iaculis justo. Sed at vestibulum purus, sit amet viverra diam nulla ac nisi rhoncus.</p> -->
      </div>


      <div class="row">
        <div id="blogGrid">
          <div v-for="article in articles" class="col-xs-12 col-sm-6 col-md-4 blog-grid-item">
            <article class="post-wrapper">

              <div class="thumb-wrapper humb-cut waves-effect waves-block waves-light">
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
                  <p>{{article.highlight}}
                    <router-link :to="'/articles/'+article.slugtitle">Read More <i class="fa fa-long-arrow-right"></i></router-link>
                  </p>
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
export default {
  name: 'articles',
  data() {
    return {
      articles: []
    }
  },
  created() {
    this.$http.get('api/articles')
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
