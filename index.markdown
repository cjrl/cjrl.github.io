---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

---

# About Me

I am a Mathematician at the [Federal Aviation Administration](https://www.faa.gov/) (FAA), where I develop mathematical and computational solutions to optimize the efficiency and predictability of national airspace operations. I design high-performance algorithms and machine learning systems that operate on large-scale, near-real-time flight data, enabling system-wide performance monitoring across the United States airspace.  

My work combines predictive modeling, statistical inference, geospatial analysis, and distributed computation. I have built scalable algorithms and data pipelines capable of processing millions of flight trajectories, leveraging high-performance computing environments to deliver actionable insights for air traffic operations.  

I received my Ph.D. in Mathematics from the University of Virginia in 2021, where I specialized in algebraic topology under [Professor Nicholas Kuhn](https://uva.theopenscholar.com/nick-kuhn). My dissertation, [Applications of Chromatic Fixed Point Theory](https://doi.org/10.18130/3h64-wv15), involved designing algorithms for high-performance computing clusters to solve complex abstract problems in algebraic topology. 

# Talks

<style>
.timeline {
  position: relative;
  margin: 2rem auto;
  padding: 0;
  max-width: 700px;
  list-style: none;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 20px;
  top: 0;
  bottom: 0;
  width: 3px;
  background: #e0e0e0;
}

.timeline-item {
  position: relative;
  margin: 2rem 0;
  padding-left: 60px;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: 11px;
  top: 0.6em;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background: #4a90e2;
}

.timeline-content {
  background: #fff;
  padding: 1rem 1.5rem;
  border-radius: 0.75rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.timeline-content h3 {
  margin: 0 0 0.5rem;
  font-size: 1.1rem;
}

.timeline-content small {
  color: #666;
  font-size: 0.9rem;
  display: block;
  margin-bottom: 0.5rem;
}

.timeline-content img {
  max-width: 100%;
  border-radius: 0.5rem;
  margin-top: 0.5rem;
  transition: transform 0.2s ease-in-out;
}

.timeline-content img:hover {
  transform: scale(1.02);
}
</style>

<ul class="timeline">
  {% for post in site.posts %}
    {% if post.categories contains "talk" %}
      <li class="timeline-item">
        <div class="timeline-content">
          <h3>{{ post.title }}</h3>
          <small>{{ post.date | date: "%B %d, %Y" }}</small>

          {% if post.video-link %}
            {% assign yt_id = post.video-link | split: "v=" | last | split: "&" | first %}
            <a href="{{ post.video-link }}" target="_blank">
              <img src="https://img.youtube.com/vi/{{ yt_id }}/hqdefault.jpg" alt="Talk video thumbnail">
            </a>
          {% endif %}
        </div>
      </li>
    {% endif %}
  {% endfor %}
</ul>
    
# Papers

## Machine Learning in Aviation

<style>
.timeline {
  position: relative;
  margin: 2rem auto;
  padding: 0;
  max-width: 700px;
  list-style: none;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 20px;
  top: 0;
  bottom: 0;
  width: 3px;
  background: #e0e0e0;
}

.timeline-item {
  position: relative;
  margin: 2rem 0;
  padding-left: 60px;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: 11px;
  top: 0.6em;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background: #4a90e2;
}

.timeline-content {
  background: #fff;
  padding: 1rem 1.5rem;
  border-radius: 0.75rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.timeline-content h3 {
  margin: 0 0 0.5rem;
  font-size: 1.1rem;
}

.timeline-content small {
  color: #666;
  font-size: 0.9rem;
  display: block;
  margin-bottom: 0.25rem;
}

.timeline-meta {
  margin-top: 0.5rem;
  font-size: 0.9rem;
  color: #444;
}

.timeline-meta a {
  margin-right: 1rem;
  color: #4a90e2;
  text-decoration: none;
}

.timeline-meta a:hover {
  text-decoration: underline;
}
</style>


<ul class="timeline">
  {% for post in site.posts %}
    {% if post.categories contains "aviation" %}
      <li class="timeline-item">
        <div class="timeline-content">
          <h3>
            <a href="{{post.main-link}}">{{post.title}}</a>
          </h3>
          
          <small>
            {% if post.show-date %}
              {{post.date | date: "%B %d, %Y"}}
            {% else %}
              ({{post.date | date: '%Y'}})
            {% endif %}
            
            {% if post.coauthors %}
              — with
              {% assign n = post.coauthors | size %}
              {% if n > 1 %}
                {% assign first = post.coauthors | first %}
                {{ first.name }} et al.
              {% else %}
                {{ post.coauthors[0].name }}
              {% endif %}
            {% endif %}
          </small>

          {% if post.conference %}
            <div class="timeline-meta">
              <em>{{ post.conference }}</em>
              {% if post.session %}
                — {{ post.session }}
              {% endif %}
            </div>
          {% endif %}

          <div class="timeline-meta">
            {% if post.doi %}
              <a href="{{post.doi}}" target="_blank">DOI</a>
            {% endif %}
            
            {% if post.link %}
              <a href="{{post.link}}" target="_blank">Publisher Link</a>
            {% endif %}
          </div>
        </div>
      </li>
    {% endif %}
  {% endfor %}
</ul>

<br/>
## Algebraic Topology 

<style>
.timeline {
  position: relative;
  margin: 2rem auto;
  padding: 0;
  max-width: 700px;
  list-style: none;
}

.timeline::before {
  content: '';
  position: absolute;
  left: 20px;
  top: 0;
  bottom: 0;
  width: 3px;
  background: #e0e0e0;
}

.timeline-item {
  position: relative;
  margin: 2rem 0;
  padding-left: 60px;
}

.timeline-item::before {
  content: '';
  position: absolute;
  left: 11px;
  top: 0.6em;
  width: 18px;
  height: 18px;
  border-radius: 50%;
  background: #4a90e2;
}

.timeline-content {
  background: #fff;
  padding: 1rem 1.5rem;
  border-radius: 0.75rem;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
}

.timeline-content h3 {
  margin: 0 0 0.5rem;
  font-size: 1.1rem;
}

.timeline-content small {
  color: #666;
  font-size: 0.9rem;
  display: block;
  margin-bottom: 0.25rem;
}

.timeline-meta {
  margin-top: 0.5rem;
  font-size: 0.9rem;
  color: #444;
}

.timeline-meta a {
  margin-right: 1rem;
  color: #4a90e2;
  text-decoration: none;
}

.timeline-meta a:hover {
  text-decoration: underline;
}
</style>


<ul class="timeline">
  {% for post in site.posts %}
    {% if post.categories contains "paper" %}
      <li class="timeline-item">
        <div class="timeline-content">
          <h3>
            <a href="{{post.main-link}}">{{post.title}}</a>
          </h3>
          
          <small>
            {% if post.show-date %}
              {{post.date | date: "%B %d, %Y"}}
            {% else %}
              ({{post.date | date: '%Y'}})
            {% endif %}
            
            {% if post.coauthors %}
              — with
              {% for coa in post.coauthors %}
                {% if coa.noweb != true %}
                  <a href="{{coa.web}}">{{coa.name}}</a>
                {% else %}
                  {{coa.name}}
                {% endif %}
                {% unless forloop.last %}, {% endunless %}
              {% endfor %}
            {% endif %}
          </small>
          
          {% if post.journal %}
            <div class="timeline-meta">
              <em>{{ post.journal }}</em>
            </div>
          {% endif %}

          <div class="timeline-meta">
            {% if post.arXiv %}
              <a href="https://arxiv.org/abs/{{post.arXiv | split: ' ' | first}}" target="_blank">
                arXiv:{{post.arXiv}}
              </a>
            {% endif %}
            
            {% if post.doi %}
              <a href="{{post.doi}}" target="_blank">DOI</a>
            {% endif %}
            
            {% if post.open-access %}
              <a href="{{post.open-access}}" target="_blank">Open Access</a>
            {% endif %}
          </div>
        </div>
      </li>
    {% endif %}
  {% endfor %}
</ul>

<!-- 
** Papers 
   - Kuhn, Nicholas J., and Christopher JR Lloyd. "Computing the Morava K–theory of real Grassmannians using chromatic fixed point theory." /Algebraic & Geometric Topology/ 24, no. 2 (2024): 919-950. [[https://doi.org/10.2140/agt.2024.24.919][https://doi.org/10.2140/agt.2024.24.919]]. [[https://msp.org/agt/2024/24-2/agt-v24-n2-p07-s.pdf][Open access]].
** Ten Minute Research Summary
#+BEGIN_EXPORT html
   <iframe width="640" height="385" src="https://www.youtube.com/embed/yXYueCOpgd4" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe><br/><br/>
#+END_EXPORT
** Recent Talks
   - 06/08/2023 - [[https://arc.aiaa.org/doi/abs/10.2514/6.2023-4213][AIAA Operationalizing Machine Learning Models for Strategic Planning]]
   - 08/09/2021 - [[https://folk.ntnu.no/drewkh/conf.html][Transchromatic homotopy online conference]]
   - 01/05/2021 - [[https://www.math.northwestern.edu/events/seminars/?group=ToSe][Chicago-Northwestern Topology Seminar]]
   - 12/04/2020 - [[https://math.virginia.edu/seminars/gradsem/][UVA Graduate Seminar]] --- Version controlling your
     thesis with Git ([[https://raw.githubusercontent.com/cjl8zf/uva-grad-sem-git-guide/master/uva_grad_sem_git_guide.pdf][handout)]]
   - 11/06/2020 - [[https://www.sas.rochester.edu/mth/news-events/events/topology-seminars.html][University of Rochester Topology Seminar]]
   - 11/03/2020 - University of Illinois Urbana-Champaign Homotopy Theory Seminar
   - 10/19/2020 - [[https://math.jhu.edu/~vzakhar2/topology-seminar/][Johns Hopkins Topology Seminar]]
   - 09/24/2020 - [[https://math.virginia.edu/seminars/topology/][University of Virginia Topology Seminar]]
** Engagement 
*** Career Panels
   - 03/01/2024 - UVA Graduate Seminar - Transitioning from Academia to Industry
   - 06/29/2023 - Jepson Summer Science - Academia and Industry Panel
   - 03/20/2019 - UMW Math Department Career Night - Applying to Math
     Grad School

*** Directed Reading Program
    Starting in Fall 2018 I have worked closely with [[https://sites.google.com/view/sara-maloni][Professor Sara Maloni]]
    to organize the University of Virginia chapter of the [[https://math.virginia.edu/drp/][Directed
    Reading Program]]. This program pairs advanced undergraduates with
    graduate student mentors to explore an area of math not typically
    covered in the undergraduate curriculum. This program is very
    important to me which is why I have taken on the following roles:
    - Graduate committee chair
    - Webmaster 
    - Mentor
     
*** Research Experience for Undergraduates 
    
    In the Summer of 2020 I participated as a mentor in the University
    of Virginia Topology and Geometry REU. I worked under the
    direction of [[https://sites.google.com/view/julie-bergner/][Professor Julie Bergner]] with fellow graduate student
    [[https://sites.google.com/view/rossakhmechet][Ross Akhmechet]] to assist the undergraduate researchers as they
    explored the feasibility of a TQFT theory for embedded
    cobordisms that could detect knottings. 
    
*** Teaching Mentor 
    As a 5th year graduate student I have had the opportunity to teach
    a variety of classes at the university level, however not so many
    that I no longer remember what it was like to be a first time
    instructor. For this reason I was very pleased to accept the
    invitation from [[https://uva.theopenscholar.com/paul-bourdon][Professor Paul Bourdon]] to be a teaching mentor for
    a second year graduate student in Fall 2020.
    
** Teaching
*** University of Virginia
  - Spring 2021 :: Instructor of record for an uncoordinated section of Math 1140 --- Financial Mathematics 
  - Fall 2019 :: Instructor of record for an uncoordinated section of Math 1140 --- Financial Mathematics 
  - Fall 2018 :: Instructor of record for an uncoordinated section of Math 1140 --- Financial Mathematics 
  - Spring 2018 :: Instructor of record for one section of Math 1220 --- A Survey of Calculus II 
  - Fall 2017 :: Instructor of record for one section of Math 1210 --- A Survey of Calculus I 
  - Spring 2017 :: Teaching Assistant for two sections of Math 3250 --- Ordinary Differential Equations 
  - Fall 2016  :: Teaching Assistant for two sections of Math 3250 ---
    Ordinary Differential Equations
*** University of Mary Washington
  - Spring 2016 :: Teaching Assistant for Math 201 --- Introduction to Discrete Mathematics 
** This Website

   You can view the source of this website [[https://github.com/cjl8zf/cjl8zf.github.io][here]]. It is written in the
   org mark-up language inside of the Emacs text editor (which I live in).
   
    -->
