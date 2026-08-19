---
layout: page
permalink: /aboutme/
title: About me
description: Some information about me together with related photos.  
nav: true
nav_order: 3
---

<section class="about-me">
  <h1>About me</h1>
  <p class="intro">Hello — I'm Martin. This page is a short bio and a gallery where I share photos and short stories. Replace this paragraph with a brief description about yourself: who you are, what you do, and what you enjoy.</p>

  <h2>Gallery</h2>
  <p class="gallery-note">Click on any image to view a larger version and a short caption.</p>

  <div class="gallery" aria-live="polite">
    <!--
      Add your images to assets/images/aboutme/ and name them photo1.jpg, photo2.jpg, etc.
      For each .gallery-item set the data-caption attribute to the description you want shown when clicked.
      Example:
    --->
        <figure class="gallery-item" data-caption="A relaxing day hiking in the mountains.">
          <img src="{{ '/assets/images/aboutme/photo1.jpg' | relative_url }}" alt="Hiking in mountains">
          <figcaption>Hiking</figcaption>
        </figure>
    <figure class="gallery-item" data-caption="Describe this photo here.">
      <img src="{{ '/assets/images/aboutme/photo2.jpg' | relative_url }}" alt="Photo 1">
      <figcaption>Photo 2</figcaption>
    </figure>
    <figure class="gallery-item" data-caption="Describe this photo here.">
      <img src="{{ '/assets/images/aboutme/photo3.jpg' | relative_url }}" alt="Photo 2">
      <figcaption>Photo 3</figcaption>
    </figure>

    <figure class="gallery-item" data-caption="Describe this photo here.">
      <img src="{{ '/assets/images/aboutme/photo3.jpg' | relative_url }}" alt="Photo 3">
      <figcaption>Photo 3</figcaption>
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

<!-- cooking, sports, nature, food, piano, languages -->
