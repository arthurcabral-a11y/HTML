# HTML
/* =========================================================
   Página de notícias de tecnologia
   Estrutura HTML esperada:
   header.site-header > .brand + nav.nav
   main.container
     article.destaque (h1, p.resumo, .meta)
     .grade > article.card[data-categoria="ia|hardware|seguranca|software"]
       (.categoria, h2 > a, p, .meta)
     aside.mais-lidas > ol > li > a
   footer.site-footer
   ========================================================= */

@import url("https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@500;700;800&family=Literata:opsz,wght@7..72,400;7..72,600&display=swap");

:root {
  --papel: #eef1f6;
  --superficie: #ffffff;
  --tinta: #121a2b;
  --tinta-suave: #4a566d;
  --linha: #d5dbe6;
  --acento: #2f54eb;

  --cat-ia: #7a3cff;
  --cat-hardware: #0b8a6a;
  --cat-seguranca: #d6336c;
  --cat-software: #2f54eb;

  --titulo: "Bricolage Grotesque", "Segoe UI", system-ui, sans-serif;
  --texto: "Literata", Georgia, "Times New Roman", serif;

  --raio: 6px;
  --largura: 72rem;
}

@media (prefers-color-scheme: dark) {
  :root {
    --papel: #0e1422;
    --superficie: #161e30;
    --tinta: #e8ecf5;
    --tinta-suave: #9aa6bf;
    --linha: #26314a;
    --acento: #7d9bff;
    --cat-ia: #b18cff;
    --cat-hardware: #3ecfaa;
    --cat-seguranca: #ff7aa8;
    --cat-software: #7d9bff;
  }
}

*, *::before, *::after { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  margin: 0;
  background: var(--papel);
  color: var(--tinta);
  font-family: var(--texto);
  font-size: 1.0625rem;
  line-height: 1.65;
}

a { color: inherit; text-decoration-color: var(--linha); text-underline-offset: 0.2em; }
a:hover { text-decoration-color: var(--acento); }
:focus-visible { outline: 3px solid var(--acento); outline-offset: 3px; }

/* ---------- Cabeçalho ---------- */
.site-header {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  max-width: var(--largura);
  margin: 0 auto;
  padding: 1.25rem 1.25rem;
  border-bottom: 2px solid var(--tinta);
}

.brand {
  font-family: var(--titulo);
  font-weight: 800;
  font-size: 1.75rem;
  letter-spacing: -0.03em;
  text-decoration: none;
}

.nav { display: flex; flex-wrap: wrap; gap: 0.25rem 1.25rem; }
.nav a {
  font-family: var(--titulo);
  font-weight: 500;
  font-size: 0.95rem;
  text-decoration: none;
  color: var(--tinta-suave);
  padding: 0.25rem 0;
  border-bottom: 2px solid transparent;
}
.nav a:hover,
.nav a[aria-current="page"] { color: var(--tinta); border-bottom-color: var(--acento); }

/* ---------- Layout ---------- */
.container {
  display: grid;
  grid-template-columns: minmax(0, 1fr);
  gap: 2.5rem;
  max-width: var(--largura);
  margin: 0 auto;
  padding: 2rem 1.25rem 4rem;
}

@media (min-width: 62rem) {
  .container { grid-template-columns: minmax(0, 1fr) 18rem; }
  .destaque, .grade { grid-column: 1; }
  .mais-lidas { grid-column: 2; grid-row: 1 / span 2; align-self: start; position: sticky; top: 1.5rem; }
}

/* ---------- Destaque (o elemento memorável) ---------- */
.destaque {
  padding-bottom: 2rem;
  border-bottom: 1px solid var(--linha);
}
.destaque h1 {
  font-family: var(--titulo);
  font-weight: 800;
  font-size: clamp(2.25rem, 6vw, 4rem);
  line-height: 1.02;
  letter-spacing: -0.035em;
  margin: 0.5rem 0 1rem;
  max-width: 18ch;
}
.destaque .resumo {
  font-size: 1.25rem;
  color: var(--tinta-suave);
  max-width: 60ch;
  margin: 0 0 1rem;
}

/* ---------- Grade de cards ---------- */
.grade {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(16rem, 1fr));
  gap: 1.25rem;
}

.card {
  --cor: var(--acento);
  background: var(--superficie);
  border: 1px solid var(--linha);
  border-top: 4px solid var(--cor);
  border-radius: var(--raio);
  padding: 1.25rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}
.card[data-categoria="ia"] { --cor: var(--cat-ia); }
.card[data-categoria="hardware"] { --cor: var(--cat-hardware); }
.card[data-categoria="seguranca"] { --cor: var(--cat-seguranca); }
.card[data-categoria="software"] { --cor: var(--cat-software); }

.card .categoria {
  font-family: var(--titulo);
  font-weight: 700;
  font-size: 0.85rem;
  color: var(--cor);
}
.card h2 {
  font-family: var(--titulo);
  font-weight: 700;
  font-size: 1.3rem;
  line-height: 1.2;
  letter-spacing: -0.01em;
  margin: 0;
}
.card h2 a { text-decoration: none; }
.card h2 a:hover { text-decoration: underline; text-decoration-color: var(--cor); }
.card p { margin: 0; color: var(--tinta-suave); font-size: 0.98rem; }

.meta {
  font-family: var(--titulo);
  font-size: 0.85rem;
  color: var(--tinta-suave);
  margin-top: auto;
}

/* ---------- Mais lidas ---------- */
.mais-lidas {
  border-left: 1px solid var(--linha);
  padding-left: 1.25rem;
}
.mais-lidas h2 {
  font-family: var(--titulo);
  font-size: 1.1rem;
  margin: 0 0 1rem;
}
.mais-lidas ol { margin: 0; padding-left: 1.25rem; display: grid; gap: 0.9rem; }
.mais-lidas li::marker { font-family: var(--titulo); font-weight: 700; color: var(--acento); }
.mais-lidas a { font-family: var(--titulo); font-weight: 500; line-height: 1.3; }

/* ---------- Rodapé ---------- */
.site-footer {
  max-width: var(--largura);
  margin: 0 auto;
  padding: 1.5rem 1.25rem 3rem;
  border-top: 1px solid var(--linha);
  font-family: var(--titulo);
  font-size: 0.9rem;
  color: var(--tinta-suave);
}

/* ---------- Mobile e acessibilidade ---------- */
@media (max-width: 40rem) {
  body { font-size: 1rem; }
  .mais-lidas { border-left: 0; border-top: 1px solid var(--linha); padding: 1.5rem 0 0; }
}

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
}
