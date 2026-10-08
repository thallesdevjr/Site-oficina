 # Documentação do Projeto Front-end: Oficina Diesel

Data: 08/10/2026

## 1. Nome do projeto

Oficina Diesel. Eu fiz este projeto aprendendo programação do zero.

- **Autor:** Thalles Alexandre Gonçalves Mendes
- **Site publicado:** [Oficina Diesel](https://site-oficina-self.vercel.app/)

## 2. Descrição do projeto

A Oficina Diesel é uma landing page, que é uma página única de apresentação, de uma oficina fictícia de caminhões, ônibus e máquinas pesadas.

Quando comecei eu não sabia nada de programação. Segui um protótipo de layout que recebi e troquei o tema para oficina diesel, mantendo a estrutura. O site mostra a oficina, os serviços, planos de manutenção, um depoimento, novidades e um formulário de contato.

## 3. Objetivo

O objetivo é o visitante conhecer a oficina, ver os serviços e os planos, ler as novidades e falar com a oficina pelo formulário ou pelo WhatsApp.

Para mim, o objetivo também foi aprender na prática como HTML, CSS e Bootstrap trabalham juntos.

## 4. Público-alvo

Donos de caminhões e ônibus, gestores de frota, empresas de transporte e construtoras que usam máquinas pesadas, como escavadeiras e carregadeiras.

## 5. Tecnologias utilizadas

- **HTML5:** estrutura da página.
- **CSS3 (css/style.css):** cores, fontes e espaçamentos.
- **Bootstrap 5.3.3:** menu, botões, cartões, formulário e responsividade.
- **JavaScript:** janelas de "Saiba mais" e "Ler mais" e validação do formulário.
- **Google Fonts:** fontes Barlow e Barlow Condensed.
- **Vercel:** publicação do site.
- **Ferramentas de apoio:** VS Code, Live Server e o Claude (IA) como professor.

## 6. Estrutura do site

As áreas do site, na ordem em que aparecem na página:

- **Menu:** barra fixa no topo.
- **Capa:** título, botões e foto principal.
- **Clientes:** nomes de empresas.
- **Serviços:** dois blocos com foto.
- **Depoimento:** frase de um cliente.
- **Planos:** três cartões de manutenção.
- **Chamada final:** convite para agendar.
- **Novidades:** três cartões com foto.
- **Contato:** formulário e WhatsApp.
- **Rodapé:** links e informações de contato.

## 7. Organização dos arquivos

```text
Oficina_diesel/
│
├── index.html
│
├── css/
│    └── style.css
│
├── imagens/
│    ├── caminhao.png
│    ├── escavadeira.png
│    ├── oficina.png
│    ├── novidade1.webp
│    ├── novidade2.jpg
│    └── novidade3.webp
│
└── docs/
     └── documentacao.md
```

O arquivo `index.html` tem a estrutura do site e o JavaScript, que fica no final da página. O arquivo `style.css` tem as personalizações de aparência. A pasta `imagens` guarda as fotos usadas. A pasta `docs` guarda esta documentação.

Uma coisa que aprendi: o caminho escrito no código precisa ser igual ao nome real da pasta e do arquivo. Por exemplo, `imagens/caminhao.png`.

## 8. Responsividade

Responsividade quer dizer que o site se ajusta a telas de tamanhos diferentes. Eu usei os recursos do Bootstrap para isso:

- O menu mostra os links abertos no computador e vira o botão de três linhas no celular (`navbar-expand-lg`).
- Texto e foto ficam lado a lado no computador e um embaixo do outro no celular (`row` e `col-md-6`).
- Os nomes dos clientes ficam 2 por linha no celular e todos na mesma linha no computador.
- Os cartões de planos e de novidades se empilham no celular.
- As imagens encolhem para caber na tela (`img-fluid`).

Testei diminuindo a janela do navegador e usando o modo celular do F12.

## 9. Acessibilidade

Fiz só os cuidados básicos que aprendi:

- Todas as imagens têm o atributo `alt`, com uma descrição do que aparece na foto.
- Os títulos seguem uma ordem: um `h1` na capa, `h2` nas seções e `h3` nos cartões.
- O texto tem bom contraste com o fundo. Nos botões amarelos o texto é preto.
- Os links e botões têm textos claros, como "Agendar revisão" e "Enviar pedido".
- Cada campo do formulário tem um rótulo ligado a ele, e os erros aparecem escritos.
- O elemento selecionado pelo teclado ganha um contorno amarelo.
- A página está marcada como português do Brasil (`lang="pt-br"`).
- O CSS respeita quem desliga as animações no computador.

## 10. Decisões de UX

UX é a experiência de quem usa o site. As decisões que tomei pensando nisso:

- Deixar o menu fixo no topo, para a pessoa não precisar voltar ao início da página.
- Usar botões com textos fáceis de entender.
- Fazer os botões de agendar levarem direto ao formulário, já com o assunto escolhido.
- Abrir "Saiba mais" e "Ler mais" numa janelinha, para a pessoa não sair do lugar onde estava.
- Colocar o Plano Frota em destaque, para mostrar qual é o mais escolhido.
- Separar o conteúdo em seções e evitar texto demais na tela.
- Pedir poucas informações no formulário: só nome, telefone e o que a pessoa precisa são obrigatórios.
- Oferecer o WhatsApp como forma rápida de falar com a oficina.

## 11. Dificuldades encontradas

Eu não tinha conhecimento nenhum de programação quando comecei. Usei o Claude, um assistente de IA, como professor, e mesmo com essa ajuda tive várias dificuldades.

**As fotos não apareciam.** O site mostrava só o texto no lugar das imagens. Eu tinha deixado as fotos soltas, sem criar a pasta `imagens`, e o Windows escondia a extensão dos arquivos, então o nome real era `oficina.jpg.png` e o código procurava `oficina.jpg`. Resolvi criando a pasta, corrigindo os nomes e ativando a opção de mostrar as extensões. O mesmo erro voltou com o `style.css`, que estava como `style.css.css` e fora da pasta `css`, e resolvi do mesmo jeito.

**Colocar o texto ao lado da foto.** Não entendia como deixar duas coisas lado a lado. Aprendi o sistema de `row` e `col` do Bootstrap, que divide a linha em 12 partes. Com `col-md-6`, cada lado ocupa metade, e no celular eles se empilham sozinhos.

**O texto ficou centralizado sem eu querer.** A chamada final estava dentro da seção de preços porque faltou fechar a tag `</section>`. Aprendi que toda tag que abre precisa fechar no lugar certo, senão o bloco herda o estilo do de cima.

**Os botões não faziam nada.** Só descia a tela ou nada acontecia. Aprendi que `<button>` sozinho não tem destino e que um link (`<a>`) leva a outro lugar. Depois fiz os botões de agendar levarem a um formulário e os de "Saiba mais" e "Ler mais" abrirem uma janela com informações.

**O menu mudava quando eu diminuía a tela.** Achei que era erro, mas era o recurso responsivo do Bootstrap: em tela pequena os links viram o botão de três linhas. Também precisei fixar o menu no topo para ele acompanhar a rolagem.

**O formulário não envia de verdade.** Aprendi que um site só com HTML, CSS e JavaScript no navegador não consegue mandar e-mail, porque precisaria de um servidor. Por isso o envio é simulado: o formulário confere os campos e mostra uma mensagem de sucesso.

**O JavaScript.** Foi a parte mais difícil de entender, porque eu só conhecia a lógica de programação básica. Pedi para explicarem o código linha por linha, e foi assim que consegui entender o que cada parte faz.

## 12. Melhorias futuras

Futuramente, o projeto poderia receber:

- envio real do formulário, por um servidor ou um serviço de formulários, em vez do envio simulado;
- páginas separadas para os serviços e para as novidades, no lugar das janelas;
- um sistema de agendamento online com escolha de data e horário;
- um mapa com o endereço da oficina;
- um arquivo de CSS mais completo, com mais personalizações;
- fotos e logos reais dos clientes, no lugar dos nomes fictícios.
