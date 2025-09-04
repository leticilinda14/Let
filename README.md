# Site acessível sobre Tropicália

## Sobre
Este projeto consiste na refatoração de um site sobre o movimento Tropicália, implementando recursos de acessibilidade em HTML, CSS e JavaScript. O objetivo é promover uma navegação inclusiva para todos os usuários, atendendo a boas práticas de acessibilidade web.

## Recursos de acessibilidade
- Utilização de atributos `aria` para melhor compreensão por leitores de tela.
- Inclusão de textos alternativos (`alt`) em imagens.
- Uso de `tabindex` para navegação eficiente via teclado.
- Implementação de menu de acessibilidade para facilitar ajustes e acessos rápidos.

## Tecnologias utilizadas
- [Bootstrap](https://getbootstrap.com/): Framework CSS para design responsivo.
- [ScrollReveal.js](https://scrollrevealjs.org/): Biblioteca JS para animações ao rolar a página.
- HTML5
- CSS3
- JavaScript

## Como contribuir
Sinta-se à vontade para enviar sugestões, abrir issues ou fazer pull requests!

## Licença
Este projeto está sob a licença MIT.

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Site Acessível sobre Tropicália</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css">
</head>
<body>
    <header>
        <h1>Tropicália</h1>
        <nav>
            <ul>
                <li><a href="#sobre" tabindex="0">Sobre</a></li>
                <li><a href="#recursos" tabindex="0">Recursos</a></li>
                <li><a href="#contato" tabindex="0">Contato</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="sobre">
            <h2>Sobre o Movimento</h2>
            <p>O movimento Tropicália foi uma revolução cultural brasileira que misturou música, artes e política...</p>
            <img src="assets/tropicalia.jpg" alt="Cartaz do movimento Tropicália" tabindex="0">
        </section>

        <section id="recursos">
            <h2>Recursos de Acessibilidade</h2>
            <ul>
                <li>Atributos ARIA</li>
                <li>Textos alternativos em imagens</li>
                <li>Navegação por teclado (tabindex)</li>
                <li>Menu de acessibilidade</li>
            </ul>
        </section>

        <section id="contato">
            <h2>Contato</h2>
            <p>Entre em contato para mais informações sobre o projeto.</p>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 Site sobre Tropicália</p>
    </footer>

    <script src="script.js"></script>
    <script src="https://unpkg.com/scrollreveal"></script>
</body>
</html>

// Exemplo de ScrollReveal
ScrollReveal().reveal('section', { 
    delay: 200,
    distance: '50px',
    origin: 'bottom',
    duration: 1000
});

// Menu de acessibilidade (exemplo simples)
document.addEventListener('keydown', (e) => {
    if(e.key === 'Tab') {
        document.body.classList.add('focus-outline');
    }
});
