# en-US
## Project Challenge
This project is the solution to a challenge. The classes and methods names were named in portuguese because the initial source code and the challenge were provided by a brazilian tech organization.

## Context
You are working on a system, and your managers have reported frequent issues with the software: bugs, functionalities that were working suddenly stop, validation problems, etc. Customers are beginning to doubt the quality of the code.

Given this, you suggested the implementation of unit tests: writing tests covering the most critical parts of the system, with positive and negative scenarios, in order to have traceability and control of the code, thus improving the quality of this system.

The managers accepted your idea, and with that, you need to implement unit tests in the system.

## Assumptions
The system today has two projects: a console type, and a test type with **xUnit**. The console type project has two classes where the main logic is carried out: **ValidacoesLista** and **ValidacoesString**. These classes contain common methods that are used to perform various validations in certain scenarios.

The test project has the test classes **ValidacoesListaTests** and **ValidacoesStringTests**, as well as their methods to validate the console type project, but they are incomplete.

Your goal is to implement the test methods contained in the project.

## Console Project, its Classes and Methods

These are the classes of the console project, where the main logic of the system resides.

**ValidacoesLista Class**

Class responsible for performing various validations involving lists.

| Class            | Method                       | Objective                                                                                                                 |
|----------------- |----------------------------- |------------------------------------------------------------------------------------------------------------------------- |
| ValidacoesLista  | RemoverNumerosNegativos      | Receives a list of integers and returns a new list, only with positive numbers                                           |
| ValidacoesLista  | ListaContemDeterminadoNumero | Receives a list of integers and checks if a certain number is present within that list                                   |
| ValidacoesLista  | MultiplicarNumerosLista      | Receives a list of integers and returns a new list, with its values multiplied by a certain number                       |
| ValidacoesLista  | RetornarMaiorNumeroLista     | Receives a list of integers and returns the highest number among them                                                    |
| ValidacoesLista  | RetornarMenorNumeroLista     | Receives a list of integers and returns the lowest number among them                                                     |

**ValidacoesString Class**

Class responsible for performing various validations involving strings.

| Class            | Method                       | Objective                                                                                                                 |
|----------------- |----------------------------- |-------------------------------------------------------------------------------------------------------------------------- |
| ValidacoesString | RetornarQuantidadeCaracteres | Receives any text and returns the number of characters present in the text                                                |
| ValidacoesString | ContemCaractere              | Receives any text and a text to be searched, returns true or false if a certain searched snippet is present in the text   |
| ValidacoesString | TextoTerminaCom              | Receives any text and a snippet to be searched, returns true or false if a certain searched snippet is present only at the end of the text |

## Test Project, its Classes and Methods

**ValidacoesListaTests Class**

Class responsible for testing the ValidacoesLista class.

| Class                 | Test Method                                 | Expected Test Result                                                                                                      |
|---------------------- |-------------------------------------------- |------------------------------------------------------------------------------------------------------------------------- |
| ValidacoesListaTests  | DeveRemoverNumerosNegativosDeUmaLista       | When passing a list with several numbers, including positive and negative, it should return a new list only with positive numbers |
| ValidacoesListaTests  | DeveConterONumero9NaLista                   | When passing a list with several numbers, including the number 9, it should return true, as it found the 9 in the list  |
| ValidacoesListaTests  | NaoDeveConterONumero10NaLista               | When passing a list with several numbers, but without the number 10, it should return false, as it did not find the 10 in the list |
| ValidacoesListaTests  | DeveMultiplicarOsElementosDaListaPor2       | When passing a list of integers, it should return a new list, with all elements of the list multiplied by 2              |
| ValidacoesListaTests  | DeveRetornar9ComoMaiorNumeroDaLista         | When passing a list of integers, the largest being 9, it should return 9 as the largest element within that list         |
| ValidacoesListaTests  | DeveRetornarOitoNegativoComoMenorNumeroDaList | When passing a list of integers, the smallest being -8, it should return -8 as the smallest element within that list     |

**ValidacoesStringTests Class**

Class responsible for testing the ValidacoesString class.

| Class                  | Test Method                                  | Expected Test Result                                                                                                      |
|----------------------- |--------------------------------------------- |-------------------------------------------------------------------------------------------------------------------------- |
| ValidacoesStringTests  | DeveRetornar6QuantidadeCaracteresDaPalavraMatrix | When passing a text written with the word "Matrix", it should return the number 6, representing 6 characters present in the word |
| ValidacoesStringTests  | DeveContemAPalavraQualquerNoTexto            | When passing a text written "This is any text" and searching for the word "any", it should return true because the word exists in the text |
| ValidacoesStringTests  | NaoDeveConterAPalavraTesteNoTexto            | When passing a text written "This is any text" and searching for the word "test", it should return false because the word does not exist in the text |
| ValidacoesStringTests  | TextoDeveTerminarComAPalavraProcurado        | When passing a text written "Beginning, middle, and end of the sought text" and searching for the word "sought", it should return true because the word exists in the text and is included at the end of the text |

## Project Structure

The project is structured as follows:

![Métodos Swagger](Imagens/projeto.png)

## Solution
The test code is halfway done, and you should continue implementing the tests described above, so that in the end, we have a functional test program. Look for the commented word "TODO" in the code, then implement it according to the above rules.

# pt-BR
## Desafio de projeto
Esse projeto é a solução de um desafio.

## Contexto
Você está trabalhando em um sistema, e seus gestores relataram que frequentemente há problemas no software: bugs, funcionalidades que estavam funcionando de repente não funcionam mais, problemas de validações, entre outros. Os clientes já começam a duvidar da qualidade do código.

