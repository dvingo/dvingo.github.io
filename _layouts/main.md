<!DOCTYPE html>
<html>
  <head>
    <meta charset='utf-8'>
    <meta http-equiv="X-UA-Compatible" content="chrome=1">
    <link rel="stylesheet" type="text/css" href="stylesheets/stylesheet.css" media="screen">
    <link rel="stylesheet" type="text/css" href="stylesheets/pygment_trac.css" media="screen">
    <title>Dvingo.GitHub.io by dvingo</title>
  </head>
  <body>
    <header>
      <div class="container">
        <h1>Dvingo.GitHub.io</h1>
        <section id="downloads">
          <a href="https://github.com/dvingo" class="btn btn-github"><span class="icon"></span>View on GitHub</a>
          <a href="/about.html" class="btn"></span>About</a>
        </section>
      </div>
    </header>

    <div class="container">
      <section id="main_content">
      <ul>
        {% for post in site.posts %}
          <li>
            <a href="{{ post.url }}">{{ post.title }}</a>
            <span style="float:right">{{ post.date | date_to_long_string }}</span>
          </li>
        {% endfor %}
      </ul>
    </div>
  </body>
</html>
