<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Currículo - Exemplo</title>
    <!-- Importação de fontes do Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
    <style>
        /* Estilos CSS */
        body {
            font-family: 'Montserrat', Arial, sans-serif; /* Fonte do corpo */
            margin: 0; /* Remove margens padrão */
            padding: 0; /* Remove preenchimento padrão */
            background-color: #a2c2e6; /* Fundo azul */
            position: relative; /* Para posicionar formas geométricas */
            color: #333; /* Cor do texto padrão */
        }

        .container {
            max-width: 800px; /* Largura máxima do conteúdo */
            margin: 40px auto; /* Centraliza o container */
            padding: 40px; /* Preenchimento interno */
            background-color: rgba(211, 211, 211, 0.9); /* Fundo cinza semi-transparente */
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3); /* Sombra ao redor do container */
            border-radius: 12px; /* Bordas arredondadas */
            position: relative; /* Para o posicionamento das formas */
            z-index: 1; /* Para ficar acima das formas */
        }

        header {
            background-color: rgba(0, 76, 153, 0.9); /* Cabeçalho azul escuro */
            color: #fff; /* Cor do texto no cabeçalho */
            padding: 30px; /* Preenchimento interno */
            text-align: center; /* Centraliza o texto */
            border-radius: 12px 12px 0 0; /* Bordas arredondadas no topo */
        }

        h1 {
            font-family: 'Playfair Display', serif; /* Fonte do título principal */
            margin: 0; /* Remove margens padrão */
            font-size: 2.5em; /* Tamanho da fonte */
        }

        /* Estilo para a imagem do perfil */
        .profile-pic {
            width: 150px; /* Largura da imagem */
            height: 150px; /* Altura da imagem */
            border-radius: 50%; /* Faz a imagem ficar redonda */
            margin: 20px 0; /* Espaçamento acima e abaixo */
        }

        h2 {
            font-family: 'Playfair Display', serif; /* Fonte dos subtítulos */
            margin-top: 0; /* Remove margem superior */
            font-size: 1.8em; /* Tamanho da fonte */
            border-bottom: 2px solid #004a99; /* Linha abaixo do título */
            padding-bottom: 10px; /* Preenchimento inferior */
        }

        .section {
            margin-bottom: 40px; /* Espaço abaixo das seções */
            padding: 20px; /* Preenchimento interno */
            border: 1px solid #e0e0e0; /* Borda das seções */
            border-radius: 8px; /* Bordas arredondadas */
            background-color: rgba(249, 249, 249, 0.95); /* Fundo semi-transparente para seções */
            transition: background-color 0.3s ease; /* Transição suave ao mudar a cor de fundo */
        }

        .section:hover {
            background-color: rgba(241, 241, 241, 0.95); /* Muda a cor de fundo ao passar o mouse */
        }

        ul {
            list-style-type: none; /* Remove marcadores das listas */
            padding: 0; /* Remove preenchimento */
        }

        li {
            margin-bottom: 10px; /* Espaço abaixo dos itens da lista */
        }

        a {
            color: #0066cc; /* Cor dos links */
            text-decoration: none; /* Remove sublinhado dos links */
            transition: color 0.3s ease; /* Transição suave para a cor dos links */
        }

        a:hover {
            color: #004a99; /* Cor dos links ao passar o mouse */
        }

        .theme-toggle {
            position: fixed; /* Fixa o botão na tela */
            top: 20px; /* Distância do topo */
            right: 20px; /* Distância da direita */
            padding: 10px 15px; /* Preenchimento interno do botão */
            background-color: #0066cc; /* Cor de fundo do botão */
            color: #fff; /* Cor do texto no botão */
            border: none; /* Remove bordas */
            border-radius: 5px; /* Bordas arredondadas */
            cursor: pointer; /* Muda o cursor ao passar o mouse */
            transition: background-color 0.3s ease; /* Transição suave ao mudar a cor de fundo */
            z-index: 2; /* Para ficar acima das formas */
        }

        .theme-toggle:hover {
            background-color: #004a99; /* Cor do botão ao passar o mouse */
        }

        /* Estilos para formas geométricas */
        .shape {
            position: absolute; /* Posiciona as formas de forma absoluta */
            border-radius: 50%; /* Forma redonda */
            opacity: 0.1; /* Leve transparência */
            pointer-events: none; /* Ignora eventos do mouse */
        }

        .shape1 {
            width: 200px; /* Largura da forma 1 */
            height: 200px; /* Altura da forma 1 */
            background-color: #004a99; /* Azul escuro */
            top: 10%; /* Posição vertical */
            left: -100px; /* Posição horizontal */
        }

        .shape2 {
            width: 150px; /* Largura da forma 2 */
            height: 150px; /* Altura da forma 2 */
            background-color: #0066cc; /* Azul claro */
            top: 30%; /* Posição vertical */
            right: -80px; /* Posição horizontal */
        }

        .shape3 {
            width: 250px; /* Largura da forma 3 */
            height: 250px; /* Altura da forma 3 */
            background-color: #0088cc; /* Azul médio */
            bottom: 20px; /* Posição vertical */
            left: 50px; /* Posição horizontal */
        }

        /* Estilos para o modo escuro */
        .dark-mode {
            background-color: #333; /* Fundo escuro */
            color: #fff; /* Texto claro */
        }

        .dark-mode .container {
            background-color: #444; /* Fundo cinza escuro para o container */
        }

        .dark-mode header {
            background-color: #1a2a3a; /* Cabeçalho escuro */
        }

        .dark-mode a {
            color: #79b8ff; /* Cor dos links no modo escuro */
        }

        .dark-mode .section {
            background-color: rgba(255, 255, 255, 0.1); /* Seções com fundo leve no modo escuro */
            border: 1px solid #666; /* Contorno mais claro no modo escuro */
        }
    </style>
