# Projeto Conta Bancária

<h2>1. O Projeto Conta Bancária</h2>

Diagrama de Classes do Projeto Conta Bancária completo na figura abaixo:

```mermaid
classDiagram
class Conta {
<<Abstract>>
  - numero : int
  - agencia : int
  - tipo : int
  - titular : String
  - saldo : float
  + int getNumero()
  + int getAgencia()
  + int getTipo()
  + String getTitular()
  + float getSaldo()
  + void setNumero(int numero)
  + void setAgencia(int agencia)
  + void setTipo(int tipo)
  + void setTitular(String titular)
  + void setSaldo(float saldo)
  + boolean sacar(float valor)
  + void depositar(float valor)
  + void visualizar()
}
class ContaCorrente {
  - limite : float
  + float getLimite()
  + void setLimite(float limite)
  + boolean sacar(float valor)
  + void visualizar()
}
class ContaPoupanca {
  - aniversario : int
  + int getAniversario()
  + void setAniversario(int aniversario)
  + void visualizar()
}
class ContaRepository{
<< Interface >>
+ void procurarPorNumero(int numero)
+ void listarTodas()
+ void cadastrar(Conta conta)
+ void atualizar(Conta conta)
+ void deletar(int numero)
+ void sacar(int numero, float valor)
+ void depositar(int numero, float valor)
+ void transferir(int numeroOrigem, int numeroDestino, float valor)
}
class ContaController{
+ void procurarPorNumero(int numero)
+ void listarTodas()
+ void cadastrar(Conta conta)
+ void atualizar(Conta conta)
+ void deletar(int numero)
+ void sacar(int numero, float valor)
+ void depositar(int numero, float valor)
+ void transferir(int numeroOrigem, int numeroDestino, float valor)
+ int gerarNumero()
+ Conta buscarNaCollection(int numero)
+ int retornaTipo(int numero)
}
Conta <|-- ContaCorrente
Conta <|-- ContaPoupanca
Conta <.. ContaRepository
ContaRepository <|.. ContaController
```

<br />

O Projeto será composto pelas seguintes Classes e Interfaces:

| Classe/Interface    | Descrição                                                    |
| ------------------- | ------------------------------------------------------------ |
| **Menu**            | Classe principal, que conterá o Método main, responsável por criar o Menu inicial da aplicação com todas as funcionalidades do sistema. |
| **Cores**           | Classe utilitária, que possui a função de aplicar cores ao Menu. |
| **Conta**           | Classe responsável por definir o Objeto Conta genérico.      |
| **ContaCorrente**   | Classe responsável por definir o Objeto Conta Corrente.      |
| **ContaPoupanca**   | Classe responsável por definir o Objeto Conta Poupanca.      |
| **ContaRepository** | Interface responsável por encapsular os Métodos que serão utilizados no Menu da aplicação |
| **ContaController** | Classe responsável por implementar a Interface ContaRepository. |


<h2>2. Como executar o Projeto Conta Bancária</h2>

### Pré-requisitos

Certifique-se de que você tenha o seguinte instalado em seu sistema:

       [Spring Tool Suite 4]
***
## Passo 1: Clonar o Repositório

Abra um terminal ou prompt de comando. <br/>
Navegue até o diretório onde você deseja clonar o repositório. <br/>
Execute o seguinte comando para clonar o repositório:

```
git clone https://github.com/RitaAlmeidah/ContaBancaria.git
```

Aguarde até que o processo de clonagem seja concluído.

***
## Passo 2: Entrar na Pasta do Projeto

Após a conclusão da clonagem, abra o arquivo no Spring Tool Suite 4.

***
## Passo 3: Executar o Projeto

Para executarmos o Projeto, clique no botão <img src="https://i.imgur.com/t28CIT4.png" title="source: imgur.com" width="4%"/>**Run**, na **Barra de Ferramentas**

***
## Autora:

- Rita Almeida(https://github.com/RitaAlmeidah))





