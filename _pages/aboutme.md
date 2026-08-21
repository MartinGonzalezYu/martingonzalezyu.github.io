---
layout: page
permalink: /aboutme/
title: About me
description: Here you can get to know me a bit beyond maths
nav: true
nav_order: 3
---

<section class="about-me">
  <h2>Basic info</h2>
  <p class="intro">
    Hi! My name is Martin. I was born in 2002 and raised in Sant Cugat del Vallès, a large town about 30 minutes away from Barcelona. I speak fluent Catalan, Spanish, and English. I am also trying to learn German, and I can roughly understand French and Italian.
  </p>

  <h2>My interests</h2>
  <p class="intro">Here is a list of some of my hobbies and interests:</p>
  <ul class="intro">
    <li><strong>Food and cooking</strong>, although I cannot stand doing the dishes.</li>
    <li><strong>Sports:</strong> currently, I mostly do calisthenics and run, but I am open to anything.</li>
    <li><strong>Nature and animals,</strong> I particularly enjoy any place with a large body of fresh water to hike around and swim in.</li>
    <li><strong>Music:</strong> I like listening to almost anything and have taught myself to play the piano.</li>
  </ul>

  <h2>My trajectory</h2>
  <p class="intro">
    After finishing high school, I decided to study mathematics and physics (a very common double degree program in Spain) at UAB for two reasons: I have always liked both subjects, and I enjoy a challenge. At first, I was more interested in theoretical physics, but after getting into pure math, I had a clear preference. During my undergrad studies, I took a small detour from pure science to learn some data analysis and intern at a consulting firm in Madrid for a summer. I also did an exchange semester in Bologna, Italy, where I got to eat some great food and travel around the country.
  </p>

  <h2>Some photos</h2>
  <!---<p class="gallery-note">Click on any image to view a larger version and a short caption.</p> --->
  <div class="gallery" aria-live="polite">
    <!--
      Add your images to assets/images/aboutme/ and name them photo1.jpg, photo2.jpg, etc.
      For each .gallery-item set the data-caption attribute to the description you want shown when clicked.
      Example:
    --->
    <figure class="gallery-item" data-caption="Here I am officially receiving my scholarship to study at ETH Zürich from His Majesty King Felipe VI.">
      <img src="{{ '/assets/img/aboutme/photo2.jpg' | relative_url }}" alt="Photo 3">
    </figure>
    <figure class="gallery-item" data-caption="A photo taken during the 'la Caixa' scholarship award ceremony.">
      <img src="{{ '/assets/img/aboutme/photo3.jpg' | relative_url }}" alt="Photo 2">
    </figure>
      <figure class="gallery-item" data-caption="Not so serious graduation class photo.">
        <img src="{{ '/assets/img/aboutme/photo6.jpeg' | relative_url }}" alt="Photo 6">
      </figure>
     <figure class="gallery-item" data-caption="Went to Dublin (Ireland) to participate in the 2025 PLANCKS final with the Oppenhomies team.">
        <img src="{{ '/assets/img/aboutme/photo11.jpg' | relative_url }}" alt="Photo 11">
      </figure>
    
     <figure class="gallery-item" data-caption="From my time in Bologna.">
        <img src="{{ '/assets/img/aboutme/photo4.jpg' | relative_url }}" alt="Photo 4">
      </figure>
    <figure class="gallery-item" data-caption="From my time in Madrid.">
        <img src="{{ '/assets/img/aboutme/photo10.jpg' | relative_url }}" alt="Photo 10">
      </figure>
              <figure class="gallery-item" data-caption="Cooking a paella for my hometown's 2026 Concurs d'arrossos (rice-cooking contest).">
        <img src="{{ '/assets/img/aboutme/photo1.jpg' | relative_url }}" alt="Photo 1">
      </figure>
      <figure class="gallery-item" data-caption="Some running.">
        <img src="{{ '/assets/img/aboutme/photo7.jpg' | relative_url }}" alt="Photo 7">
      </figure>
      
      <figure class="gallery-item" data-caption="Kayaking on a lake in Catalonia.">
        <img src="{{ '/assets/img/aboutme/photo8.jpg' | relative_url }}" alt="Photo 8">
      </figure>
      <figure class="gallery-item" data-caption="Skiing in Pizol.">
        <img src="{{ '/assets/img/aboutme/photo9.jpg' | relative_url }}" alt="Photo 9">
      </figure>
      <figure class="gallery-item" data-caption="Paragliding in the Engelberg valley.">
        <img src="{{ '/assets/img/aboutme/photo12.jpg' | relative_url }}" alt="Photo 12">
      </figure>
      <figure class="gallery-item" data-caption="Hiking Tre Cime di Lavaredo in Dolomiti.">
        <img src="{{ '/assets/img/aboutme/photo13.jpg' | relative_url }}" alt="Photo 13">
      </figure>
      
      <figure class="gallery-item" data-caption="My dog.">
        <img src="{{ '/assets/img/aboutme/photo14.jpg' | relative_url }}" alt="Photo 14">
      </figure>

    <!-- Duplicate the block above for more images -->
  </div>
