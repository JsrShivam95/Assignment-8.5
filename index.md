        HTML 

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Assignment 8.5 — CSS Grid Mini-Project | Luminary Gallery</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>

  <!-- ================= RULE 1 & 3: GRID CONTAINER WITH NAMED AREAS ================= -->
  <div class="site-grid">

    <!-- Header Area -->
    <header class="site-header">
      <div class="header-inner">
        <a href="#" class="logo">LUMINARY<span>.</span></a>
        <nav class="header-nav">
          <a href="#featured">Featured</a>
          <a href="#collections">Collections</a>
          <a href="#curators">Curators</a>
        </nav>
      </div>
    </header>

    <!-- Main Content Area -->
    <main class="site-main">
      <div class="main-heading">
        <span class="eyebrow">Autumn 2026 Collection</span>
        <h1>Curated Natural Perspectives</h1>
        <p>A responsive visual portfolio exploring terrestrial light, topography, and geometry.</p>
      </div>

      <!-- ================= RULES 2, 3 & 4: MAIN PHOTO GRID ================= -->
      <section class="gallery-grid" id="featured">

        <!-- Card 1: Featured Hero Card (Explicit Placement - Spans 2 Cols & 2 Rows) -->
        <article class="gallery-card card-featured">
          <div class="image-wrapper">
            <img 
              src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?w=1000&auto=format&fit=crop&q=80" 
              alt="Yosemite valley mist reflecting on water"
              loading="lazy"
            >
          </div>
          <div class="card-caption">
            <span class="tag">Editor's Choice</span>
            <h2>Yosemite Alpine Mist</h2>
            <p>Glacial peaks catching golden morning reflections across mirror waters.</p>
          </div>
        </article>

        <!-- Card 2: Standard Card -->
        <article class="gallery-card">
          <div class="image-wrapper">
            <img 
              src="https://images.unsplash.com/photo-1470071459604-3b5ec3a7fe05?w=700&auto=format&fit=crop&q=80" 
              alt="Misty mountain ridges"
              loading="lazy"
            >
          </div>
          <div class="card-caption">
            <span class="tag">Atmosphere</span>
            <h2>Cloud Inversion</h2>
            <p>Layered ridge elevations piercing high altitude cloud decks.</p>
          </div>
        </article>

        <!-- Card 3: Standard Card -->
        <article class="gallery-card">
          <div class="image-wrapper">
            <img 
              src="https://images.unsplash.com/photo-1441974231531-c6227db76b6e?w=700&auto=format&fit=crop&q=80" 
              alt="Dense pine forest with sunbeams"
              loading="lazy"
            >
          </div>
          <div class="card-caption">
            <span class="tag">Wilderness</span>
            <h2>Ancient Canopy</h2>
            <p>Morning light breaking through primeval forest canopies.</p>
          </div>
        </article>

        <!-- Card 4: Tall Portrait Card (Explicit Placement - Spans 2 Rows) -->
        <article class="gallery-card card-tall">
          <div class="image-wrapper">
            <img 
              src="https://images.unsplash.com/photo-1469474968028-56623f02e42e?w=700&auto=format&fit=crop&q=80" 
              alt="Valley vista at dusk"
              loading="lazy"
            >
          </div>
          <div class="card-caption">
            <span class="tag">Topography</span>
            <h2>Highland Basin</h2>
            <p>Undulating ridges exposed to high alpine wind systems.</p>
          </div>
        </article>

        <!-- Card 5: Standard Card -->
        <article class="gallery-card">
          <div class="image-wrapper">
            <img 
              src="https://images.unsplash.com/photo-1426604966848-d7adac402bff?w=700&auto=format&fit=crop&q=80" 
              alt="Granite mountain face above stream"
              loading="lazy"
            >
          </div>
          <div class="card-caption">
            <span class="tag">Geology</span>
            <h2>Granite Monolith</h2>
            <p>Weathered sedimentary crags rising above seasonal creek beds.</p>
          </div>
        </article>

        <!-- Card 6: Wide Card (Explicit Placement - Spans 2 Cols) -->
        <article class="gallery-card card-wide">
          <div class="image-wrapper">
            <img 
              src="https://images.unsplash.com/photo-1472214103451-9374bd1c798e?w=900&auto=format&fit=crop&q=80" 
              alt="Golden rolling agricultural hills"
              loading="lazy"
            >
          </div>
          <div class="card-caption">
            <span class="tag">Rural</span>
            <h2>Golden Horizon</h2>
            <p>Panoramic warm sundown settling over western grassland acreage.</p>
          </div>
        </article>

      </section>
    </main>

    <!-- Sidebar Area -->
    <aside class="site-aside" id="curators">
      <div class="aside-block">
        <h3>Exhibition Details</h3>
        <ul class="meta-list">
          <li><strong>Curator:</strong> Elena Rostova</li>
          <li><strong>Images:</strong> 6 Selections</li>
          <li><strong>Resolution:</strong> Ultra HD Master</li>
          <li><strong>Color Space:</strong> Display P3</li>
        </ul>
      </div>

      <div class="aside-block callout">
        <h3>Submit Work</h3>
        <p>Photographers shooting environmental realism are invited to submit collections for the next seasonal publication.</p>
        <button class="aside-btn" type="button">Submission Portal →</button>
      </div>
    </aside>

    <!-- Footer Area -->
    <footer class="site-footer">
      <div class="footer-inner">
        <p>&copy; 2026 Luminary Photographic Archive. All works copyrighted by respective creators.</p>
        <div class="footer-links">
          <a href="#">License</a>
          <a href="#">Privacy</a>
          <a href="#">RSS Feed</a>
        </div>
      </div>
    </footer>

  </div>

