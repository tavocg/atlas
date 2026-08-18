---
title: Contacto
toc: false
---

<style>
.contact-layout {
  display: grid;
  gap: 2rem;
  grid-template-columns: minmax(0, 0.8fr) minmax(0, 1.2fr);
  margin-top: 2rem;
}
.contact-intro h2 {
  margin-top: 0;
}
.contact-intro p {
  color: rgb(75 85 99);
  text-align: left;
  text-indent: 0;
}
.contact-links {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin-top: 1.5rem;
}
.contact-form {
  display: grid;
  gap: 1rem;
  grid-template-columns: repeat(2, minmax(0, 1fr));
}
.contact-field {
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
}
.contact-field-full {
  grid-column: 1 / -1;
}
.contact-field label {
  font-size: 0.9rem;
  font-weight: 600;
}
.contact-field input,
.contact-field select,
.contact-field textarea {
  background: transparent;
  border: 1px solid rgb(229 231 235);
  border-radius: 0.375rem;
  color: inherit;
  font: inherit;
  padding: 0.7rem 0.8rem;
  width: 100%;
}
.contact-field input:focus,
.contact-field select:focus,
.contact-field textarea:focus {
  border-color: hsl(var(--primary-hue) 100% 45%);
  outline: none;
}
html.dark .contact-field input,
html.dark .contact-field select,
html.dark .contact-field textarea {
  border-color: rgb(255 255 255 / 0.16);
}
html.dark .contact-field input:focus,
html.dark .contact-field select:focus,
html.dark .contact-field textarea:focus {
  border-color: hsl(var(--primary-hue) 100% 65%);
}
.contact-field textarea {
  resize: vertical;
}
.contact-submit {
  background: hsl(var(--primary-hue) 100% 45%);
  border: 0;
  border-radius: 0.375rem;
  color: white;
  cursor: pointer;
  font-weight: 700;
  padding: 0.75rem 1rem;
  width: fit-content;
}
.contact-hidden {
  display: none;
}
@media (max-width: 768px) {
  .contact-layout,
  .contact-form {
    grid-template-columns: 1fr;
  }
}
</style>

<div class="contact-layout">
<section class="contact-intro">
<h2>Conversemos sobre su proyecto</h2>
<p>Cuéntenos qué necesita y le responderemos para coordinar una primera conversación.</p>
<div class="contact-links">
<a href="mailto:info@atlascstg.com">info@atlascstg.com</a>
</div>
</section>
<form class="contact-form" action="https://formspree.io/f/xvkpvpab" method="POST">
<input type="hidden" name="_subject" value="Nuevo mensaje desde Atlas Consulting">
<input type="text" name="_gotcha" class="contact-hidden" tabindex="-1" autocomplete="off">
<div class="contact-field">
<label for="name">Nombre</label>
<input id="name" name="name" type="text" autocomplete="name" required>
</div>
<div class="contact-field">
<label for="email">Correo electrónico</label>
<input id="email" name="email" type="email" autocomplete="email" required>
</div>
<div class="contact-field">
<label for="organization">Organización</label>
<input id="organization" name="organization" type="text" autocomplete="organization">
</div>
<div class="contact-field">
<label for="service">Área de interés</label>
<select id="service" name="service">
<option value="">Seleccione una opción</option>
<option>Consultoría para eventos deportivos</option>
<option>Asesoría administrativa y estratégica</option>
<option>Plataforma y digitalización de torneos</option>
<option>Otro</option>
</select>
</div>
<div class="contact-field contact-field-full">
<label for="message">Mensaje</label>
<textarea id="message" name="message" rows="7" required></textarea>
</div>
<button class="contact-submit" type="submit">Enviar mensaje</button>
</form>
</div>
