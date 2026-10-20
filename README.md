# Mini Bio — Modelo Base (Psicóloga)

Mini site de página única, estilo página-bio, usado como **modelo demonstrativo**
para apresentar o serviço a clientes. Todos os textos entre [colchetes] são
marcadores para substituir pelos dados reais da profissional. Nenhuma pessoa
fictícia é apresentada como real.

## Estrutura da página

1. Capa/bio: foto (marcador), nome, profissão + CRP, cidade, frase de apresentação
   e botões de WhatsApp, Instagram e um link livre.
2. Sobre mim: apresentação + cartão de formação/abordagem/CRP.
3. Áreas de atendimento: 4 cartões substituíveis.
4. Como funciona: 3 passos (WhatsApp → primeira sessão → processo).
5. Perguntas frequentes (acordeão nativo, sem JavaScript pesado).
6. Chamada final + rodapé. Botão flutuante de WhatsApp.

Sem depoimentos de pacientes, por seguir as regras de publicidade do
Conselho de Psicologia.

## Arquivos

- `index.html` — página completa (com meta tags de SEO e dados estruturados já no formato)
- `styles.css` — visual mobile-first: paleta do acolhimento (creme quente, sálvia, argila e marrom suave) e fontes Fraunces (títulos) + Nunito Sans (texto), via Google Fonts com `display=swap`
- `script.js` — só o ano automático do rodapé

Sem imagens binárias: a foto é um marcador em CSS/SVG, trocado pela foto real da cliente na personalização.

## Para personalizar (por cliente)

1. Trocar todos os textos entre [colchetes].
2. Trocar o número `5500000000000` pelo WhatsApp real (nos 3 links: capa, CTA final e botão flutuante).
3. Trocar `instagram.com/seuusuario` e `@[seuinstagram]` pelo perfil real.
4. Trocar o marcador "SUA FOTO AQUI" por uma `<img>` com a foto real.
5. Ajustar as cores em `:root` no `styles.css`, se a cliente escolher outra paleta.

## Publicação no Cloudflare Pages

1. Cloudflare → Workers & Pages → Create → Pages → Connect to Git.
2. Selecionar o repositório `minibiomodelo`.
3. Production branch: `main`. Framework preset: **None**.
4. Build command: deixar **vazio**. Build output directory: deixar **/** (raiz).
5. Save and Deploy. O endereço fica `minibiomodelo.pages.dev` (ou o nome escolhido no projeto).
6. Domínio próprio (quando houver): Custom domains → Set up a domain e seguir a verificação de DNS.

Cada push novo na `main` republica o site automaticamente.
