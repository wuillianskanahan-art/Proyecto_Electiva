# Proyecto_Electiva
Mi primer proyecto de practica para reforzar mi aprendizaje 
<!DOCTYPE html>
<html lang="es">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Primera Tarea de Electiva Web 1</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,300;0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">

  <style>
    :root {
      /* Nueva paleta de colores completamente renovada */
      --amarillo-pollito: #F97316;    /* Ahora es un Naranja Coral enérgico */
      --azul-cielo: #D946EF;          /* Ahora es un Fucsia/Magenta vibrante */
      --rojo-sangre: #0D9488;         /* Ahora es un Verde Azulado (Teal) elegante */
      --verde-manzana: #3B82F6;       /* Ahora es un Azul Eléctrico */
      --radio-del-borde: 12px;
      --gris: #64748B;                /* Gris pizarra moderno */
      --fondo-oscuro: #0F172A;        /* Azul oscuro profundo para Navbar y Footer */
    }

    * {
      font-family: 'Poppins', sans-serif; /* Nueva tipografía general */
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    html,
    body {
      height: 100%;
      margin: 0;
      background-color: #F8FAFC; /* Fondo de página sutilmente grisáceo/azul */
    }

    body {
      display: flex;
      flex-direction: column;
    }

    main {
      flex: 1;
      display: grid;
      grid-template-columns: 3fr 1fr;
      gap: 24px;
      padding: 24px;
    }

    /* Estilos de la barra de navegación */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background-color: var(--fondo-oscuro);
      padding: 1.2rem 2rem;
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
    }

    .navbar h1 {
      color: #fff;
      margin: 0;
      font-size: 1.4rem;
      font-weight: 600;
      letter-spacing: -0.5px;
    }

    .nav-links a {
      color: #94A3B8; /* Gris claro para los enlaces inactivos */
      text-decoration: none;
      margin-left: 1.5rem;
      font-weight: 500;
      transition: color 0.3s ease;
    }

    /* Hover con el nuevo color de acento */
    .nav-links a:hover {
      color: var(--amarillo-pollito);
    }

    /* Tarjetas de contenido */
    article {
      margin-bottom: 24px;
    }

    .tarjetaConBordeIzquierdo {
      background-color: #ffffff;
      padding: 24px;
      border-radius: var(--radio-del-borde);
      border-left: 6px solid var(--amarillo-pollito);
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05), 0 2px 4px -1px rgba(0, 0, 0, 0.03);
    }

    .borderojo { border-left-color: var(--rojo-sangre); }
    .bordeazul { border-left-color: var(--azul-cielo); }
    .bordeverde { border-left-color: var(--verde-manzana); }

    h2, h3, h4 {
      font-family: 'Poppins', sans-serif;
      font-weight: 700;
      margin-top: 0;
      color: #1E293B;
    }

    /********** Estilo del aside **********/
    .lorem-aside {
      background-color: #ffffff;
      border-left: 4px solid var(--rojo-sangre);
      padding: 24px;
      border-radius: var(--radio-del-borde);
      height: fit-content;
      box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.05);
    }

    .aside-badge {
      display: inline-block;
      background-color: #FFE4E6; /* Fondo rosa suave */
      color: #9F1239;            /* Texto carmesí oscuro */
      font-size: 0.75rem;
      font-weight: 700;
      padding: 4px 10px;
      border-radius: 9999px;
      text-transform: uppercase;
      margin-bottom: 12px;
    }

    .lorem-aside h3 {
      margin: 0 0 10px 0;
      color: #0F172A;
      font-size: 1.2rem;
    }

    .lorem-aside p {
      color: #475569;
      font-size: 0.9rem;
      line-height: 1.6;
      margin-bottom: 15px;
    }

    .aside-quote {
      font-style: italic;
      color: var(--gris);
      border-left: 3px solid #E2E8F0;
      padding-left: 12px;
      margin: 0 0 15px 0;
      font-size: 0.85rem;
    }

    .aside-link {
      color: var(--amarillo-pollito);
      font-size: 0.85rem;
      font-weight: 600;
      text-decoration: none;
      transition: color 0.2s ease, padding-left 0.2s ease;
    }

    .aside-link:hover {
      color: var(--rojo-sangre);
      text-decoration: underline;
      padding-left: 4px;
    }

    /********** Estilo del Footer **********/
    footer {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      background-color: var(--fondo-oscuro);
      color: white;
      padding: 10px;
      text-align: center;
      height: 80px;
      box-shadow: 0 -4px 6px -1px rgba(0, 0, 0, 0.05);
    }

    footer h4 {
      color: #F1F5F9;
      margin: 0;
      font-size: 0.95rem;
      font-weight: 500;
    }

    footer img {
      width: 36px;
      height: 36px;
      filter: grayscale(1) brightness(1.5); /* Hace las imágenes armoniosas con el fondo oscuro */
      transition: transform 0.2s ease, filter 0.2s ease;
    }

    footer img:hover {
      transform: scale(1.15);
      filter: none; /* Recupera el color original al pasar el cursor */
    }
  </style>