</body>
</html>


              CSS

/* --- Global Reset & Variables --- */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --bg-body: #090d16;
  --bg-surface: #111827;
  --bg-card: #1f2937;
  --accent: #38bdf8;
  --accent-hover: #0284c7;
  --text-main: #f9fafb;
  --text-muted: #9ca3af;
  --border: #374151;
  --gap: 1.75rem;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  background-color: var(--bg-body);
  color: var(--text-main);
  line-height: 1.5;
  min-height: 100vh;
}

/* ================= RULE 1 & 3: PRIMARY PAGE GRID WITH NAMED AREAS ================= */
.site-grid {
  display: grid;
  min-height: 100vh;
  gap: var(--gap);
  padding: 1.5rem;
  max-width: 1440px;
  margin: 0 auto;

  /* Rule 2: Using fr units */
  grid-template-columns: 1fr 300px;
  grid-template-rows: auto 1fr auto;

  /* Rule 3: Named layout areas */
  grid-template-areas:
    "header header"
    "main   aside"
    "footer footer";
}

/* --- Area: Header --- */
.site-header {
  grid-area: header;
  background-color: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 1rem 2rem;
}

.header-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-size: 1.4rem;
  font-weight: 900;
  letter-spacing: 0.1em;
  color: var(--text-main);
  text-decoration: none;
}

.logo span {
  color: var(--accent);
}

.header-nav {
  display: flex;
  gap: 1.75rem;
}

.header-nav a {
  color: var(--text-muted);
  text-decoration: none;
  font-size: 0.95rem;
  font-weight: 500;
  transition: color 0.2s ease;
}

.header-nav a:hover {
  color: var(--accent);
}

/* --- Area: Main --- */
.site-main {
  grid-area: main;
  min-width: 0;                      /* Rule 4: Critical to prevent grid child overflow */
}

.main-heading {
  margin-bottom: 2rem;
}

.eyebrow {
  display: inline-block;
  font-size: 0.75rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--accent);
  margin-bottom: 0.5rem;
}

.main-heading h1 {
  font-size: 2.25rem;
  font-weight: 800;
  letter-spacing: -0.02em;
}

.main-heading p {
  color: var(--text-muted);
  margin-top: 0.4rem;
  font-size: 1rem;
}

/* ================= RULE 2, 3 & 4: INNER PHOTO GRID ================= */
.gallery-grid {
  display: grid;
  /* Rule 2: repeat(), minmax(), and fr units */
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: var(--gap);
  grid-auto-flow: dense;             /* Fills empty holes left by larger spans */
}

.gallery-card {
  background-color: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: 12px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: transform 0.25s ease, border-color 0.25s ease;
  min-width: 0;                      /* Rule 4: Prevents text-overflow from pushing grid */
}

.gallery-card:hover {
  transform: translateY(-4px);
  border-color: var(--accent);
}

