/*
  Stylesheet for the modernized Le Chamois website.
  The palette is inspired by the warmth of melted cheese and rustic wood,
  pairing golden hues with earthy browns and a clean, light background.
*/

/* CSS variables for easy theme adjustments */
:root {
  --primary-color: #b96e0b; /* warm amber reminiscent of cheese */
  --secondary-color: #4b2e20; /* deep brown for contrast */
  --light-background: #f9f5f0;
  --text-color: #2c2c2c;
  --heading-font: 'Playfair Display', serif;
  --body-font: 'Montserrat', sans-serif;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: var(--body-font);
  color: var(--text-color);
  background: var(--light-background);
  line-height: 1.6;
}

/* Navigation */
header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.9);
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  z-index: 1000;
}

.navbar {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0.5rem 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.navbar .brand {
  font-family: var(--heading-font);
  font-weight: 600;
  font-size: 1.5rem;
  color: var(--secondary-color);
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 1.5rem;
}

.nav-links li a {
  text-decoration: none;
  color: var(--secondary-color);
  font-weight: 500;
  transition: color 0.2s ease;
}

.nav-links li a:hover {
  color: var(--primary-color);
}

/* Hero section */
.hero {
  height: 90vh;
  background-image: url('hero.jpg');
  background-size: cover;
  background-position: center;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.45);
  z-index: 1;
}

.hero-content {
  position: relative;
  z-index: 2;
  color: #ffffff;
  max-width: 700px;
  padding: 0 1rem;
}

.hero-content h1 {
  font-family: var(--heading-font);
  font-size: 3rem;
  margin-bottom: 0.5rem;
}

.hero-content p {
  font-size: 1.2rem;
  margin-bottom: 1.5rem;
}

.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border-radius: 25px;
  text-decoration: none;
  font-weight: 600;
  transition: background 0.2s ease;
}

.btn-primary {
  background: var(--primary-color);
  color: #fff;
}

.btn-primary:hover {
  background: var(--secondary-color);
}

/* Generic sections */
/* Sections are padded evenly and include scroll-margin to accommodate the fixed navigation bar.
   The scroll-margin-top property ensures that section headings are not hidden behind
   the fixed header when navigating via anchor links. */
.section {
  padding: 4rem 1rem;
  max-width: 1200px;
  margin: 0 auto;
  position: relative;
  scroll-margin-top: 100px;
}

.section h2 {
  font-family: var(--heading-font);
  font-size: 2rem;
  margin-bottom: 1.5rem;
  color: var(--secondary-color);
}

/* About section */
.about p {
  max-width: 800px;
  margin: 0 auto;
  font-size: 1.1rem;
  text-align: center;
}

/* Increase spacing above the about section heading so it clears the fixed header */
#about {
  padding-top: 6rem;
}

/* Menu section */
.menu-intro {
  text-align: center;
  margin-bottom: 2rem;
  font-size: 1rem;
}

.menu-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
  gap: 1.5rem;
}

.menu-category {
  background: #fff;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
  padding: 1.5rem;
  border-top: 4px solid var(--primary-color);
}

.menu-category h3 {
  font-family: var(--heading-font);
  color: var(--secondary-color);
  margin-bottom: 0.75rem;
}

.menu-category ul {
  list-style: none;
  padding-left: 0;
}

.menu-category li {
  margin-bottom: 0.5rem;
  font-size: 0.95rem;
  line-height: 1.3;
}

.menu-category li:last-child {
  margin-bottom: 0;
}

/* Reservation section */
.reservation-form {
  max-width: 800px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.form-row {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}

.form-group {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.form-group label {
  margin-bottom: 0.3rem;
  font-weight: 600;
}

.form-group input,
.form-group textarea {
  padding: 0.6rem;
  border: 1px solid #ccc;
  border-radius: 4px;
  font-size: 1rem;
}

.form-group textarea {
  resize: vertical;
}

.reservation-form button {
  align-self: flex-start;
  border: none;
  cursor: pointer;
}

/* Contact section */
.contact-grid {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.contact-details p {
  margin-bottom: 0.75rem;
  font-size: 1rem;
}

.contact-details a {
  color: var(--primary-color);
  text-decoration: none;
}

.contact-details a:hover {
  text-decoration: underline;
}

.contact-map iframe {
  width: 100%;
  height: 300px;
  border: 0;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

@media (min-width: 768px) {
  .contact-grid {
    flex-direction: row;
    align-items: flex-start;
  }
  .contact-details {
    flex: 1;
  }
  .contact-map {
    flex: 2;
  }
}

/* Footer */
footer {
  background: var(--secondary-color);
  color: #fff;
  text-align: center;
  padding: 1rem;
}

footer p {
  font-size: 0.9rem;
}