</head>

<body>

  <header>
    <nav class="navbar">
      <h1>Práctica de BoxModel</h1>
      <div class="nav-links">
        <a href="#ancla1">¿Qué es?</a>
        <a href="#ancla2">¿De dónde viene?</a>
        <a href="#ancla3">¿Por qué lo usamos?</a>
        <a href="#ancla4">¿Dónde conseguirlo?</a>
      </div>
    </nav>
  </header>

  <main>
    <section>
      <article id="ancla1">
        <div class="tarjetaConBordeIzquierdo bordeverde">
          <h2>¿Qué es Lorem Ipsum?</h2>
          <p>
            Lorem Ipsum es simplemente el texto de relleno de las imprentas y archivos de texto. Lorem Ipsum ha sido el
            texto de relleno estándar de las industrias desde el año 1500, cuando un impresor desconocido usó una galería de textos y los mezcló de tal manera que logró hacer un
            libro de textos especimen. No sólo sobrevivió 500 años, sino que tambien ingresó como texto de relleno en
            documentos electrónicos, quedando esencialmente igual al original.
          </p>
        </div>
      </article>

      <article id="ancla2">
        <div class="tarjetaConBordeIzquierdo">
          <h2>¿De dónde viene? (Sección 2)</h2>
          <p>
            Al contrario del pensamiento popular, el texto de Lorem Ipsum no es simplemente texto aleatorio. Tiene sus
            raíces en una pieza clásica de la literatura del Latín, que data del año 45 antes de Cristo, haciendo que
            este adquiera más de 2000 años de antigüedad. Richard McClintock, un profesor de Latín de la Universidad de
            Hampden-Sydney en Virginia, encontró una de las palabras más oscuras de la lengua del latín, "consecteur",
            en un pasaje de Lorem Ipsum.
          </p>
          <p>
            El trozo de texto estándar de Lorem Ipsum usado desde el año 1966 es reproducido debajo para aquellos
            interesados. Las secciones 1.10.32 y 1.10.33 de "de Finibus Bonorum et Malorum" por Cicerón son también
            reproducidas en su forma original exacta.
          </p>
        </div>
      </article>

      <article id="ancla3">
        <div class="tarjetaConBordeIzquierdo bordeazul">
          <h2>¿Por qué lo usamos?</h2>
          <p>
            Es un hecho establecido hace demasiado tiempo que un lector se distraerá con el contenido del texto de un
            sitio mientras que mira su diseño. El punto de usar Lorem Ipsum es que tiene una distribución más o menos
            normal de las letras, al contrario de usar textos como por ejemplo "Contenido aquí, contenido aquí". Estos
            textos hacen parecerlo un español que se puede leer.
          </p>
        </div>
      </article>

      <article id="ancla4">
        <div class="tarjetaConBordeIzquierdo borderojo">
          <h2>¿Dónde puedo conseguirlo?</h2>
          <p>
            Hay muchas variaciones de los pasajes de Lorem Ipsum disponibles, pero la mayoría sufrió alteraciones en
            alguna manera, ya sea porque se le agregó humor, o palabras aleatorias que no parecen ni un poco creíbles.
            Si vas a utilizar un pasaje de Lorem Ipsum, necesitás estar seguro de que no hay nada avergonzante escondido en
            el medio del texto.
          </p>
        </div>
      </article>
    </section>

    <aside class="lorem-aside">
      <div class="aside-badge">¿Sabías que?</div>
      <h3>El Mito de Cicerón</h3>
      <p>
        Aunque parece latín sin sentido, el <em>Lorem Ipsum</em> tiene raíces en una pieza de la literatura latina
        clásica del año 45 a.C., escrita por el filósofo <strong>Cicerón</strong>.
      </p>
      <blockquote class="aside-quote">
        "De finibus bonorum et malorum"
      </blockquote>
      <a href="#ancla2" class="aside-link">Leer más sobre el origen →</a>
    </aside>
  </main>

  <footer>
    <h4>Nuestras Redes Sociales</h4>
    <img src="https://proferobyir.github.io/pictures/rrss/facebook.png" alt="Facebook">
    <img src="https://proferobyir.github.io/pictures/rrss/youtube.png" alt="YouTube">
    <img src="https://proferobyir.github.io/pictures/rrss/x.png" alt="X">
    <img src="https://proferobyir.github.io/pictures/rrss/instagram.png" alt="Instagram">
  </footer>

</body>
</html>

