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