</section>

<!-- Modal / Lightbox -->
<div id="lightbox" class="lightbox" role="dialog" aria-modal="true" aria-hidden="true" aria-label="Image preview">
  <button id="lightbox-close" class="lightbox-close" aria-label="Close">×</button>
  <div class="lightbox-content">
    <img id="lightbox-image" src="" alt="">
    <p id="lightbox-caption"></p>
  </div>
</div>

<style>
/* Basic page spacing */
.about-me { max-width: 900px; margin: 0 auto; padding: 1.25rem; }
.intro { font-size: 1.05rem; line-height: 1.5; }

/* Responsive gallery using CSS grid */
.gallery { display: grid; grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); gap: 12px; margin-top: 1rem; }
.gallery-item { position: relative; overflow: hidden; border-radius: 8px; background: #eee; cursor: pointer; }
.gallery-item img { display: block; width: 100%; height: 100%; object-fit: cover; aspect-ratio: 4/3; transition: transform .25s ease; }
.gallery-item:hover img { transform: scale(1.05); }
.gallery-item figcaption { position: absolute; left: 0; right: 0; bottom: 0; padding: 8px 10px; background: linear-gradient(transparent, rgba(0,0,0,0.5)); color: #fff; font-size: 0.95rem; }

/* Lightbox styles */
.lightbox { display: none; position: fixed; inset: 0; background: rgba(0,0,0,0.75); align-items: center; justify-content: center; z-index: 9999; padding: 20px; }
.lightbox[aria-hidden="false"] { display: flex; }
.lightbox-content { max-width: 95%; max-height: 95%; text-align: center; color: #fff; }
.lightbox-content img { max-width: 100%; max-height: 70vh; border-radius: 6px; }
.lightbox-content p { margin-top: 0.75rem; font-size: 1rem; }
.lightbox-close { position: absolute; top: 18px; right: 20px; background: transparent; border: none; color: #fff; font-size: 2rem; line-height: 1; cursor: pointer; }
.lightbox-close:focus { outline: 2px solid #fff; }

@media (max-width: 480px) {
  .gallery { gap: 8px; }
  .gallery-item img { aspect-ratio: 3/2; }
}
</style>

<script>
document.addEventListener('DOMContentLoaded', function () {
  const lightbox = document.getElementById('lightbox');
  const lightboxImage = document.getElementById('lightbox-image');
  const lightboxCaption = document.getElementById('lightbox-caption');
  const closeBtn = document.getElementById('lightbox-close');

  function openLightbox(src, alt, caption) {
    lightboxImage.src = src;
    lightboxImage.alt = alt || '';
    lightboxCaption.textContent = caption || '';
    lightbox.setAttribute('aria-hidden', 'false');
    // prevent background from scrolling
    document.documentElement.style.overflow = 'hidden';
    closeBtn.focus();
  }

  function closeLightbox() {
    lightbox.setAttribute('aria-hidden', 'true');
    lightboxImage.src = '';
    lightboxCaption.textContent = '';
    document.documentElement.style.overflow = '';
  }

  document.querySelectorAll('.gallery-item').forEach(item => {
    item.addEventListener('click', function (e) {
      const img = item.querySelector('img');
      const src = img ? img.src : '';
      const alt = img ? img.alt : '';
      const caption = item.getAttribute('data-caption') || item.querySelector('figcaption')?.textContent || '';
      openLightbox(src, alt, caption);
    });

    // make gallery items keyboard accessible
    item.tabIndex = 0;
    item.addEventListener('keydown', function (e) {
      if (e.key === 'Enter' || e.key === ' ') {
        e.preventDefault();
        item.click();
      }
    });
  });

  closeBtn.addEventListener('click', closeLightbox);
  lightbox.addEventListener('click', function (e) {
    if (e.target === lightbox) closeLightbox();
  });
  document.addEventListener('keydown', function (e) {
    if (e.key === 'Escape' && lightbox.getAttribute('aria-hidden') === 'false') closeLightbox();
  });
});
</script>