</head>
<body>
    <!-- Formas geométricas de fundo -->
    <div class="shape shape1"></div>
    <div class="shape shape2"></div>
    <div class="shape shape3"></div>

    <!-- Botão para alternar entre temas -->
    <button class="theme-toggle">Alternar Tema</button>

    <div class="container">
        <!-- Cabeçalho do currículo -->
        <header>
            <img src="gato de oculos.jpg.jpg" alt="Foto de Gabriel Barreto Sterpin" class="profile-pic"> <!-- Insira o caminho correto da imagem -->
            <h1>Gabriel Barreto Sterpin</h1>
            <p>Estudante</p>
        </header>

        <!-- Seção "Sobre" -->
        <section class="section">
            <h2>Sobre</h2>
            <p>Profissional com experiência em desenvolvimento web, com conhecimentos em HTML, CSS e JavaScript.</p>
        </section>

        <!-- Seção "Contato" -->
        <section class="section">
            <h2>Contato</h2>
            <ul>
                <li>Email: <a href="mailto:fulano@email.com">fulano@email.com</a></li>
                <li>Telefone: (00) 00000-0000</li>
                <li>LinkedIn: <a href="https://linkedin.com/in/fulano" target="_blank">linkedin.com/in/fulano</a></li>
            </ul>
        </section>

        <!-- Seção "Formação" -->
        <section class="section">
            <h2>Formação</h2>
            <ul>
                <li>Graduação em Ciência da Computação (Cursando)</li>
                <li>Cursos Complementares em Desenvolvimento Web</li>
            </ul>
        </section>

        <!-- Seção "Experiência Profissional" -->
        <section class="section">
            <h2>Experiência Profissional</h2>
            <ul>
                <li>Inova Capixaba - Formar - Assistente ADM (2018 - 2022)</li>
            </ul>
        </section>

        <!-- Seção "Interesses" -->
        <section class="section">
            <h2>Interesses</h2>
            <ul>
                <li>Programação</li>
                <li>Design de interface</li>
                <li>Tecnologias emergentes</li>
            </ul>
        </section>
    </div>

    <script>
        // Seleciona o botão de alternar tema e o corpo do documento
        const themeToggle = document.querySelector('.theme-toggle');
        const body = document.body;

        let isDarkMode = false; // Variável para controle do modo escuro

        // Função para alternar o tema
        function toggleTheme() {
            isDarkMode = !isDarkMode; // Inverte o estado do modo
            body.classList.toggle('dark-mode', isDarkMode); // Adiciona ou remove a classe de modo escuro
        }

        // Adiciona um ouvinte de evento ao botão para alternar o tema ao clicar
        themeToggle.addEventListener('click', toggleTheme);
    </script>
</body>
</html>
