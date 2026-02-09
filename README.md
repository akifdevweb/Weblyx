<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Weblyx - Explore free interactive web projects with premium animations and responsive design.">
<meta name="keywords" content="web projects, interactive, free, black and white theme, premium design, testimonials">
<title>Weblyx - Interactive Web Projects</title>

<style>
/* ===== Reset & Body ===== */
* { margin:0; padding:0; box-sizing:border-box; font-family:'Arial',sans-serif; }
body { background:#111; color:#eee; line-height:1.6; scroll-behavior:smooth; }

/* ===== Links ===== */
a { color:#ff6600; text-decoration:none; }
a:hover { text-decoration:underline; }

/* ===== Sections ===== */
section { padding:60px 20px; opacity:0; transform:translateY(30px); animation:fadeIn 1s forwards; margin-bottom:40px; }
@keyframes fadeIn { to { opacity:1; transform:translateY(0); } }

/* ===== Hero ===== */
#hero { text-align:center; padding-top:80px; }
#hero h1 { font-size:3rem; color:#fff; margin-bottom:10px; }
#hero h2 { font-size:1.5rem; color:#ccc; margin-bottom:15px; }
#hero p { font-size:1rem; max-width:600px; margin:0 auto; color:#aaa; }

/* ===== Projects ===== */
.projects { display:grid; grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); gap:20px; }
.project-card { background:#1a1a1a; padding:25px; border-radius:12px; transition:transform 0.4s, box-shadow 0.4s; box-shadow:0 4px 12px rgba(255,255,255,0.05); }
.project-card:hover { transform:translateY(-10px); box-shadow:0 12px 30px rgba(255,255,255,0.15); }
.project-card h3 { color:#ff6600; margin-bottom:10px; font-size:1.3rem; }
.project-card p { margin-bottom:15px; font-size:0.95rem; color:#ccc; }
.project-card button { padding:10px 15px; background:#ff6600; border:none; border-radius:6px; color:#fff; cursor:pointer; transition:0.3s; font-weight:600; }
.project-card button:hover { background:#fff; color:#000; }

/* ===== Testimonials ===== */
.testimonials { display:flex; flex-direction:column; gap:20px; margin-top:20px; }
.testimonial-card { background:#1a1a1a; padding:20px; border-radius:12px; box-shadow:0 4px 12px rgba(255,255,255,0.05); }
.testimonial-card p { margin-bottom:5px; }
.testimonial-card span { font-weight:600; color:#ff6600; }

/* ===== Forms ===== */
form { display:flex; flex-direction:column; gap:10px; max-width:500px; margin-top:20px; }
input, textarea { padding:12px; border-radius:6px; border:1px solid #333; background:#111; color:#eee; width:100%; }
button.submit-btn { background:#ff6600; color:#fff; border:none; padding:12px; border-radius:6px; cursor:pointer; transition:0.3s; font-weight:600; }
button.submit-btn:hover { background:#fff; color:#000; }

/* ===== Footer ===== */
footer { text-align:center; margin:50px 0 20px; color:#aaa; font-size:0.9rem; }

/* ===== Responsive ===== */
@media(max-width:600px){ #hero h1 { font-size:2rem; } #hero h2 { font-size:1.2rem; } .project-card h3{ font-size:1.1rem; } .project-card p{ font-size:0.9rem; } }
</style>
</head>
<body>

<!-- Hero Section -->
<section id="hero">
  <h1>Weblyx</h1>
  <h2>Professional Interactive Web Projects</h2>
  <p>Explore free interactive projects with sleek animations. All projects are fully expandable and customizable for future updates.</p>
</section>

<!-- AdSense Placeholder -->
<div style="width:100%; text-align:center; margin:20px 0;">Ads will go here</div>

<!-- Projects Section -->
<section id="projects">
  <h2>Featured Projects</h2>
  <div class="projects" id="projectsContainer">
    <div class="project-card">
      <h3>Interactive Proposal</h3>
      <p>Demo of a playful proposal page with dynamic button animations.</p>
      <button onclick="alert('Opening Proposal Demo!')">Try Now</button>
    </div>
    <div class="project-card">
      <h3>Birthday Greeting</h3>
      <p>Animated birthday page that makes every greeting fun and interactive.</p>
      <button onclick="alert('Opening Birthday Demo!')">Try Now</button>
    </div>
    <div class="project-card">
      <h3>Anniversary Surprise</h3>
      <p>Creative anniversary project with premium animations and interactions.</p>
      <button onclick="alert('Opening Anniversary Demo!')">Try Now</button>
    </div>
  </div>
</section>

<!-- AdSense Placeholder -->
<div style="width:100%; text-align:center; margin:20px 0;">Ads will go here</div>

<!-- Testimonials Section -->
<section id="testimonials">
  <h2>Testimonials</h2>
  <div class="testimonials" id="testimonialContainer">
    <div class="testimonial-card">
      <p>"The Proposal page was fun and interactive!"</p>
      <span>- Alice</span>
    </div>
    <div class="testimonial-card">
      <p>"Birthday greeting project made my friend's day special!"</p>
      <span>- John</span>
    </div>
  </div>

  <h3>Add Your Testimonial</h3>
  <form id="testimonialForm">
    <input type="text" id="name" placeholder="Your Name" required>
    <textarea id="comment" rows="3" placeholder="Your Comment" required></textarea>
    <button type="submit" class="submit-btn">Submit</button>
  </form>
</section>

<!-- About Section -->
<section id="about">
  <h2>About Weblyx</h2>
  <p>Weblyx offers free interactive web projects with a professional look. You can expand with new products or demos anytime.</p>
</section>

<!-- Contact Section -->
<section id="contact">
  <h2>Contact</h2>
  <p>Reach out at <a href="mailto:contact@weblyx.com">contact@weblyx.com</a></p>
</section>

<!-- Privacy Section -->
<section id="privacy">
  <h2>Privacy Policy</h2>
  <p>We respect your privacy. Weblyx does not collect personal data beyond what is submitted via testimonials.</p>
</section>

<footer>
  &copy; 2026 Weblyx. All rights reserved.
</footer>

<script>
// Section Fade-in Delay
document.querySelectorAll('section').forEach((el,i)=>{ el.style.animationDelay=(i*0.2)+'s'; });

// JS Testimonial Submission
const form = document.getElementById('testimonialForm');
const container = document.getElementById('testimonialContainer');
form.addEventListener('submit', function(e){
  e.preventDefault();
  const name = document.getElementById('name').value;
  const comment = document.getElementById('comment').value;
  const card = document.createElement('div');
  card.className='testimonial-card';
  card.innerHTML=`<p>"${comment}"</p><span>- ${name}</span>`;
  container.appendChild(card);
  form.reset();
});
</script>

</body>
</html>
