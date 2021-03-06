---
layout: index
title: Richard Littauer
tagline: My personal website, where I list all of my main projects and occasionally blog.
---
{% include JB/setup %}

<div class="wrapper">
  <div class="container">
    <h1>Richard Littauer</h1>
    <h2 class="quotes display-first">Developer</h2>
    <h2 class="quotes">Nomad</h2>
    <h2 class="quotes">Linguist</h2>
    <h2 class="quotes">Poet</h2>
    <h2 class="quotes">Designer</h2>
    <h2 class="quotes">Organizer</h2>
    <h2 class="quotes">Sailor</h2>
    <h2 class="quotes">Writer</h2>
    <h2 class="quotes">Trekker</h2>
    <h2 class="quotes">Creator</h2>

    <div class='social-media'>
      <a href="https://github.com/RichardLitt" rel="me"><i class="fa fa-github"></i></a>
      <a href="https://twitter.com/#!/richlitt" rel="me"><i class="fa fa-twitter"></i></a>
      <a href="https://medium.com/@richlitt"><i class="fa fa-medium"></i></a>
      <a href="https://instagram.com/richlittv3/"><i class="fa fa-instagram"></i></a>
      <a href="https://dribbble.com/richlitt"><i class="fa fa-dribbble"></i></a>
      <a href="http://www.flickr.com/photos/101526362@N04/"><i class="fa fa-flickr"></i></a>
      <a href="http://www.last.fm/user/RichardFenn"><i class="fa fa-lastfm"></i></a>
      <a href="https://angel.co/richlitt"><i class="fa fa-angellist"></i></a>
    </div>

    <!--
    <div class="posts">
      {% for post in site.posts limit:3 %}
      <a href="{{ BASE_PATH }}{{ post.url }}">{{ post.title }}</a><br />
      {% endfor %}
      <a class="more" href="/archive">More posts...</a>
    </div>
    -->

    <form class="tlemailform" action="https://tinyletter.com/richlitt" method="post" target="popupwindow" onsubmit="window.open('https://tinyletter.com/richlitt', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true">
      <span class="input input--madoka">
          <input type="hidden" value="1" name="embed" />
          <input class="input__field input__field--madoka" name="email" type="text" id="tlemail" />
          <label class="input__label input__label--madoka" for="tlemail">
          <svg class="graphic graphic--madoka" width="100%" height="100%" viewBox="0 0 404 77" preserveAspectRatio="none">
          <path d="m0,0l404,0l0,77l-404,0l0,-77z"/>
          </svg>
          <span class="input__label-content input__label-content--madoka">Email</span>
      </label>
      </span>
      <button class="btn btn-subscribe" type="submit" value="Subscribe">Start reading my weekly newsletter</button>
    </form>

    <div class="posts"><a href="/the-litt-review/">...or check out what I am reading at The Litt Review.</a></div>


    <div class="row col-md-12 projects">
      {% assign projects = (site.projects | sort: 'ranking') %}
      {% for project in projects limit:16 %}
        {% assign loopindex = forloop.index | modulo: 3 %}
        {% if loopindex == 1 %}
          <div class="project col-xs-6 col-sm-4 col-md-3 no-left-margin">
        {% else %}
          <div class="project col-xs-6 col-sm-4 col-md-3">
        {% endif %}
            <div class="img-container">
              <a href="{{ project.url }}">
                <img src="assets/img/project/{{ project.picture }}" class="card-image"/>
              </a>
            </div>
            <a class="project-title" href="{{ project.url }}">
              <h4>
                {{ project.title }}
              </h4>
              <p>{{ project.stub}}<br />
              {{ project.role }} <span class="status">{{ project.status }}</span></p>
            </a>
          </div>
        {% if forloop.index == 3 %}
          <div class="clearfix visible-sm-block"></div>
        {% elsif forloop.index == 4 %}
          <div class="clearfix visible-md-block visible-lg-block"></div>
        {% elsif forloop.index == 12 %}
          <div class="clearfix visible-md-block visible-lg-block"></div>
        {% endif %}
      {% endfor %}
    </div>
  </div>
</div>

