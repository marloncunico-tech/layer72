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

## Envio dos orçamentos por e-mail (FormSubmit)

Orçamentos e mensagens vão para **contato@zirconiumlabs.com** pelo FormSubmit (formsubmit.co), sem servidor próprio. O envio segue o caminho que o FormSubmit documenta para anexos:

- **Formulário:** um formulário comum (`POST`, `multipart/form-data`) com um campo de arquivo `attachment`.
- **Arquivos:** os arquivos do cliente (STL, DXF, Gerbers, KiCad, Eagle) são compactados no navegador num único `.zip`, com nome no formato `Layer72-Nome-AAAA-MM-DD.zip` ou `VIA72-Nome-AAAA-MM-DD.zip`. Assim o anexo não depende de o FormSubmit aceitar essas extensões.
- **Limite:** 10 MB por envio. Acima disso o orçamento sai sem anexo, com a lista dos arquivos, e o site pede ao cliente que mande os arquivos por e-mail.
- **Depois do envio:** o FormSubmit devolve o cliente para a página (campo `_next`), que mostra a confirmação.

Teste depois de publicar:
1. Faça um orçamento com arquivo em cada site.
2. Confira se o e-mail chega com o `.zip` anexado.
3. Se o FormSubmit pedir uma nova confirmação do endereço, clique no link de ativação.

Na pré-visualização do Claude o envio fica bloqueado. No GitHub Pages ele funciona.

## Antes de divulgar

- Confira os preços, a tolerância informada nas dúvidas frequentes e o horário de atendimento.
