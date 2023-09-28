
# **Desafio: Desenvolvimento de API RESTful**

## Descrição
	Você é um desenvolvedor .NET/Node.js em nossa equipe, e um novo projeto requer a criação de uma API RESTful para permitir a comunicação entre um aplicativo web (frontend) e um banco de dados. 
	Você deve criar endpoints RESTful para realizar operações CRUD (Criar, Ler, Atualizar e Excluir) em uma tabela descrita abaixo. Sua tarefa é implementar esses endpoints e garantir que  eles funcionem de maneira eficaz e segura.


## Tecnologias

- [Visual Studio 2022](https://visualstudio.microsoft.com/pt-br/downloads/)
- [.NET Core 7.0.0](https://dotnet.microsoft.com/pt-br/download/dotnet/7.0
- [xUnit 2.4.2(https://www.nuget.org/packages/xunit/2.4.2)
- [Microsoft.EntityFrameworkCore 7.0.10](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.InMemory/7.0.10)
- Fine Code Coverage(https://marketplace.visualstudio.com/items?itemName=FortuneNgwenya.FineCodeCoverage2022)

## Objetivo

Vamos construir uma API web CRUD de usuário simples utilizando o  TDD com xUnit e com conexão do banco de dados SQL SERVER.


## Checklist

**Modelo de Dados:**
- CREATE TABLE Pessoa ( ID INT PRIMARY KEY AUTO_INCREMENT, Nome VARCHAR(255) NOT NULL,
	Sobrenome VARCHAR(255), DataNascimento DATE, 
	Email VARCHAR(255) UNIQUE NOT NULL, 
	Telefone VARCHAR(20), Endereco VARCHAR(255), 
	Cidade VARCHAR(100), Estado VARCHAR(50), 
	CEP VARCHAR(10), CPF-CNPJ VARCHAR(14) );

>**Modelo gerado pelo Migrations**
 - **Como fazer:**
- 1o - criar no sql server banco de dados com nome **people**
- 2o - utilizando o codigo CREATE DATADASE people
- 3o - ir para console do Gerenciador de Pacotes
- 4o - rodar o comando: **update-database --verbose**
- 5o - verificar se não foi emitido nenhum erro após esse comando

>**Tarefas referente ao banco de dados:**
 - A tabela é chamada de Pessoa.
 - Ela possui uma coluna ID como chave primária, que é autoincrementada.
 - Há uma coluna Nome para armazenar o nome da pessoa (obrigatório).
 - Há uma coluna Sobrenome para armazenar o sobrenome da pessoa.
 - A coluna DataNascimento armazena a data de nascimento da pessoa.
 - A coluna Email armazena o endereço de e-mail da pessoa, com a restrição UNIQUE para garantir que não haja duplicatas.
 - A coluna Telefone armazena o número de telefone da pessoa.
 - As colunas Endereco, Cidade, Estado e CEP são usadas para armazenar informações de endereço;
 - A coluna CPFCNPJ é obrigatória.

**Endpoints RESTful:** 
>**Crie endpoints RESTful para as operações CRUD com base no modelo de dados fornecido. Certifique-se de que os endpoints sigam as melhores práticas de design RESTful.**

**Implementação da Lógica de Negócios:**
	- Implemente a lógica para validação de e-mail válido;
	- Implemente a lógica para identificar se é CPF ou CNPJ e se ele é válido ou não.

**Testes Unitários:**
	Escreva testes unitários para garantir que os endpoints funcionem conforme o esperado e que os casos de erro sejam tratados adequadamente.

**Autenticação/Autorização:**
	Não necessita desenvolver, mas explique como você faria a autenticação e autorização para proteger os endpoints e garantir que apenas usuários autorizados possam acessá-los.
 > Utilizaria um modelo de JWT
> - conforme no modelo no link: https://www.macoratti.net/19/06/aspnc_autjwt1.htm