Feito isso, você sugeriu a implementação de testes unitários: escrever testes cobrindo as partes mais críticas do sistema, com cenários positivos e negativos, a fim de ter uma rastreabilidade e controle do código, melhorando assim a qualidade desse sistema.

Os gestores aceitaram a sua ideia, e com isso, você precisa implementar testes unitários no sistema.

## Premissas
O sistema hoje possui dois projetos: um do tipo console, e um do tipo testes com **xUnit**. O projeto do tipo console possui duas classes em que são realizadas as lógicas principais: **ValidacoesLista** e **ValidacoesString**. Essas classes contém métodos em comum que são usados para realizar diversas validações em determinados cenários.

O projeto de testes possui as classes de teste **ValidacoesListaTests** e **ValidacoesStringTests**, assim como seus métodos para validar o projeto do tipo console, porém estão incompletos. 

O seu objetivo é implementar os métodos de testes contidos no projeto.

## Projeto Console, suas classes e métodos

Essas são as classes do projeto console, onde fica a principal lógica do sistema.

**Classe ValidaçõesLista**

Classe responsável por realizar diversas validações envolvendo listas.

| Classe          | Método                       | Objetivo                                                                                                                |
|---------------- |------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| ValidacoesLista | RemoverNumerosNegativos      | Recebe uma lista de números inteiros e retorna uma nova lista, apenas com os números positivos                          |
| ValidacoesLista | ListaContemDeterminadoNumero | Recebe uma lista de números inteiros e verifica se um determinado número está presente dentro dessa lista               |
| ValidacoesLista | MultiplicarNumerosLista      | Recebe uma lista de números inteiros e retorna uma nova lista, com seus valores múltiplicados por um determinado número |
| ValidacoesLista | RetornarMaiorNumeroLista     | Recebe uma lista de números inteiros e retorna o maior número entre eles                                                |
| ValidacoesLista | RetornarMenorNumeroLista     | Recebe uma lista de números inteiros e retorna o menor número entre eles                                                |

**Classe ValidacoesString**

Classe responsável por realizar diversas validações envolvendo strings.

| Classe           | Método                       | Objetivo                                                                                                                
|------------------|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesString | RetornarQuantidadeCaracteres | Recebe um texto qualquer e retorna a quantidade de caracteres presentes no texto                                                                           |
| ValidacoesString | ContemCaractere              | Recebe um texto qualquer e um texto a ser procurado, retorna verdadeiro ou falso se um determinado trecho procurado está presente no texto                 |
| ValidacoesString | TextoTerminaCom              | Recebe um texto qualquer e um trecho a ser procurado, retorna verdadeiro ou falso se um determinado trecho procurado está presente no final do texto apenas |

## Projeto do tipo teste, suas classes e métodos

**Classe ValidacoesListaTests**

Classe responsável por realizar os testes da classe ValidacoesLista.

| Classe               | Método de teste                               | Resultado esperado do teste
|----------------------|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesListaTests | DeveRemoverNumerosNegativosDeUmaLista         | Ao passar uma lista com diversos números, incluindo positivos e negativos, deve ser retornado uma nova lista apenas com números positivos  |
| ValidacoesListaTests | DeveConterONumero9NaLista                     | Ao passar uma lista com diversos números, incluindo o número 9, deve retornar verdadeiro, pois encontrou o 9 na lista                      |
| ValidacoesListaTests | NaoDeveConterONumero10NaLista                 | Ao passar uma lista com diversos números, mas sem o número 10, deve retornar falso, pois não encontrou o 10 na lista                       |
| ValidacoesListaTests | DeveMultiplicarOsElementosDaListaPor2         | Ao passar uma lista de inteiros, deve retornar uma nova lista, com todos os elementos da lista multiplicados por 2                         |
| ValidacoesListaTests | DeveRetornar9ComoMaiorNumeroDaLista           | Ao passar uma lista de números inteiros, sendo o maior deles 9, deve retornar o 9 como maior elemento dentro dessa lista                   |
| ValidacoesListaTests | DeveRetornarOitoNegativoComoMenorNumeroDaList | Ao passar uma lista de números inteiros, sendo o menor deles -8, deve retornar o -8 como menor elemento dentro dessa lista                 |

**Classe ValidacoesStringTests**

Classe responsável por realizar os testes da classe ValidacoesString.

| Classe                | Método de teste                                  | Resultado esperado do teste
|---------------------- |--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ValidacoesStringTests | DeveRetornar6QuantidadeCaracteresDaPalavraMatrix | Ao passar um texto escrito a palavra "Matrix", deve retornar o número 6, representando 6 caracteres presentes na palavra                                                                         |
| ValidacoesStringTests | DeveContemAPalavraQualquerNoTexto                | Ao passar um texto escrito "Esse é um texto qualquer" e procurar pela palavra "qualquer", deve retornar verdadeiro pois a palavra existe no texto                                                |
| ValidacoesStringTests | NaoDeveConterAPalavraTesteNoTexto                | Ao passar um texto escrito "Esse é um texto qualquer" e procurar pela palavra "teste", deve retornar falso pois a palavra não existe no texto                                                    |
| ValidacoesStringTests | TextoDeveTerminarComAPalavraProcurado            | Ao passar um texto escrito "Começo, meio e fim do texto procurado" e procurar pela palavra "procurado", deve retornar verdadeiro pois a palavra existe no texto e está inclusa no final do texto |

## Estrutura do projeto

O projeto está estruturado da seguinte maneira:

![Métodos Swagger](Imagens/projeto.png)


## Solução
O código de testes está pela metade, e você deverá dar continuidade implementando os testes descritos acima, para que no final, tenhamos um programa de testes funcional. Procure pela palavra comentada "TODO" no código, em seguida, implemente conforme as regras acima.
