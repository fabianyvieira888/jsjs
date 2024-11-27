<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ferramenta de Estudo</title>
    <style>
        /* Estilo base - Mobile First */
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            color: #333;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #6200ea;
            color: white;
            text-align: center;
            padding: 20px 10px;
        }

        .container {
            padding: 15px;
            margin: 0 auto;
        }

        textarea, input {
            width: 100%;
            margin-top: 10px;
            padding: 10px;
            font-size: 16px;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-sizing: border-box;
        }

        button {
            width: 100%;
            background-color: #6200ea;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
            margin-top: 10px;
        }

        button:hover {
            background-color: #3700b3;
        }

        .result {
            margin-top: 20px;
            padding: 10px;
            background-color: #f0f0f5;
            border-radius: 5px;
            border: 1px solid #ddd;
        }

        /* Ajustes para telas maiores (desktop) */
        @media (min-width: 768px) {
            .container {
                max-width: 800px;
                background: white;
                border-radius: 8px;
                box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
                padding: 20px;
                margin: 20px auto;
            }

            button {
                width: auto;
                padding: 10px 15px;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>Ferramenta de Estudo</h1>
        <p>Sua plataforma para aprender e organizar ideias!</p>
    </header>
    <div class="container">
        <h2>Faça uma pergunta ou digite um tópico</h2>
        <textarea id="questionInput" placeholder="Digite sua pergunta ou assunto..."></textarea>
        <button onclick="generateResponse()">Gerar Resposta</button>
        
        <div id="responseArea" class="result" style="display: none;">
            <h3>Resposta:</h3>
            <p id="responseText"></p>
        </div>
        
        <h2>Suas anotações</h2>
        <textarea id="notes" rows="5" placeholder="Escreva aqui suas anotações..."></textarea>
    </div>

    <script>
        function generateResponse() {
            const question = document.getElementById('questionInput').value;
            const responseArea = document.getElementById('responseArea');
            const responseText = document.getElementById('responseText');

            if (question.trim() === "") {
                responseText.innerText = "Por favor, insira uma pergunta ou tópico.";
            } else {
                // Simulação de resposta gerada por IA
                responseText.innerText = `Você perguntou: "${question}". Aqui está uma breve explicação: [insira conteúdo relevante].`;
            }
            responseArea.style.display = "block";
        }
    </script>
</body>
</html>
