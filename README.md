<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login com Imagem</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f0f0f0;
        }
        .login-container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            width: 300px;
            text-align: center;
        }
        .login-container h1 {
            margin-bottom: 20px;
        }
        .login-container input {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .login-container button {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .login-container button:hover {
            background-color: #0056b3;
        }
        #success-image {
            margin-top: 20px;
            display: none;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h1>Login</h1>
        <form onsubmit="validateLogin(event)">
            <input type="text" id="username" placeholder="Usuário" required>
            <input type="password" id="password" placeholder="Senha" required>
            <button type="submit">Entrar</button>
        </form>
        <p id="error-message" style="color: red; display: none;">Usuário ou senha incorretos!</p>
        <!-- Espaço para exibir a imagem -->
        <img id="AMOR" src="C:\Users\vanes\Downloads\AMOR.jpg" alt="Imagem de Sucesso" width="300">
    </div>

    <script>
        function validateLogin(event) {
            event.preventDefault(); // Evita o envio do formulário padrão

            // Login e senha pré-definidos
            const correctUsername = "AMANDA66";
            const correctPassword = "Guilherme66";

            // Valores inseridos pelo usuário
            const enteredUsername = document.getElementById("username").value;
            const enteredPassword = document.getElementById("password").value;

            // Validação
            if (enteredUsername === correctUsername && enteredPassword === correctPassword) {
                alert("Login bem-sucedido!");
                const successImage = document.getElementById("success-image");
                successImage.style.display = "block"; // Exibe a imagem
            } else {
                const errorMessage = document.getElementById("error-message");
                errorMessage.style.display = "block"; // Exibe mensagem de erro
            }
        }
    </script>
</body>
</html>