<div class="wrapper" id="contact" >
  <div class="container">
    <div class="row col-md-12 press" >
      <div class="col-sm-5 col-sm-offset-1 col-md-5 col-md-offset-1 speak">
        <h1 >Speak</h1>
        <p><a href="mailto:richard@burntfen.com">richard@burntfen.com</a></p>
        <p>I build things, make art, code tools, write words, have fun.</p>
        <p>I am available for…</p>
        <p class="visible-xs available">Writing • Talks • UX • Code • Walks • Letters • Collaboration • Ideas • Joy • Design • Projects</p>
      </div>
      <div class="col-sm-5 col-md-5 listen">
        <hr class="visible-xs">
        <h1 >Listen</h1>
        <div>
          <p><a href="https://tinyletter.com/richlitt">tinyletter.com/richlitt</a></p>
          <p>I write a weekly newsletter, from me to your inbox.</p>
          <p class="hidden-xs">I write about…</p>
        </div>
      </div>
      </div>
    <div class="row col-md-8 col-md-offset-2 hidden-xs">
      <p class="available available-sm">Writing • Talks • UX • Code • Walks • Letters • Collaboration • Ideas • Joy • Design • Projects</p>
    </div>
  </div>
</div>


<div class="wrapper">
  <div class="container">

    <div class="row col-md-12 press">
      <h1 class="section-header">Press</h1>
      {% for press in site.data.press %}
        {% if forloop.index == 7 %}
          <div class="col-xs-4 col-sm-3 col-md-2 col-md-offset-2">
        {% elsif forloop.index == 9 %}
          <div class="col-xs-4 col-sm-3 col-sm-offset-3 col-md-2 col-md-offset-0">
        {% elsif forloop.index == 10 %}
          <div class="col-xs-4 col-xs-offset-4 col-sm-3 col-sm-offset-0 col-md-2">
        {% else %}
          <div class="col-xs-4 col-sm-3 col-md-2">
        {% endif %}
          <div class="img-container">
            <a href="{{ press.url }}" title="{{ press.title }}">
              <img src="assets/img/press/{{ press.image }}" class="card-image">
            </a>
          </div>
        </div>
      {% endfor %}
    </div>

  </div>
</div>

<div class="wrapper" id="other-projects">
  <div class="container">

    <div class="row col-md-12 projects">
      <h1 class="section-header">Other Projects</h1>
      {% assign projects = (site.projects | sort: 'ranking') %}
      {% for project in projects offset:16 %}
        {% assign loopindex = forloop.index | modulo: 3 %}
        {% if loopindex == 1 %}
          <div class="project col-xs-6 col-sm-4 col-md-3 no-left-margin" >
        {% else %}
          <div class="project col-xs-6 col-sm-4 col-md-3">
        {% endif %}
            <div class="img-container">
              <a href="{{ project.url }}">
                <img src="assets/img/project/{{ project.picture }}" class="card-image"/>
              </a>
            </div>
            <a class="project-title" href="{{ project.url }}">
              <h4>
                {{ project.title }}
              </h4>
              <p>{{ project.stub}}<br />
              {{ project.role }} <span class="status">{{ project.status }}</span></p>
            </a>
          </div>
          {% if forloop.index == 3 %}
            <div class="clearfix visible-sm-block"></div>
          {% elsif forloop.index == 4 %}
            <div class="clearfix visible-md-block visible-lg-block"></div>
          {% elsif forloop.index == 16 %}
            <div class="clearfix visible-md-block visible-lg-block"></div>
          {% elsif forloop.index == 20 %}
            <div class="clearfix visible-md-block visible-lg-block"></div>
          {% endif %}
      {% endfor %}
    </div>

     <footer>
     <p>Send me a letter: <a href="mailto:richard@burntfen.com">richard@burntfen.com</a></p>
     <p><a href='http://webring.dinhe.net/prev/burntfen.com'>Previous</a> (<a href="http://webring.dinhe.net/">Join the retronaut webring.</a>) <a href='http://webring.dinhe.net/next/burntfen.com'>Next</a>
      </p>
      <p>{{ site.author.name }} &copy; {{ site.time | date: '%Y' }}.
        <a href="https://github.com/RichardLitt/richardlitt.github.com">Source</a>.
      </p>
    </footer>
  <div class="push"></div>

</div> <!-- /container -->

</div> <!-- /wrapper -->
