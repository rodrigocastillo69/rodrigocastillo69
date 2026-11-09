<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Rodrigo Castillo · IA y Ciencia de Datos</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#EEF2F7; --cell:#FFFFFF; --ink:#16233A; --muted:#5B6B82; --line:#D5DDE8;
  --py:#3776AB; --yellow:#FFD43B; --code:#F5F8FC; --ok:#1E8E5A;
  --sans:"IBM Plex Sans",system-ui,-apple-system,"Segoe UI",sans-serif;
  --mono:"IBM Plex Mono",ui-monospace,Menlo,Consolas,monospace;
}
@media (prefers-color-scheme:dark){
  :root{--bg:#0F1724; --cell:#172236; --ink:#E6EDF7; --muted:#93A4BC; --line:#27364F; --py:#6FA8DC; --code:#101B2D; --ok:#4FD08F;}
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;background:var(--bg);color:var(--ink);font:16px/1.65 var(--sans);}
.wrap{max-width:860px;margin:0 auto;padding:40px 20px 72px}
a{color:var(--py)}
a:focus-visible,button:focus-visible{outline:3px solid var(--yellow);outline-offset:2px}

/* celdas de notebook */
.cell{display:grid;grid-template-columns:64px 1fr;gap:0 14px;margin:0 0 22px}
.prompt{font:500 13px/1.9 var(--mono);color:var(--py);text-align:right;padding-top:16px;user-select:none}
.body{background:var(--cell);border:1px solid var(--line);border-left:4px solid var(--py);border-radius:6px;padding:20px 24px}
.out .prompt{color:var(--ok)}
.out .body{border-left-color:var(--ok)}
h1{font-size:clamp(2rem,6vw,3.1rem);line-height:1.1;margin:0 0 8px;letter-spacing:-.02em}
h2{font-size:1.25rem;margin:0 0 12px}
p{margin:0 0 12px}
p:last-child{margin-bottom:0}
.muted{color:var(--muted)}
pre,code{font-family:var(--mono)}
pre{margin:0;background:var(--code);border:1px solid var(--line);border-radius:6px;padding:14px 16px;overflow-x:auto;font-size:14px;line-height:1.7}
.k{color:#B2478B}.s{color:#1E8E5A}.f{color:var(--py)}.c{color:var(--muted)}
@media (prefers-color-scheme:dark){.k{color:#E58BC4}.s{color:#7FDBA9}}

/* hero */
.hero .body{border-left-color:var(--yellow);padding:28px 26px}
.role{font:500 15px var(--mono);color:var(--py);margin:0 0 18px}
.cta{display:flex;gap:10px;flex-wrap:wrap;margin-top:20px}
.btn{display:inline-block;padding:9px 16px;border-radius:6px;font-weight:600;font-size:14px;text-decoration:none;border:1px solid var(--py)}
.btn.main{background:var(--py);color:#fff}
.btn.alt{color:var(--py);background:transparent}
.btn:hover{filter:brightness(1.1)}

/* skills */
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(112px,1fr));gap:10px;margin-top:14px}
.tool{display:flex;flex-direction:column;align-items:center;gap:8px;padding:14px 6px;border:1px solid var(--line);border-radius:8px;background:var(--code);font:500 13px var(--mono);text-align:center}
.tool img{width:38px;height:38px}
.tool.dim{opacity:.85;border-style:dashed}
.legend{font-size:13px;margin-top:12px}

/* proyectos */
.projects{display:grid;gap:12px;margin-top:6px}
.proj{border:1px solid var(--line);border-radius:8px;padding:14px 16px;background:var(--code)}
.proj h3{margin:0 0 4px;font-size:1rem}
.proj p{font-size:14.5px}
.tags{display:flex;gap:6px;flex-wrap:wrap;margin-top:8px}
.tags span{font:500 12px var(--mono);padding:2px 8px;border-radius:99px;background:var(--yellow);color:#16233A}

/* lista */
ul.clean{list-style:none;margin:0;padding:0}
ul.clean li{padding:6px 0;border-bottom:1px dashed var(--line)}
ul.clean li:last-child{border:0}

/* una sola entrada: el cursor de la primera celda */
.cursor{display:inline-block;width:9px;height:1.05em;background:var(--yellow);vertical-align:-3px;margin-left:3px;animation:blink 1.1s steps(1) infinite}
@keyframes blink{50%{opacity:0}}
@media (prefers-reduced-motion:reduce){.cursor{animation:none}html{scroll-behavior:auto}}

footer{text-align:center;color:var(--muted);font:13px var(--mono);margin-top:36px}

@media (max-width:620px){
  .cell{grid-template-columns:1fr}
  .prompt{text-align:left;padding:0 0 4px}
  .body{padding:18px}
}
</style>
</head>
<body>
<main class="wrap">

  <!-- 1. PRESENTACIÓN -->
  <section class="cell hero">
    <div class="prompt">In [1]:</div>
    <div class="body">
      <p class="role">Estudiante de IA y Ciencia de Datos</p>
      <h1>Hola, soy Rodrigo Castillo<span class="cursor" aria-hidden="true"></span></h1>
      <p class="muted">Estoy empezando en tecnología y aprendiendo a convertir datos en respuestas con Python. Me gusta entender cómo funcionan las cosas y construir proyectos pequeños que pueda explicar paso a paso.</p>
      <div class="cta">
        <a class="btn main" href="#proyectos">Ver mis proyectos</a>
        <a class="btn alt" href="#contacto">Contactarme</a>
      </div>
    </div>
  </section>

  <!-- 2. CÓDIGO "SOBRE MÍ" -->
  <section class="cell">
    <div class="prompt">In [2]:</div>
    <div class="body">
      <h2>Sobre mí</h2>
<pre><span class="k">class</span> <span class="f">Rodrigo</span>:
    estudia   = <span class="s">"Inteligencia Artificial y Ciencia de Datos"</span>
    lenguaje  = <span class="s">"Python"</span>
    ubicacion = <span class="s">"Guadalajara, México"</span>   <span class="c"># edita si prefieres otra</span>
    idiomas   = [<span class="s">"Español"</span>, <span class="s">"Inglés (tu nivel)"</span>]
    objetivo  = <span class="s">"Mi primer empleo o prácticas en datos / IA"</span></pre>
    </div>
  </section>

  <!-- 3. HABILIDADES -->
  <section class="cell out">
    <div class="prompt">Out [2]:</div>
    <div class="body">
      <h2>Herramientas</h2>
      <p class="muted">Lo que uso y lo que estoy aprendiendo.</p>
      <div class="grid">
        <div class="tool"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" onerror="this.style.display='none'">Python</div>
        <div class="tool"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/pandas/pandas-original.svg" onerror="this.style.display='none'">Pandas</div>
        <div class="tool"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/numpy/numpy-original.svg" onerror="this.style.display='none'">NumPy</div>
        <div class="tool"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jupyter/jupyter-original-wordmark.svg" onerror="this.style.display='none'">Jupyter</div>
        <div class="tool"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" onerror="this.style.display='none'">Git</div>
        <div class="tool"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/github/github-original.svg" onerror="this.style.display='none'">GitHub</div>
        <div class="tool dim"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/scikitlearn/scikitlearn-original.svg" onerror="this.style.display='none'">scikit-learn</div>
        <div class="tool dim"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/matplotlib/matplotlib-original.svg" onerror="this.style.display='none'">Matplotlib</div>
        <div class="tool dim"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" onerror="this.style.display='none'">SQL</div>
        <div class="tool dim"><img alt="" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg" onerror="this.style.display='none'">TensorFlow</div>
      </div>
      <p class="legend muted">Borde sólido: lo uso. Borde punteado: lo estoy aprendiendo. Deja solo lo que de verdad hayas tocado.</p>
    </div>
  </section>

  <!-- 4. PROYECTOS -->
  <section class="cell" id="proyectos">
    <div class="prompt">In [3]:</div>
    <div class="body">
      <h2>Proyectos</h2>
      <div class="projects">
        <article class="proj">
          <h3><a href="https://github.com/rodrigocastillo69">Análisis de un dataset real</a></h3>
          <p>Limpieza, exploración y gráficas de un conjunto de datos público. Qué pregunta me hice y qué descubrí.</p>
          <div class="tags"><span>Python</span><span>Pandas</span><span>Matplotlib</span></div>
        </article>
        <article class="proj">
          <h3><a href="https://github.com/rodrigocastillo69">Mi primer modelo de Machine Learning</a></h3>
          <p>Un modelo sencillo que predice algo (precios, aprobación, clasificación) y cómo medí su resultado.</p>
          <div class="tags"><span>scikit-learn</span><span>Jupyter</span></div>
        </article>
        <article class="proj">
          <h3><a href="https://github.com/rodrigocastillo69">Un script que automatiza algo</a></h3>
          <p>Algo de tu día a día: renombrar archivos, leer un Excel, un bot sencillo. Lo útil vale más que lo complejo.</p>
          <div class="tags"><span>Python</span><span>Automatización</span></div>
        </article>
      </div>
      <p class="legend muted">Estos tres son ejemplos: reemplaza título, descripción y enlace por tus repositorios reales.</p>
    </div>
  </section>

  <!-- 5. APRENDIENDO -->
  <section class="cell">
    <div class="prompt">In [4]:</div>
    <div class="body">
      <h2>Lo que estoy aprendiendo ahora</h2>
      <ul class="clean">
        <li>Estadística y probabilidad aplicadas a datos</li>
        <li>SQL para consultar bases de datos</li>
        <li>Machine Learning con scikit-learn</li>
        <li>Visualización de datos que se entienda sin explicación</li>
      </ul>
    </div>
  </section>

  <!-- 6. CONTACTO -->
  <section class="cell out" id="contacto">
    <div class="prompt">Out [4]:</div>
    <div class="body">
      <h2>Hablemos</h2>
      <p>Busco mi primera oportunidad en datos o IA y me encantaría aprender de un equipo.</p>
<pre><span class="k">contacto</span> = {
    <span class="s">"github"</span>:   <span class="s">"github.com/rodrigocastillo69"</span>,
    <span class="s">"linkedin"</span>: <span class="s">"linkedin.com/in/tu-usuario"</span>,
    <span class="s">"email"</span>:    <span class="s">"tu-correo@ejemplo.com"</span>,
}</pre>
      <div class="cta">
        <a class="btn main" href="https://github.com/rodrigocastillo69">GitHub</a>
        <a class="btn alt" href="https://linkedin.com/in/tu-usuario">LinkedIn</a>
        <a class="btn alt" href="mailto:tu-correo@ejemplo.com">Correo</a>
      </div>
    </div>
  </section>

  <footer>Hecho con Python en la cabeza y HTML en las manos</footer>
</main>
</body>
</html>
