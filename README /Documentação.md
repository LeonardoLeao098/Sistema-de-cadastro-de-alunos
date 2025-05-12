Documentação do Sistema de Cadastro em Python (modo console)

Descrição Geral
Este é um sistema simples de cadastro de pessoas feito em Python, executado via console, com armazenamento dos dados em arquivo .json. Ele permite:

Cadastrar uma nova pessoa com dados pessoais e notas.

Armazenar os dados localmente de forma estruturada.

Listar todos os cadastros realizados.

Alterar um cadastro existente (com verificação de senha).

O sistema é útil para fins educacionais e foi feito com foco em praticar conceitos de lógica, estruturação de dados e manipulação de arquivos com Python.

Estrutura do Projeto
dados.json: Arquivo onde todos os dados dos cadastros são armazenados.

Funções principais:

carregar_dados()

salvar_dados(lista)

cadastrar_pessoa()

listar_pessoas()

alterar_cadastro()

menu()

Descrição das Funções
carregar_dados()
Verifica se o arquivo dados.json existe.

Se existir, lê e carrega os dados em formato de lista de dicionários.

Se não existir, retorna uma lista vazia.

salvar_dados(lista)
Salva a lista de pessoas (cadastros) no arquivo dados.json no formato JSON com indentação.

cadastrar_pessoa()
Coleta informações pessoais do usuário (nome, CPF, e-mail, etc.).

Solicita três notas: nota1, nota2 e trabalho.

Exige que o usuário crie uma senha com no mínimo 8 caracteres, que será usada para alterações futuras.

Exibe uma declaração de consentimento sobre uso educacional dos dados.

Se o usuário confirmar a declaração, os dados são salvos.

listar_pessoas()
Carrega os cadastros e exibe os dados de cada pessoa cadastrada.

Usa get() para evitar erros caso algum campo esteja ausente.

alterar_cadastro()
Solicita o CPF do usuário cujo cadastro será alterado.

Verifica se o CPF existe nos dados.

Solicita a senha do cadastro antes de permitir alterações.

Permite editar todos os campos (basta deixar em branco para manter o valor atual).

Salva os dados atualizados.

menu()
Exibe o menu principal do sistema com as opções:

1: Cadastrar

2: Listar

3: Alterar

4: Sair

Chama a função correspondente com base na escolha do usuário.

Segurança e Validação
Senha obrigatória com no mínimo 8 caracteres.

A alteração de dados só é permitida mediante autenticação por senha.

O CPF é usado como chave de identificação única de cada pessoa no sistema.

Dados são persistidos localmente, não são enviados para nenhum servidor.

========================================================================

English Version

Documentation of the Python Console-Based Registration System

General Description
This is a simple person registration system written in Python and executed through the console, with data stored in a .json file. It allows users to:

Register a new person with personal information and grades.

Store the data locally in a structured way.

List all registered users.

Edit an existing registration (with password verification).

The system is intended for educational purposes and was developed to practice concepts such as logic, data structuring, and file handling in Python.

Project Structure
dados.json: File where all user data is stored.

Main Functions:

carregar_dados() (load data)

salvar_dados(lista) (save data)

cadastrar_pessoa() (register person)

listar_pessoas() (list people)

alterar_cadastro() (edit registration)

menu() (main menu)

Function Descriptions
carregar_dados()
Checks if the dados.json file exists.

If it does, it loads the data as a list of dictionaries.

If not, it returns an empty list.

salvar_dados(lista)
Saves the list of people (registrations) into the dados.json file using JSON format with indentation.

cadastrar_pessoa()
Collects personal information from the user (name, CPF, email, etc.).

Asks for three grades: nota1, nota2, and trabalho.

Requires the user to create a password with at least 8 characters, which will be used to authorize future edits.

Displays a data use declaration informing the user the data is for educational purposes only.

If the user confirms, the data is saved.

listar_pessoas()
Loads the registrations and displays the data of each person.

Uses get() to safely access fields, avoiding errors if some data is missing.

alterar_cadastro()
Asks for the CPF of the person whose registration is to be updated.

Searches for the CPF in the data.

Requests the password before allowing any modifications.

Allows all fields to be edited (leaving blank keeps the current value).

Saves the updated data back to the file.

menu()
Displays the system's main menu with the following options:

1: Register

2: List

3: Edit

4: Exit

Calls the corresponding function based on the user's input.

Security and Validation
Password must be at least 8 characters long.

Data editing is only allowed with password authentication.

CPF is used as a unique identifier key for each person in the system.

All data is stored locally and not sent to any server.