/* Rule 3: Explicit Grid Placement (Spanning Rows & Columns) */
.card-featured {
  grid-column: span 2;
  grid-row: span 2;
}

.card-tall {
  grid-row: span 2;
}

.card-wide {
  grid-column: span 2;
}

/* Image Wrapper & Overflow Prevention (Rule 4) */
.image-wrapper {
  position: relative;
  width: 100%;
  height: 240px;
  overflow: hidden;
  background-color: #1e293b;
}

/* Dynamically adjust image heights for spanned cards */
.card-featured .image-wrapper {
  height: 380px;
}

.card-tall .image-wrapper {
  height: 380px;
}

.image-wrapper img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  display: block;
  transition: transform 0.4s ease;
}

.gallery-card:hover .image-wrapper img {
  transform: scale(1.04);
}

.card-caption {
  padding: 1.25rem;
  display: flex;
  flex-direction: column;
  flex-grow: 1;
}

.tag {
  font-size: 0.7rem;
  font-weight: 700;
  text-transform: uppercase;
  color: var(--accent);
  letter-spacing: 0.05em;
  margin-bottom: 0.35rem;
}

.card-caption h2 {
  font-size: 1.15rem;
  font-weight: 700;
  color: var(--text-main);
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;           /* Rule 4: Text overflow prevention */
}

.card-caption p {
  color: var(--text-muted);
  font-size: 0.875rem;
  margin-top: 0.35rem;
  line-height: 1.4;
}

/* --- Area: Aside --- */
.site-aside {
  grid-area: aside;
  display: flex;
  flex-direction: column;
  gap: var(--gap);
}

.aside-block {
  background-color: var(--bg-surface);
  border: 1px solid var(--border);
  border-radius: 12px;
  padding: 1.5rem;
}

.aside-block h3 {
  font-size: 1rem;
  font-weight: 700;
  margin-bottom: 1rem;
  border-bottom: 1px solid var(--border);
  padding-bottom: 0.5rem;
}

.meta-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 0.65rem;
  font-size: 0.875rem;
  color: var(--text-muted);
}

.meta-list strong {
  color: var(--text-main);
}

.callout {
  background: linear-gradient(145deg, #111827 0%, #1e293b 100%);
}

.callout p {
  font-size: 0.875rem;
  color: var(--text-muted);
  margin-bottom: 1.25rem;
}

.aside-btn {
  width: 100%;
  padding: 0.75rem;
  background-color: var(--accent);
  color: #090d16;
  border: none;
  border-radius: 6px;
  font-weight: 700;
  font-size: 0.85rem;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.aside-btn:hover {
  background-color: var(--accent-hover);
  color: #ffffff;
}

/* --- Area: Footer --- */
.site-footer {
  grid-area: footer;
  border-top: 1px solid var(--border);
  padding-top: 1.5rem;
}

.footer-inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.85rem;
  color: var(--text-muted);
}

.footer-links {
  display: flex;
  gap: 1.5rem;
}

.footer-links a {
  color: var(--text-muted);
  text-decoration: none;
  transition: color 0.2s ease;
}

.footer-links a:hover {
  color: var(--text-main);
}

/* ================= RULE 5: RESPONSIVE VIEWPORT TESTING ================= */

/* Tablet Viewport (Max 1024px) */
@media (max-width: 1024px) {
  .site-grid {
    grid-template-columns: 1fr;
    grid-template-areas:
      "header"
      "main"
      "aside"
      "footer";
  }

  .gallery-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .card-featured {
    grid-column: span 2;
    grid-row: span 1;
  }

  .card-tall {
    grid-row: span 1;
  }

  .card-wide {
    grid-column: span 2;
  }
}

/* Mobile Viewport (Max 640px) */
@media (max-width: 640px) {
  .site-grid {
    padding: 1rem;
    gap: 1rem;
  }

  .gallery-grid {
    grid-template-columns: 1fr;       /* Single column stack */
  }

  .card-featured,
  .card-wide {
    grid-column: span 1;
    grid-row: span 1;
  }

  .card-featured .image-wrapper,
  .card-tall .image-wrapper {
    height: 240px;
  }

  .footer-inner {
    flex-direction: column;
    gap: 1rem;
    text-align: center;
  }
}