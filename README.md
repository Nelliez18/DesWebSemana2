Entregável de Desenvolvimento Web – Estilização do Formulário de Inscrição
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DevBlog - Inscrição Estilizada</title>
    <style>
        /* --- CONFIGURAÇÕES GERAIS DA PÁGINA --- */
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            line-height: 1.6; 
            margin: 0; 
            padding: 20px; 
            background-color: #f0f2f5; /* Fundo cinza claro para destacar os elementos */
            color: #333;
        }

        header { 
            background: #1a1a1a; 
            color: #fff; 
            padding: 15px 30px; 
            border-radius: 8px;
        }
        
        nav a { 
            color: #fff; 
            margin-right: 20px; 
            text-decoration: none; 
            font-weight: 500;
        }

        .container { 
            display: flex; 
            gap: 30px; 
            margin-top: 25px; 
        }

        main { 
            flex: 2; 
        }

        article { 
            background: #fff;
            padding: 20px;
            margin-bottom: 25px; 
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }

        img { 
            max-width: 100%; 
            height: auto; 
            display: block; 
            margin-top: 15px; 
            border-radius: 6px;
        }

        /* --- ESTILIZAÇÃO DO FORMULÁRIO (ASIDE) --- */
        aside { 
            flex: 1; 
            background-color: #ffffff; /* Fundo diferente da página */
            padding: 25px; 
            border-radius: 8px; 
            max-width: 450px; /* Largura máxima do container */
            box-shadow: 0 4px 12px rgba(0,0,0,0.1); /* Sombra sutil para usabilidade */
            height: fit-content;
        }

        aside h3 {
            margin-top: 0;
            color: #1a1a1a;
            border-bottom: 2px solid #007bff;
            padding-bottom: 8px;
        }

        /* Estrutura principal do formulário empilhada */
        form {
            display: flex;
            flex-direction: column;
            gap: 16px; /* Organiza os campos um embaixo do outro com espaçamento constante */
        }

        /* BÔNUS: Grupo para colocar Nome e E-mail lado a lado */
        .form-row {
            display: flex;
            gap: 12px;
            justify-content: space-between;
        }

        /* Ajuste para que cada campo na linha ocupe o mesmo espaço proporcional */
        .form-group-inline {
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 6px;
        }

        /* Grupo padrão para os campos individuais */
        .form-group {
            display: flex;
            flex-direction: column;
            gap: 6px;
        }

        /* Estilização dos Labels */
        label {
            font-size: 14px;
            font-weight: 600;
            color: #444;
        }

        /* Estilização de Inputs e Selects */
        input[type="text"],
        input[type="email"],
        input[type="number"],
        select {
            padding: 10px 12px;
            border: 1px solid #ccc;
            border-radius: 6px; /* Cantos arredondados */
            font-size: 15px;
            background-color: #fafafa;
            transition: border-color 0.2s, box-shadow 0.2s;
            width: 100%;
            box-sizing: border-box;
        }

        /* Efeito de foco para melhorar a usabilidade */
        input:focus, select:focus {
            border-color: #007bff;
            box-shadow: 0 0 0 3px rgba(0, 123, 255, 0.15);
            outline: none;
            background-color: #fff;
        }

        /* Customização para o campo de checkbox de termos */
        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 8px;
            cursor: pointer;
            user-select: none;
            font-size: 14px;
        }

        .checkbox-group input {
            width: 18px;
            height: 18px;
            cursor: pointer;
        }

        /* Botão de Enviar com Destaque Visual */
        button[type="submit"] {
            background-color: #007bff; /* Cor de destaque azul */
            color: #ffffff; /* Texto branco */
            padding: 12px;
            border: none;
            border-radius: 6px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer; /* Cursor de clique */
            transition: background-color 0.2s, transform 0.1s;
            margin-top: 5px;
        }

        /* Efeito hover (passar o mouse) no botão */
        button[type="submit"]:hover {
            background-color: #0056b3;
        }

        /* Efeito active (clique) no botão */
        button[type="submit"]:active {
            transform: scale(0.98);
        }

        footer { 
            text-align: center; 
            margin-top: 30px; 
            padding: 15px; 
            background: #1a1a1a; 
            color: #fff; 
            border-radius: 8px;
        }

        /* Responsividade para telas menores (Celulares) */
        @media (max-width: 768px) {
            .container { flex-direction: column; }
            .form-row { flex-direction: column; gap: 16px; }
            aside { max-width: 100%; }
        }
    </style>
</head>
<body>

    <header>
        <h1>DevBlog</h1>
        <nav>
            <a href="#home">Home</a>
            <a href="#artigos">Artigos</a>
            <a href="#sobre">Sobre</a>
        </nav>
    </header>

    <div class="container">
        
        <main id="artigos">
            <article>
                <h2>Entendendo o HTML5 Semântico</h2>
                <p>Usar tags semânticas como header, main, article e aside ajuda os motores de busca (SEO) e tecnologias de assistência a compreenderem a estrutura real do seu site.</p>
                <img src="https://picsum.photos" alt="Ilustração sobre código e semântica web">
            </article>

            <article>
                <h2>A Importância da Validação de Formulários</h2>
                <p>Validar dados diretamente no navegador melhora a experiência do usuário, impedindo o envio de informações incorretas antes mesmo de chegarem ao servidor.</p>
                <img src="https://picsum.photos" alt="Ilustração sobre segurança e formulários web">
            </article>
        </main>

        <aside>
            <h3>Inscrição na Newsletter</h3>
            <form action="" method="get">
                
                <!-- BÔNUS: Nome e E-mail agrupados na mesma linha com flexbox -->
                <div class="form-row">
                    <div class="form-group-inline">
                        <label for="nome">Nome:</label>
                        <input type="text" id="nome" name="nome" minlength="3" required placeholder="Seu nome">
                    </div>

                    <div class="form-group-inline">
                        <label for="email">E-mail:</label>
                        <input type="email" id="email" name="email" required placeholder="seu@email.com">
                    </div>
                </div>

                <div class="form-group">
                    <label for="idade">Idade:</label>
                    <input type="number" id="idade" name="idade" min="18" max="120" required placeholder="De 18 a 120">
                </div>

                <div class="form-group">
                    <label for="assunto">Assunto de Interesse:</label>
                    <select id="assunto" name="assunto">
                        <option value="html">HTML5 & CSS3</option>
                        <option value="javascript">JavaScript</option>
                        <option value="carreira">Carreira em Tech</option>
                    </select>
                </div>

                <div class="checkbox-group">
                    <input type="checkbox" id="termos" name="termos" required>
                    <label for="termos">Aceito os termos de privacidade</label>
                </div>

                <button type="submit">Inscrever-se</button>
            </form>
        </aside>

    </div>

    <footer>
        <p>&copy; 2026 DevBlog. Todos os direitos reservados.</p>
    </footer>

</body>
</html>
```
