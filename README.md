<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Fofocalizando EJC BDI</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Fofocalizando EJC BDI</h1>
    
  </header>

  <div class="container" id="blogPosts">
    <!-- todas as notícias vão ser em JavaScript -->
  </div>

  <script>
    const posts = [
      {
        titulo: "Primeiro post",
        conteudo: "Notícia ...",
        imagem:""
      },
      {
        titulo: "Segundo Post",
        conteudo: "Notícia...",
      },
      {
        titulo:"Terceiro post",
        conteudo:"Notícia",
        Video:""
      }
    ];

    const container = document.getElementById("blogPosts");

    posts.forEach(post => {
      const div = document.createElement("div");
      div.className = "post";

      const titulo = document.createElement("h2");
      titulo.textContent = post.titulo;

      const data = document.createElement("div");
      data.className = "date";
      data.textContent = `Publicado em: ${new Date().toLocaleDateString()}`;

      const conteudo = document.createElement("p");
      conteudo.textContent = post.conteudo;

      div.appendChild(titulo);
      div.appendChild(data);
      div.appendChild(conteudo);

      container.appendChild(div);
    });
  </script>
</body>
</html>
