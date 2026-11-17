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

## Envio dos orçamentos por e-mail (com os arquivos)

O FormSubmit entrega o texto dos orçamentos, mas descarta os arquivos anexados. Para os arquivos chegarem, o site usa um Google Apps Script gratuito, criado na conta Google de vocês. A cada orçamento ele:

- envia o e-mail para contato@zirconiumlabs.com com os dados do pedido e os arquivos anexados (até 20 MB; acima disso, vão só os links);
- guarda os arquivos na pasta "Orçamentos dos sites" do Google Drive;
- deixa o "Responder" do e-mail apontando para o cliente.

### Configuração (uma vez, cerca de 5 minutos; o mesmo script atende os dois sites)

1. Acesse https://script.google.com com a conta Google que vai enviar os e-mails e clique em **Novo projeto**.
2. Apague o conteúdo do editor e cole o arquivo `apps-script/Code.gs` deste zip. Salve.
3. Selecione a função `testeEnvio` e clique em **Executar**. Autorize o acesso ao Gmail e ao Drive quando o Google pedir. Deve chegar um e-mail de teste com o arquivo `teste.txt` anexado.
4. Clique em **Implantar → Nova implantação**, escolha o tipo **App da Web** e configure:
   - **Executar como:** Eu
   - **Quem pode acessar:** Qualquer pessoa

   Clique em **Implantar** e copie a URL que termina em `/exec`.
5. No `index.html` de cada site, troque `const ENDPOINT = "";` por `const ENDPOINT = "https://script.google.com/macros/s/…/exec";`, colando a URL copiada. Publique de novo no GitHub.
6. Faça um orçamento de teste com arquivo em cada site.

Enquanto a URL não estiver configurada, o site continua usando o FormSubmit, e os e-mails podem chegar sem os arquivos. Se o envio falhar, o site oferece abrir o e-mail do cliente já preenchido.

Limite do cliente: 25 MB somando os arquivos. Acima disso, o orçamento é enviado sem anexo, e o site pede ao cliente que mande os arquivos por e-mail.

## Antes de divulgar

- Troque o WhatsApp provisório `(00) 00000-0000` na seção de contato.
- Confira os preços, a tolerância informada nas dúvidas frequentes e o horário de atendimento.
