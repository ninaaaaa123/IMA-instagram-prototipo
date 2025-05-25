<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Prototipo Instagram IMA - Links</title>
<style>
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: #fafafa;
    margin: 0; padding: 0;
    color: #262626;
  }
  a {
    color: inherit;
    text-decoration: none;
  }
  a:hover {
    text-decoration: underline;
  }
  .container {
    max-width: 800px;
    margin: 20px auto 60px;
    background: white;
    border: 1px solid #dbdbdb;
    border-radius: 8px;
    padding: 20px;
  }
  .profile-header {
    display: flex;
    align-items: center;
    gap: 20px;
    border-bottom: 1px solid #dbdbdb;
    padding-bottom: 15px;
  }
  .profile-photo {
    width: 80px; height: 80px;
    border-radius: 50%;
    background: url('https://upload.wikimedia.org/wikipedia/commons/thumb/a/a2/IMA_Logo_Example.png/512px-IMA_Logo_Example.png') center/contain no-repeat;
    background-color: #e1e1e1;
    flex-shrink: 0;
  }
  .profile-info h1 {
    margin: 0;
    font-size: 28px;
    font-weight: 700;
  }
  .profile-info p {
    margin: 5px 0;
    font-size: 16px;
    line-height: 1.4;
  }
  .bio-linktree a {
    display: inline-block;
    background-color: #0095f6;
    color: white;
    padding: 8px 12px;
    border-radius: 20px;
    font-weight: 600;
    margin-right: 8px;
    font-size: 14px;
    transition: background-color 0.3s ease;
  }
  .bio-linktree a:hover {
    background-color: #0077c9;
  }
  .posts {
    margin-top: 25px;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 15px;
  }
  .post {
    background: #f9f9f9;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 1px 3px rgb(0 0 0 / 0.1);
    display: flex;
    flex-direction: column;
    cursor: pointer;
    transition: box-shadow 0.3s ease, transform 0.3s ease;
  }
  .post:hover {
    box-shadow: 0 8px 20px rgba(0,0,0,0.2);
    transform: translateY(-4px);
  }
  .post img {
    width: 100%;
    height: 160px;
    object-fit: cover;
  }
  .post-content {
    padding: 12px 15px;
    flex-grow: 1;
  }
  .post-title {
    font-weight: 700;
    font-size: 16px;
    margin: 0 0 8px;
    color: #0095f6;
  }
  .post-desc {
    font-size: 14px;
    color: #555;
    margin: 0;
  }
  /* WhatsApp fixed button */
  .whatsapp-btn {
    position: fixed;
    bottom: 30px;
    right: 30px;
    background-color: #25d366;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    box-shadow: 0 2px 8px rgba(0,0,0,0.3);
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    z-index: 9999;
    transition: background-color 0.3s ease;
  }
  .whatsapp-btn:hover {
    background-color: #1ebe57;
  }
  .whatsapp-btn svg {
    width: 32px;
    height: 32px;
    fill: white;
  }
</style>
</head>
<body>

