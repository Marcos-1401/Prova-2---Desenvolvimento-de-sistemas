RELATÓRIO DE PROJETO - SISTEMA DE ESTOQUE 

1) Nome da Aplicação: 
   Gerenciador Integrado de Estoque (GUI + API)

2) Descrição das Funcionalidades:
   O sistema permite o gerenciamento completo (CRUD) de um estoque de produtos.
   
   - Banco de Dados Relacional: Utiliza SQLite com duas tabelas ('produtos' e 'categorias') ligadas por chave estrangeira para garantir a integridade dos dados.
   - Interface Gráfica (GUI): Desenvolvida em Tkinter, oferece visualização em lista (Treeview), formulários para inserção/edição e botões de ação intuitivos com validação de dados.
   - API Local: Desenvolvida em Flask, oferece endpoints REST (GET, POST, DELETE) permitindo que sistemas externos acessem e modifiquem o mesmo banco de dados usado pela interface gráfica.
   - Modularização: O código foi refatorado utilizando Orientação a Objetos, separando a lógica de banco de dados da camada de apresentação.

3) Como Executar o Projeto:

   Pré-requisitos:
   - Python instalado.
   - Biblioteca Flask instalada (comando: pip install flask).

   Passo a Passo:
   1. Certifique-se de que os arquivos (db.py, gui.py, api.py, main.py) estão na mesma pasta.
   
   2. Para abrir a Interface Gráfica:
      - Abra o terminal na pasta do projeto.
      - Execute: python main.py
      - A janela abrirá, permitindo cadastrar e visualizar produtos.

   3. Para rodar a API (em paralelo):
      - Abra um SEGUNDO terminal na pasta.
      - Execute: python api.py
      - Acesse no navegador: http://127.0.0.1:5000/produtos para ver o JSON dos dados.

   As alterações feitas na Interface Gráfica aparecem instantaneamente na API e vice-versa, pois compartilham o 'Estoque.db'.
   
