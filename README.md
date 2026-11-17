# Site Layer72

Site de uma página da Layer72 Fabricação Digital (impressão 3D em resina e corte CNC), uma operação Zirconium.

## Conteúdo

- `index.html`: o site completo, com estilos e scripts no próprio arquivo.
- `.nojekyll`: faz o GitHub Pages publicar os arquivos como estão.

Bibliotecas e fontes carregadas da internet: three.js r128 (cdnjs), OrbitControls (jsDelivr), Poppins e Inter (Google Fonts).

## Publicar no GitHub Pages

1. Crie um repositório no GitHub (por exemplo, `layer72-site`).
2. Envie `index.html` e `.nojekyll` para a raiz da branch `main`: arraste os arquivos em **Add file → Upload files**, ou use `git push`.
3. No repositório, abra **Settings → Pages**. Em **Build and deployment**, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`. Salve.
4. Em 1 a 2 minutos o site fica em `https://<usuario>.github.io/layer72-site/`.

## Domínio próprio (layer72.com.br)

1. Registre o domínio no Registro.br.
2. Em **Settings → Pages → Custom domain**, informe `layer72.com.br`. O GitHub cria o arquivo `CNAME` no repositório.
3. No DNS do Registro.br, crie registros A para o domínio apontando para 185.199.108.153, 185.199.109.153, 185.199.110.153 e 185.199.111.153, e um CNAME `www` para `<usuario>.github.io`.
4. Depois que o DNS propagar, marque **Enforce HTTPS**.

Confira esses passos na documentação oficial do GitHub Pages, porque os endereços podem mudar.

## Envio dos orçamentos por e-mail

Orçamentos e mensagens do formulário de contato vão para **contato@zirconiumlabs.com** pelo FormSubmit (formsubmit.co), sem servidor próprio.

1. Depois de publicar, envie um orçamento de teste pelo site.
2. O FormSubmit manda um e-mail de ativação para contato@zirconiumlabs.com. Clique no link para confirmar.
3. Envie outro orçamento e confira se ele chegou com o arquivo STL/DXF anexado.

Se o envio falhar, o site abre o e-mail do visitante já preenchido, para ele enviar manualmente.

Para trocar o destino, edite a constante `EMAIL` no script do `index.html` e os textos que mostram o endereço.

## Antes de divulgar

- Troque o WhatsApp provisório `(00) 00000-0000` na seção de contato.
- Confira os preços, a tolerância informada nas dúvidas frequentes e o horário de atendimento.
