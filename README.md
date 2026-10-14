# A Jornada do Amor — como publicar

Pasta pronta para o GitHub Pages. Não precisa instalar nada.

Arquivos:
- `index.html` → o jogo inteiro (história, personagens, cenários, animações e sons já estão dentro dele)
- `config.js` → um arquivo de UMA linha, onde você cola o endereço para receber as respostas por e-mail
- `.nojekyll` → arquivo vazio (pode ficar; se seu computador esconder, ignore, o jogo funciona sem ele)

---

## PASSO 1 (faça ANTES de publicar): receber as respostas por e-mail

O jogo envia as respostas do Matheus por um serviço gratuito chamado Formspree.
Eu não consegui criar essa conta por você (ela precisa ser confirmada no seu e-mail), então esta é a única etapa externa.

1. Acesse https://formspree.io e crie uma conta grátis (use o e-mail onde quer receber as respostas).
2. Confirme o e-mail que o Formspree vai te mandar.
3. Clique em **New Form** (Novo formulário), dê o nome "Jornada do Amor" e escolha o e-mail que vai receber as mensagens.
4. Depois de criar, o Formspree mostra um endereço parecido com `https://formspree.io/f/abcdwxyz`. Copie esse endereço.
5. Abra o arquivo `config.js` num editor de texto (Bloco de Notas serve) e cole o endereço entre as aspas:

   `FORMSPREE_URL: "https://formspree.io/f/abcdwxyz"`

   Salve. É a única edição necessária.

Como funciona: quando o Matheus termina a fase do "Caminho do Castelo", o jogo manda UM e-mail com as respostas. Se a internet cair, o jogo guarda e tenta de novo na próxima vez que ele abrir. O que ele escrever fica salvo no aparelho mesmo se ele clicar em "Pular" ou "Continuar".

Limites do plano grátis: 50 envios por mês, e o Formspree guarda os envios por 30 dias no painel dele. A cópia de segurança permanente é o próprio e-mail, então não apague.

Se ficar vazio (`""`), o jogo funciona normalmente, só não envia nada.

---

## PASSO 2: publicar no GitHub Pages

1. Crie uma conta grátis em https://github.com (se ainda não tiver).
2. Clique no **+** (canto superior direito) → **New repository**.
3. Em "Repository name" escreva `jornada-do-amor`. Deixe **Public**. Clique em **Create repository**.
4. Na página que abrir, clique no link **uploading an existing file**.
5. Abra a pasta `jornada-do-amor` do seu computador e arraste os arquivos DE DENTRO dela (`index.html`, `config.js`, `.nojekyll`) para a janela do GitHub. Importante: os arquivos, não a pasta.
6. Role até o fim e clique em **Commit changes**.
7. Vá em **Settings** (aba no topo do repositório) → **Pages** (menu da esquerda).
8. Em "Build and deployment", em **Source** escolha **Deploy from a branch**. Em **Branch** escolha `main` e a pasta `/ (root)`. Clique em **Save**.
9. Espere 1 a 2 minutos e atualize a página. Vai aparecer o link do seu jogo, no formato:
   `https://SEU-USUARIO.github.io/jornada-do-amor/`

Esse é o link para mandar ao Matheus.

### Se esquecer de colocar o endereço do Formspree
No GitHub, clique em `config.js` → ícone de lápis (✏️) → cole o endereço → **Commit changes**. Em cerca de 1 minuto o site atualiza.

---

## PASSO 3: teste antes de mandar para ele

1. Abra o link e jogue até o "Caminho do Castelo". Escreva respostas de teste.
2. Confira se chegou o e-mail (olhe também o spam). Na primeira vez o Formspree pode pedir uma confirmação por e-mail.
3. Para zerar o jogo: ⚙️ → "Recomeçar do zero". Ou abra o link no celular dele, que é outro navegador e começa limpo.

---

## Bom saber

- O repositório precisa ser **Public** para o Pages grátis. Qualquer pessoa que descobrir o endereço pode abrir o código e ler a carta final antes da hora. Não divulgue o link além dele.
- O endereço do Formspree é público por natureza e não é senha, mas alguém poderia usá-lo para mandar mensagens falsas para você. Se acontecer, apague o formulário no painel do Formspree e crie outro.
- Para editar textos (carta, perguntas, falas), abra `index.html` e procure `LETTER`, `LEVELS`, `INTRO`, `REUNION`.
- Para trocar os desenhos por imagens suas, veja `CUSTOM_IMAGES` no começo do script de `index.html`.
