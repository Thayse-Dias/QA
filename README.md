Realizar LOGIN com usuário inválido:

1.	Acessa o site https://www.saucedemo.com/ (cy.visit('https://www.saucedemo.com/')).
2.	Seleciona o campo de nome de usuário (cy.get('[data-test="username"]')).
3.	Insere um nome de usuário inválido (cy.type('usuario_invalido')).
4.	Seleciona o campo de senha (cy.get('[data-test="password"]')).
5.	Insere uma senha inválida (cy.type('senha_invalida')).
6.	Seleciona o botão de login (cy.get('[data-test="login-button"]')).
7.	Clica no botão de login (cy.click()).
8.	Verifica a presença de uma mensagem de erro (cy.get('[data-test="error"]')).
9.	Confirma que a mensagem de erro contém o texto "Username and password do not match any user in this service" (cy.get('[data-test="error"]').should('contain', 'Username and password do not match any user in this service')).
10.	Verifica a URL atual (cy.url()).
11.	Confirma que a URL deve ser https://www.saucedemo.com/inventory.html (cy.url().should('eq', 'https://www.saucedemo.com/inventory.html')).

Adicionando itens no carrinho de compras

1. Acesse o site https://www.saucedemo.com/ (cy.visit('https://www.saucedemo.com/')).
2. Selecione o campo de nome do usuário (cy.get('[data-test="username"]')).
3. Insira o nome de usuário válido (cy.type('standard_user')).
4. Selecione o campo de senha (cy.get('[data-test="password"]')).
5. Insira a senha válida (cy.type('secret_sauce')).
6. Selecione o botão de login (cy.get('[data-test="login-button"]')).
7. Clique no botão de login (cy.click()).
8. Selecione o botão "Add to cart" do produto "Sauce Labs Backpack" (cy.get('[data-test="add-to-cart-sauce-labs-backpack"]')).
9. Clique no botão "Add to cart" (cy.click()).
10. Verifique a presença do ícone do carrinho com o número de itens (cy.get('.shopping_cart_badge')).
11. Confirme que o ícone do carrinho está visível (cy.get('.shopping_cart_badge').should('be.visible')).
12. Confirme que o ícone do carrinho contém o texto "1" (cy.get('.shopping_cart_badge').should('have.text', '1')).
13. Selecione o ícone do carrinho (cy.get('#shopping_cart_container')).
14. Clique no ícone do carrinho (cy.click()).
15. Verifique a presença do produto "Sauce Labs Backpack" na página do carrinho (cy.contains('Sauce Labs Backpack')).
16. Confirme que o produto "Sauce Labs Backpack" está visível (cy.contains('Sauce Labs Backpack').should('be.visible')).

Explicação:

Arrange: Configura o estado inicial (navega até o site e faz login com credenciais válidas).

Act: Executa a ação de adicionar o produto "Sauce Labs Backpack" ao carrinho.

Assert: Verifica se o ícone do carrinho foi atualizado para "1" e se o produto aparece na página do carrinho.