<div class="container" role="main">

  <!-- Perfil Header -->
  <header class="profile-header">
    <div class="profile-photo" aria-label="Logo IMA"></div>
    <div class="profile-info">
      <h1>IMA_Sostenible</h1>
      <p>Soluciones precisas y sostenibles para plantas de tratamiento de agua 💧<br>
         Tecnología FLAEBI | Asesoría ambiental | Contáctanos 👇</p>
      <nav class="bio-linktree" aria-label="Enlaces a canales externos">
        <a href="https://wa.me/1234567890" target="_blank" rel="noopener" aria-label="Contactar por WhatsApp">WhatsApp</a>
        <a href="https://facebook.com/IMA" target="_blank" rel="noopener" aria-label="Página de Facebook">Facebook</a>
        <a href="https://youtube.com/IMA" target="_blank" rel="noopener" aria-label="Canal de YouTube">YouTube</a>
        <a href="https://linkedin.com/company/IMA" target="_blank" rel="noopener" aria-label="Perfil LinkedIn">LinkedIn</a>
      </nav>
    </div>
  </header>

  <!-- Posts como enlaces -->
  <section class="posts" aria-label="Publicaciones recientes">

    <a href="https://example.com/flaebi" class="post" aria-label="Ver detalles de Reactor FLAEBI">
      <img src="https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=600&q=80" alt="Reactor FLAEBI en operación" />
      <div class="post-content">
        <h2 class="post-title">Conoce el Reactor FLAEBI</h2>
        <p class="post-desc">Tecnología de flujo pistón con bioaumentación para optimizar plantas de tratamiento.</p>
      </div>
    </a>

    <a href="https://example.com/ecobacter" class="post" aria-label="Ver detalles de ECOBACTER">
      <img src="https://images.unsplash.com/photo-1573496776239-c06cc2f3f375?auto=format&fit=crop&w=600&q=80" alt="Envase de microorganismos ECOBACTER" />
      <div class="post-content">
        <h2 class="post-title">ECOBACTER en acción</h2>
        <p class="post-desc">Microorganismos especializados para descontaminación eficiente.</p>
      </div>
    </a>

    <a href="https://example.com/asesoria" class="post" aria-label="Ver detalles de asesoría ambiental">
      <img src="https://images.unsplash.com/photo-1504384308090-c894fdcc538d?auto=format&fit=crop&w=600&q=80" alt="Asesoría ambiental con equipo de trabajo" />
      <div class="post-content">
        <h2 class="post-title">Asesoría ambiental para empresas</h2>
        <p class="post-desc">Gestión integral y sostenible para tu industria.</p>
      </div>
    </a>

    <a href="https://example.com/proyectos" class="post" aria-label="Ver detalles de proyectos destacados">
      <img src="https://images.unsplash.com/photo-1519337265831-281ec6cc8514?auto=format&fit=crop&w=600&q=80" alt="Planta de tratamiento moderna" />
      <div class="post-content">
        <h2 class="post-title">Proyectos destacados</h2>
        <p class="post-desc">Colaboramos con Consorcio Civil Minero, Universidad de la Costa y más.</p>
      </div>
    </a>

  </section>

</div>

<!-- WhatsApp fixed button -->
<a href="https://wa.me/1234567890" target="_blank" rel="noopener" aria-label="Contactar por WhatsApp" class="whatsapp-btn" title="Chat WhatsApp">
  <svg viewBox="0 0 24 24" aria-hidden="true" focusable="false">
    <path d="M20.52 3.48A11.91 11.91 0 0012 0a11.91 11.91 0 00-8.52 3.48A11.91 11.91 0 000 12c0 2.1.55 4.12 1.6 5.9L0 24l6.23-1.58A11.91 11.91 0 0012 24c6.62 0 12-5.38 12-12a11.91 11.91 0 00-3.48-8.52zm-8.5 16.68a7.56 7.56 0 01-3.88-1.1l-.27-.17-3.69.94.99-3.6-.18-.29a7.54 7.54 0 1110.88 10.87 7.44 7.44 0 01-3.05.34zm4.27-5.75c-.23-.12-1.36-.67-1.57-.75-.2-.08-.34-.12-.48.12-.14.23-.57.75-.7.91-.13.15-.26.17-.49.06-.23-.12-1-.36-1.9-1.17-.7-.63-1.17-1.4-1.3-1.63-.13-.23-.01-.35.1-.47.1-.1.23-.27.34-.4.11-.13.15-.23.23-.38.08-.14.04-.27-.02-.4-.07-.14-.48-1.17-.66-1.6-.17-.42-.35-.37-.48-.37-.12 0-.26 0-.4 0-.13 0-.34.05-.52.23s-.68.67-.68 1.63.7 1.9.8 2.04c.1.15 1.4 2.14 3.4 3 2 .86 2 .57 2.36.54.36-.03 1.16-.47 1.32-.92.17-.44.17-.82.12-.91-.05-.1-.19-.15-.41-.27z"/>
  </svg>
</a>

</body>
</html>
