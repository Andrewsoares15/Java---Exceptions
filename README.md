# Java---Exceptions
Meu aprendizado sobre Exceptions com Java <br>
As exceções ocorrem quando algum imprevisto acontece, elas podem ser provenientes de erros de lógica ou acesso a recursos que talvez não estejam disponíveis. <br>
Exemplos: Dividir um número por 0, tentar acessar um objeto inexistente e etc...

## Tratamento de Exceptions
Para tratar excessões utilizamos os comandos **Try** , **Catch**  e **Finally**.
 ```
  try
{
  //Código perigoso que pode vir a jogar uma exception
}
catch(nomeException ex)
{
  //"Pegando" a exception e definindo a ação a set tomada
} 
finally{
  // Encerrando
  }
  
  ```
## Existem dois tipos de Exceptions Checked e Uncheked.
Existe uma hierarquia grande de classes, uma Exception é "filha" da classe **RuntimeException** que também herda da classe **Exception**  que por sua vez <br>
Herda da classe mais genérica das Exceptions que é a **Throwable**.

**Checked**: São Exceptions que herdam diretamente da class Exception, o compilador verifica e te obriga a trata-lá seja colocando na assinatura do método a palavra chave **throws nomeException** ou fazendo o bloco Try, Catch para avisar que esse método pode lançar uma Exception. <br>
**UnChecked**: São Exceptions que herdam diretamente da class RuntimeException o compilador não te obriga a trata-la!

## Criando uma Exception!

```
public class NomeDaClasse extends RuntimeException // Exception Unchecked
  public NomeDaClasse(String s){ // devemos "aproveitar" os construtores da class Mãe.
        super(s);
  }

```

## Lançando uma Exception no método
```
  public void testando(){
  syos("Testando");
  throw new NullPointerException();
  }
```
**throw**: Usamos essa palavra chave do Java, quando queremos lançar uma Exception em algum lugar.
