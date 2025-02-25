                  README - Sistema de Cadastro de Usuários
Este projeto é um simples sistema de cadastro de usuários, desenvolvido em PHP com a integração de banco de dados MySQL. O sistema permite realizar as operações básicas de CRUD (Criar, Ler, Atualizar e Deletar) para o gerenciamento de usuários.
Estrutura do Projeto
O sistema é composto pelos seguintes arquivos PHP:
1. index.php
Página inicial do sistema, onde é exibida a lista de usuários cadastrados. Permite a adição de um novo usuário, edição e exclusão de usuários existentes.
2. usuario-create.php
Página de criação de um novo usuário. Um formulário permite a inserção dos dados do usuário, como nome, e-mail, data de nascimento e senha.
3. usuario-edit.php
Página de edição de um usuário. Permite atualizar as informações de um usuário existente, como nome, e-mail, data de nascimento e senha.
4. usuario-view.php
Página para visualizar os detalhes de um usuário. Exibe informações como nome, e-mail e data de nascimento.
5. mensagem.php
Responsável por exibir mensagens de sucesso ou erro após uma ação, como criar, editar ou excluir um usuário. As mensagens são passadas por meio da variável $_SESSION.
6. acoes.php
Arquivo responsável pelo processamento das ações de CRUD. Ele recebe as solicitações de criação, atualização e exclusão de usuários, manipula os dados e interage com o banco de dados.
7. conexao.php
Arquivo responsável pela conexão com o banco de dados MySQL. Contém as credenciais de acesso ao banco de dados (host, usuário, senha e nome do banco de dados).
8. navbar.php
Barra de navegação que aparece em todas as páginas do sistema, permitindo fácil acesso às páginas principais.
Funcionalidades
- Listagem de Usuários (index.php)
Na página inicial, é exibida uma tabela com todos os usuários cadastrados, apresentando suas informações como ID, nome, e-mail e data de nascimento. A partir dessa página, é possível editar ou excluir um usuário.
- Cadastro de Novo Usuário (usuario-create.php)
Na página de criação, é possível adicionar um novo usuário ao sistema preenchendo um formulário com os campos de nome, e-mail, data de nascimento e senha.
- Edição de Usuário (usuario-edit.php)
Na página de edição, um formulário pré-preenchido permite alterar os dados do usuário, como nome, e-mail e data de nascimento. A senha pode ser alterada, mas é opcional.
- Visualização de Usuário (usuario-view.php)
A página de visualização mostra as informações completas de um usuário, como nome, e-mail e data de nascimento.
- Exclusão de Usuário
Na página de listagem de usuários (index.php), há a opção de excluir um usuário. A exclusão é confirmada por um prompt de confirmação, garantindo que a exclusão não seja feita sem o consentimento do usuário.
Como Usar
1. Configuração do Banco de Dados
Certifique-se de ter um banco de dados MySQL configurado. No arquivo conexao.php, as credenciais de acesso ao banco de dados são definidas:
define('HOST', '127.0.0.1');
define('USUARIO', 'root');
define('SENHA', 'srilanka');
define('DB', 'canalti');
Substitua os valores conforme a configuração do seu ambiente.
2. Criação da Tabela usuarios
A estrutura da tabela usuarios deve ser criada no banco de dados. Abaixo está um exemplo de como criar a tabela:
CREATE TABLE usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    data_nascimento DATE NOT NULL,
    senha VARCHAR(255) NOT NULL
);
3. Ações CRUD
    • Criar Usuário: Clique no botão "Adicionar usuário" na página inicial e preencha o formulário. 
    • Editar Usuário: Clique no botão "Editar" ao lado do usuário que deseja editar. 
    • Visualizar Usuário: Clique no botão "Visualizar" para ver os detalhes completos do usuário. 
    • Excluir Usuário: Clique no botão "Excluir" e confirme a exclusão. 
Requisitos
    • PHP 7.0 ou superior 
    • Servidor Web (ex: Apache) 
    • Banco de Dados MySQL 
    • Bootstrap 5 para a interface de usuário (CDN) 
Dependências
    • Bootstrap 5: Utilizado para o design responsivo da interface. 
    • Bootstrap Icons: Para os ícones utilizados nas ações de visualização, edição e exclusão de usuários. 
Segurança
    • Hash de Senha: As senhas dos usuários são armazenadas de forma segura utilizando o algoritmo password_hash() do PHP. 
    • Proteção contra SQL Injection: As entradas do usuário são tratadas com mysqli_real_escape_string() para evitar SQL Injection. 
    • Sessões para Mensagens de Sucesso e Erro: As mensagens de status são armazenadas nas variáveis de sessão para exibição. 
Considerações Finais
Este sistema pode ser utilizado como base para sistemas mais complexos de gerenciamento de usuários. Ele oferece uma interface simples para cadastro e gestão de informações de usuários, e pode ser expandido conforme as necessidades do seu projeto.
Autor
Desenvolvido por Danilo Cavalcante Lima

Este é um modelo básico de um CRUD em PHP com operações de gerenciamento de usuários.
        
