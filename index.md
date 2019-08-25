---
layout: home
sitemap:
    priority: 0.7
    lastmod: 2019-08-25
    changefreq: monthly
---

<section>
  <!-- WELCOME -->
  <header class="major" id="unityeditortools">
	  <h1>Unity Editor Tools</h1>
    <p>
      Useful editor tools for designers, artists, and programmers-alike.
    </p>
  </header>
  <div class="box alt">
    <div class="row 50% uniform">
      {% for unity_editor_tools in site.data.profile.unity_editor_tools %}
        <div class="4u">
          <span class="image fit">
            <a href="{{ unity_editor_tools.image_path | absolute_url }}" title="{{ unity_editor_tools.name }}">
              <img src="{{ unity_editor_tools.image_path | absolute_url }}" alt="{{ filename }}" title="" />
              <p> {{ unity_editor_tools.name }} </p>
            </a>
          </span>
        </div>
      {% endfor%}
    </div>
  </div>
  <hr/>

  <!-- EXPERIENCE -->
  <header class="major" id="experience">
	  <h1>Experience</h1>
  </header>
  {% for experience in site.data.profile.experiences %}
    <header>
      <span class="image right">
        <img src="{{experience.company_logo | absolute_url }}">
      </span>
      <h2>{{experience.title}}</h2>
      <p>
        <a href="{{experience.company_website}}" target="_blank">{{experience.company}}</a> | {{experience.location}} <br/> {{experience.duration}} <br>
      </p>
    </header>
    {% if experience.header != "" %}
      <blockquote>
        {{experience.header}}
      </blockquote>
    {% endif %}
    <p>
      <ul>
        {% for description in experience.descriptions %}
          <li>{{description}}</li>
        {% endfor %}
      </ul>
    </p>
  {% endfor %}
  <hr/>

  <!-- INTERLUDE -->
  <header class="major" id="interlude">
    <h1>{{site.data.profile.interlude_header}}</h1>
    <p>{{site.data.profile.interlude_body}}</p>
  </header>
  <div class="row">
    {% for skill in site.data.profile.skills %}
      <div class="6u 12u$(small)">
        <header>
          <i class="fa {{skill.fontawesome_icon}} fa-4x"></i>
          <h3>{{skill.header}}</h3>
          <p>{{skill.body}}</p>
        </header>
        <ul>
          {% for description in skill.descriptions %}
            <li>{{description}}</li>
          {% endfor %}
        </ul>
         <p>
          {% if skill.additional_info != "" %}
            {{skill.additional_info}}
          {% endif %}
         </p>
      </div>
    {% endfor %}
  </div>
  <hr/>

  <!-- PROJECTS -->
  <header class="major" id="projects">
    <h1>Projects</h1>
  </header>
  {% for project in site.data.profile.projects %}
    <header>
      <header>
        {% assign youtube_id = project.youtube_id %}
        {% include youtube-embed.html id=youtube_id %}
        <p>{{project.youtube.id}}</p>
        <h2>{{ project.name }}</h2>
        <p>{{ project.duration }}</p>
      </header>
      {% if project.header != "" %}
        <blockquote> {{ project.header }} </blockquote>
      {% endif %}
      <p>
        <ul>
          {% for description in project.descriptions %}
            <li>{{ description }}</li>
          {% endfor %}
        </ul>
      </p>
      <ul class="actions fit">
        {% for link in project.links %}
            <li><a href="{{link.url}}" class="button special fit center" target="_blank">{{link.name}}</a></li>
        {% endfor %}  
      </ul>
    </header>
  {% endfor %}
  <hr/>

  <!-- EDUCATION -->
  <header class="major" id="education">
    <h1>Education</h1>
  </header>
  <header>
    <span class="image right">
      <img src="{{ "images/education/DLS-CSB.png" | absolute_url }}">
    </span>
    <h2>Bachelor of Science in Information Technology
  with Specialization in Game Design and Development</h2>
    <p>
      <a href="http://benilde.edu.ph/" target="_blank">De La Salle College of Saint Benilde</a> <br> 2013-2017
    </p>
  </header>
  <p>
    <ul>
      <li>Honorable mention graduate, Dean’s lister.</li>
      <li>Attended UNITY, and UNREAL seminars with speakers coming directly from UNITY TECHNOLOGIES, and EPIC GAMES</li>
      <li>Projects that I've been involved with are usually used to represent the school's program across the country and worldwide. Events such as Electronic Sports and Game Summit, GameOn!, ToyCon, etc.</li>
    </ul>
  </p>
  <hr/>

  <!-- MORE PROJECTS -->
  <header class="major" id="moreprojects">
    <h1>More Projects</h1>
  </header>
  {% for project in site.data.profile.more_projects %}
    <header>
      <header>
        {% assign youtube_id = project.youtube_id %}
        {% include youtube-embed.html id=youtube_id %}
        <p>{{project.youtube.id}}</p>
        <h2>{{ project.name }}</h2>
        <p>{{ project.duration }}</p>
      </header>
      {% if project.header != "" %}
        <blockquote> {{ project.header }} </blockquote>
      {% endif %}
      <p>
        <ul>
          {% for description in project.descriptions %}
            <li>{{ description }}</li>
          {% endfor %}
        </ul>
      </p>
      <ul class="actions fit">
        {% for link in project.links %}
            <li><a href="{{link.url}}" class="button special fit center" target="_blank">{{link.name}}</a></li>
        {% endfor %}  
      </ul>
    </header>
  {% endfor %}
  <hr/>

  <header class="major" id="thankyou">
    <h1>Thank You</h1>
    <p>{{site.data.profile.thank_you_message}}</p>
  </header>

</section>