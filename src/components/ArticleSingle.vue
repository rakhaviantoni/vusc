<template>
<div id="single-article">
  <!--page title start-->
  <section class="page-title ptb-50">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h2>{{ article.title }}</h2>
          <ol class="breadcrumb">
            <li><router-link :to="'/'">Home</router-link></li>
            <li><router-link :to="'/articles'">Articles</router-link></li>
            <li class="active">{{ article.title }}</li>
          </ol>
        </div>
      </div>
    </div>
  </section>
  <!--page title end-->


  <!-- blog section start -->
  <section class="blog-section section-padding">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <div class="posts-content single-post">

            <article class="post-wrapper">

              <header class="entry-header-wrapper clearfix">

                <!-- <div class="author-thumb waves-effect waves-light">
                              <a href="#"><img src="assets/img/blog/author.jpg" alt=""></a>
                            </div> -->

                <div class="entry-header">
                  <h2 class="entry-title">{{ article.title }}</h2>

                  <div class="entry-meta">
                    <ul class="list-inline">
                      <li>
                        <i class="fa fa-user"></i><a>PUSC</a>
                      </li>

                      <li>
                        <i class="fa fa-clock-o"></i><a>{{ article.created_at }}</a>
                      </li>

                      <!-- <li>
                                          <i class="fa fa-heart-o"></i><a><span>1</span></a>
                                      </li>

                                      <li>
                                          <i class="fa fa-comment-o"></i><a>3</a>
                                      </li> -->
                    </ul>
                  </div>
                  <!-- .entry-meta -->
                </div>

              </header>
              <!-- /.entry-header-wrapper -->

              <div class="thumb-wrapper">
                <a :href="'https://pusc.or.id/v2/docs/'+article.image" class="tt-lightbox" :title="article.title"></a><img :src="'https://pusc.or.id/v2/docs/'+article.image" class="img-responsive" :alt="article.title" :title="article.title">
              </div>
              <!-- .post-thumb -->


              <div class="entry-content">
                <!-- <p>{{ article.description }}</p> -->
                <div v-html="article.description"></div>
              </div>
              <!-- .entry-content -->


              <footer class="entry-footer">
                <div class="post-tags">
                  <span class="tags-links">
                                <i class="fa fa-tags"></i><a>{{ article.category }}</a>
                              </span>
                </div>
                <!-- .post-tags -->

                <ul class="list-inline right share-post">
                  <li>
                    <div class="line-it-button" data-lang="en" data-type="share-a" :data-url="'https://pusc.or.id/articles/' + article.slugtitle" style="display: none;"></div>
                  </li>
                  <!-- <li><a href="#"><i class="fa fa-facebook"></i> <span>Share</span></a>
                                </li>
                                <li><a href="#"><i class="fa fa-twitter"></i> <span>Tweet</span></a>
                                </li>
                                <li><a href="#"><i class="fa fa-google-plus"></i> <span>Plus</span></a>
                                </li> -->
                </ul>
              </footer>

            </article>
            <!-- /.post-wrapper -->

            <!-- <nav class="single-post-navigation" role="navigation">
                          <div class="row">
                            <div class="col-xs-6">
                              <div class="previous-post-link">
                                <a class="waves-effect waves-light" href="#"><i class="fa fa-long-arrow-left"></i>Read Previous Post</a>
                              </div>
                            </div>

                            <div class="col-xs-6">
                              <div class="next-post-link">
                                <a class="waves-effect waves-light" href="#">Read Next Post<i class="fa fa-long-arrow-right"></i></a>
                              </div>
                            </div>
                          </div>
                        </nav> -->

            <div class="comments-wrapper">
              <div class="comments-tab">

                <!-- Nav tabs -->
                <ul class="nav nav-tabs nav-justified" role="tablist">
                  <li role="presentation" class="active"><a href="#default-comment" class="waves-effect waves-light" role="tab" data-toggle="tab">Leave a comment now</a></li>
                  <!-- <li role="presentation"><a href="#facebook-comment" class="waves-effect waves-light" role="tab" data-toggle="tab">Facebook Comment</a></li> -->
                </ul>

                <!-- Tab panes -->
                <div class="panel-body">
                  <div class="tab-content">
                    <div role="tabpanel" class="tab-pane fade in active" id="default-comment">
                      <div id="disqus_thread"></div>
                      <noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>

                    </div>
                    <!-- <div role="tabpanel" class="tab-pane fade" id="facebook-comment">
                                    <p>Duis senectus mus condimentum nunc ac habitasse duis consectetur a arcu a accumsan cras et metus ultricies justo cum a bibendum. <a href="#">Egestas vestibulum blandit sem vestibulum curabitur</a> a vel aliquet gravida ullamcorper amet dictumst vestibulum a elementum proin id volutpat magna parturient. Id ac dui libero a ullamcorper euismod himenaeos a nam condimentum a adipiscing dapibus lobortis iaculis morbi.</p>

                                    <p>Himenaeos a vestibulum morbi. <a href="#">Ullamcorper cras scelerisque</a> taciti lorem metus feugiat est lacinia facilisis id nam leo condimentum praesent id diam. Vestibulum amet porta odio elementum convallis parturient tempor tortor tempus a mi ad parturient ad nulla mus amet in penatibus nascetur at vulputate euismod a est tristique scelerisque. Aliquet facilisis nisl vel vestibulum dignissim gravida ullamcorper hac quisque ad at nisl egestas adipiscing vel blandit.</p>
                                </div> -->
                  </div>
                  <!-- /.tab-content -->
                </div>
                <!-- /.panel-body -->

              </div>
              <!-- /.comments-tab -->

            </div>
            <!-- /.comments-wrapper -->

          </div>
          <!-- /.posts-content -->
        </div>
        <!-- /.col-md-12 -->

      </div>
      <!-- /.row -->
    </div>
    <!-- /.container -->
  </section>
  <!-- blog section end -->
</div>
</template>

<script>
export default {
  name: 'articlesingle',
  data() {
    return {
      article: {}
    }
  },
  created() {
    this.$http.get('api/articles/' + this.$route.params.slug)
      .then(response => {
        this.article = response.body
      });
    let disqus = document.createElement('script');
    disqus.setAttribute('src', "//puscorid.disqus.com/embed.js");
    document.head.appendChild(disqus);
    let lineit = document.createElement('script');
    lineit.setAttribute('src', "https://d.line-scdn.net/r/web/social-plugin/js/thirdparty/loader.min.js");
    document.head.appendChild(lineit);
  }
}
</script>

<style>

</style>
