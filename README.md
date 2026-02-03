# 🎮 AluGames - Aluguel de Boardgames

Projeto desenvolvido durante o curso **Lógica de programação: praticando com desafios**, da plataforma **Alura**.

Este projeto consiste em uma página interativa para aluguel de jogos de tabuleiro (boardgames), onde o usuário pode alternar o status de cada jogo entre "Alugar" e "Devolver" com feedback visual.

---

## 📌 Sobre o projeto

O AluGames é uma interface simples e intuitiva que simula um sistema de aluguel de jogos. O usuário pode clicar nos botões dos jogos para alugá-los ou devolvê-los, com mudanças visuais que indicam claramente o status de cada item.

---

## 🎮 Funcionalidades

- ✅ Alternar status de jogos (Disponível ↔ Alugado)
- ✅ Feedback visual ao alugar (imagem escurecida)
- ✅ Mudança de cor do botão conforme status
- ✅ Mudança de texto do botão (Alugar ↔ Devolver)
- ✅ Sistema responsivo e interativo

---

## 🎯 Como funciona

### Estado Inicial
- **Monopoly** e **Ticket to Ride**: Disponíveis para alugar (botão azul)
- **Takenoko**: Já alugado (imagem escurecida, botão cinza "Devolver")

### Ao clicar em "Alugar"
- Imagem do jogo fica escurecida (overlay escuro)
- Botão muda para cinza
- Texto muda para "Devolver"

### Ao clicar em "Devolver"
- Imagem do jogo volta ao normal
- Botão muda para azul
- Texto muda para "Alugar"

---

## 🧠 Conceitos praticados

### Manipulação do DOM
- `document.getElementById()` - Selecionar elementos por ID
- `element.querySelector()` - Buscar elementos dentro de um elemento específico
- `classList.contains()` - Verificar presença de classe CSS
- `classList.add()` / `classList.remove()` - Adicionar/remover classes
- `textContent` - Alterar texto de elementos

### JavaScript
- Funções com parâmetros
- Estruturas condicionais (`if/else`)
- Manipulação de classes CSS dinamicamente
- Event handling com `onclick`

### Lógica de Programação
- Controle de estado (disponível vs alugado)
- Alternância de estados (toggle)
- Seleção de elementos específicos

---

## 🛠️ Tecnologias utilizadas

- **HTML5** - Estrutura da página (fornecida pela Alura)
- **CSS3** - Estilização visual (fornecida pela Alura)
- **JavaScript** - Interatividade e lógica (desenvolvido durante o curso)

---

## 📂 Estrutura do projeto
```text
📁 alugames
 ├── 📁 css
 │   ├── main.css
 │   └── _reset.css
 ├── 📁 img
 │   ├── logo.svg
 │   ├── monopoly.png
 │   ├── ticket_to_ride.png
 │   ├── takenoko.png
 │   ├── fade_bar.svg
 │   └── hachuras.svg
 ├── 📁 js
 │   └── app.js
 ├── index.html
 └── README.md
```

---

## ▶️ Como executar

### Opção 1: Abrir diretamente
1. Faça o download dos arquivos do projeto
2. Abra o arquivo `index.html` em seu navegador

### Opção 2: Live Server (VS Code)
1. Instale a extensão "Live Server" no VS Code
2. Clique com botão direito em `index.html`
3. Selecione "Open with Live Server"

---

## 💻 Código JavaScript

A lógica principal do projeto está na função `alterarStatus()`:
```javascript
function alterarStatus(id){
    let gameClicado = document.getElementById(`game-${id}`);
    let imagem = gameClicado.querySelector('.dashboard__item__img');
    let botao = gameClicado.querySelector('.dashboard__item__button');

    if (imagem.classList.contains('dashboard__item__img--rented')){
        imagem.classList.remove('dashboard__item__img--rented')
        botao.classList.remove('dashboard__item__button--return');
        botao.textContent = "Alugar";
    } else{
        imagem.classList.add('dashboard__item__img--rented')
        botao.textContent = "Devolver";
        botao.classList.add('dashboard__item__button--return');
    }
}
```

### Explicação do código:
1. Seleciona o jogo clicado pelo ID
2. Busca a imagem e o botão dentro desse jogo específico
3. Verifica se o jogo está alugado (classe `dashboard__item__img--rented`)
4. Se estiver alugado: remove classes e muda texto para "Alugar"
5. Se não estiver: adiciona classes e muda texto para "Devolver"

<img width="1919" height="1018" alt="image" src="https://github.com/user-attachments/assets/11196c97-1bff-4d42-a52e-7e8550c7f8af" />

---

## 🎓 Aprendizados

- ✅ Seleção precisa de elementos no DOM usando `querySelector()` dentro de elementos específicos
- ✅ Diferença entre `innerHTML` e `textContent`
- ✅ Manipulação dinâmica de classes CSS
- ✅ Controle de estado com estruturas condicionais
- ✅ Importância de selecionar o elemento correto (evitar `document.querySelector()` genérico)

---

## 📚 Curso de referência

- **Lógica de programação: praticando com desafios**
- **Plataforma:** Alura
- **Foco:** JavaScript e manipulação do DOM
- **Tipo:** Desafio prático

---

## 👨‍💻 Autor

[<img loading="lazy" src="https://github.com/user-attachments/assets/b4f96f4b-542e-4988-9bc1-b1acf22a41a1" width=115><br><sub>Renan Dias Utida</sub>](https://github.com/renan-utida)

**Renan Dias Utida**  
Estudante de Engenharia de Software

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/renan-dias-utida-1b1228225/)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/renan-utida)

---

## 📄 Licença

Este projeto foi desenvolvido exclusivamente para fins educacionais durante o curso da Alura.

---

## 📝 .gitignore
```gitignore
# Arquivos do sistema
.DS_Store
Thumbs.db

# Arquivos do VS Code
.vscode/
```
