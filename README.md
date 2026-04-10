# 📚 Estudos de jQuery - Eventos (KeyUp, KeyDown, Click)

Este repositório foi criado com o objetivo de estudar e praticar **eventos em jQuery**, focando principalmente em:

* Eventos de teclado (`keyup` e `keydown`)
* Manipulação de elementos com `$(this)`
* Delegação de eventos com `.on()`
* Alteração de CSS dinamicamente

---

## 🚀 Tecnologias utilizadas

* HTML5
* CSS3
* jQuery

---

## 📂 Estrutura do Projeto

```
📁 jquery-eventos
 ┣ 📄 index.html
 ┣ 📄 script.js
 ┗ 📄 README.md
```

---

## 🧠 Conceitos aprendidos

### 1. Evento `keyup`

Disparado quando o usuário solta uma tecla.

```js
$('input[name=nome_pessoa]').keyup(func);
```

---

### 2. Alterando CSS com jQuery

```js
var func = function(){
    $(this).css('background','green');
}
```

👉 Aqui usamos `$(this)` para acessar o input que disparou o evento.

---

### 3. Pegando o índice do elemento

```js
var func = function(){
    console.log($(this).index());
}

$('input[type=text]').keyup(func);
```

👉 Retorna a posição do elemento entre os irmãos.

---

### 4. Evento `keydown`

```js
$('input[type=text]').keydown(func);
```

👉 Executa quando a tecla é pressionada (antes de soltar).

---

### 5. Evento de clique

```js
$('a').click(function(){
    alert('Olá mundo!');
});
```

---

### 6. Delegação de eventos (`.on()`)

```js
$('body').on('click','a',function(){
    alert('Olá mundo');
    return false;
});
```

👉 Muito útil para elementos criados dinamicamente.

---

### 7. Criando elementos dinamicamente

```js
setTimeout(function(){
    $('body').html('<a href="#">Meu link!</a>');
},3000);
```

👉 Após 3 segundos, um link é inserido na página.

---

## 💻 Código completo para estudo

### 📄 index.html

```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <title>Estudo jQuery</title>

    <!-- jQuery CDN -->
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
</head>
<body>

    <h2>Teste de Eventos</h2>

    <input type="text" name="nome_pessoa" placeholder="Digite seu nome">
    <input type="text" placeholder="Outro input">

    <script src="script.js"></script>

</body>
</html>
```

---

### 📄 script.js

```js
// Função principal usada nos eventos
var func = function(){
    // Muda a cor de fundo do input
    $(this).css('background','green');

    // Mostra o índice do input
    console.log($(this).index());
};

// Evento keyup
$('input[name=nome_pessoa]').keyup(func);

// Evento keyup para todos inputs de texto
$('input[type=text]').keyup(func);

// Evento keydown
$('input[type=text]').keydown(func);

// Evento de clique direto
$('a').click(function(){
    alert('Olá mundo!');
});

// Delegação de evento (funciona com elementos criados depois)
$('body').on('click','a',function(){
    alert('Olá mundo');
    return false;
});

// Criando elemento dinamicamente após 3 segundos
setTimeout(function(){
    $('body').html('<a href="#">Meu link!</a>');
},3000);
```

---

## 🎯 Objetivo do estudo

Aprender na prática como funcionam eventos em jQuery e como manipulá-los de forma eficiente, principalmente em situações reais onde elementos são criados dinamicamente.

---

## 📌 Próximos passos

* Estudar eventos de mouse (`hover`, `mouseenter`)
* Trabalhar com formulários
* Aprender AJAX com jQuery
* Migrar conhecimento para JavaScript puro (Vanilla JS)

---

## 👨‍💻 Autor

Pedro Souza

---

💡 *Dica: pratique alterando os eventos e testando no navegador!*
