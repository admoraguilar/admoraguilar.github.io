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
  <header>
    <h2>Unity Developer</h2>
    <p>
      <a href="https://dm-ed.com/" target="_blank">David Morgan Education</a> | Oxford, United Kingdom <br/> 2018 - Present <br>
    </p>
  </header>
  <blockquote>
    Working closely with the development team to create a platform that could teach people to read through various mini-games.
  </blockquote>
  <p>
    <ul>
      <li>Creation of different games from scratch using Unity.</li>
      <li>Creation of crucial in-house tools that are helpful for designers and programmers alike.</li>
      <li>Performance optimization so the app can run smoothly on Web and Mobile.</li>
      <li>Reports directly to the Lead Developer and the CEO.</li>
    </ul>
  </p>


  <header>
    <h2>Lead Technical Developer</h2>
    <p>
      <a href="https://youtu.be/2NAbet0IDD4" target="_blank">MyHomespace Inc.</a> | Manila, Philippines <br/> 2017 - 2018
    </p>
  </header>
  <blockquote>
    Spearheaded the whole development process of creating a 3D online social media app. Reports directly to the Chairman and CEO.
  </blockquote>
  <p>
    <ul>
      <li>Responsible for the creation from scratch to release of its flagship product “Project A” which is a 3D online social mobile app like AltSpaceVR and VRChat. Prototype took 1 month to make. Polish and product changes extended it to 5 months.</li>
      <li>Implemented online connectivity such as full 3D environment navigation, voice chat, user account creation, etc.</li>
      <li>Heavily optimized the app in order for it to work even on low-end iOS and ANDROID hardware.</li>
      <li>Overlooked and taught interns about game development concepts with different skill sets: Art, Programming, Audio, etc.</li>
      <li>Overlooked the creation of assets used in the app: graphics, audio, etc. to make sure that they were game-ready before plugging them in.</li>
    </ul>
  </p>


  <header>
    <h2>Technical Developer Intern</h2>
    <p>
      <a href="https://secret6.com/" target="_blank">Secret 6</a> | Pasig, Philippines <br/> 2017
    </p>
  </header>
  <p>
    <ul>
      <li>Worked with a team for an unannounced project that's to be deployed on MOBILE platforms.</li>
      <li>Implemented GAMEPLAY, UI, OPTIMIZATIONS, and UX using UNITY.</li>
      <li>Worked closely with the team to put up features as FAST and without compromising on quality as possible.</li>
    </ul>
  </p>
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

</section>