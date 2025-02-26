# Desafio forEach - Busca de Contato

Este projeto é um pequeno desafio de JavaScript utilizando `forEach` para buscar contatos em uma lista pré-definida. O usuário pode inserir um nome no campo de entrada e clicar no botão para procurar o contato.

## 📌 Tecnologias Utilizadas
- HTML5
- CSS3
- JavaScript (ES6)

## 🚀 Como Usar
2. Abra o arquivo `index.html` no seu navegador.
3. Digite um nome no campo de entrada.
4. Clique no botão "Procurar Contato" para buscar na lista.

## 📜 Código Fonte
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Desafio_forEach</title>
</head>
<body>
    <input placeholder="Digite o nome do contato" id="nomeBusca" autocomplete="off">
    <button onclick="BuscarContato()">Procurar Contato</button>
    <p style="white-space: pre-wrap"></p>

    <script>
        let p = document.querySelector("p");
        let input = document.querySelector("#nomeBusca");

        const contacts = [
            { name: "Maria Bernadete", age: 40, number: "(74)9888-9999" },
            { name: "Bolsonaro", age: 41, number: "(74)9888-0000" },
            { name: "Dilma Roulseff", age: 42, number: "(74)9888-2222" },
            { name: "Cirilo", age: 43, number: "(74)9888-4444" }
        ];

        function BuscarContato() {
            let encontrado = contacts.find(contact => input.value.toLowerCase() === contact.name.toLowerCase());

            if (encontrado) {
                p.innerHTML = `Contato Encontrado, Nome: ${encontrado.name} Tel: ${encontrado.number}`;
            } else {
                p.innerHTML = "Contato não encontrado, tente novamente!";
            }
        }
    </script>
</body>
</html>
```

## 🛠 Melhorias Futuras
- Adicionar estilização com CSS.
- Criar um banco de dados para armazenar contatos.
- Implementar busca dinâmica conforme o usuário digita.


