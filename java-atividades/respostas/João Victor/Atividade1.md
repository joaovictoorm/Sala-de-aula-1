# Atividade 1 — Conta Bancária
```java
public class ContaBancaria {

    // Atributos
    String titular;
    int numeroConta;
    double saldo;

    // Método para depositar
    public void depositar(double valor) {
        if (valor > 0) {
            saldo += valor;
            System.out.println("Depósito realizado!");
        } else {
            System.out.println("Valor inválido!");
        }
    }

    // Método para sacar
    public void sacar(double valor) {
        if (valor > 0 && valor <= saldo) {
            saldo -= valor;
            System.out.println("Saque realizado!");
        } else {
            System.out.println("Saldo insuficiente ou valor inválido!");
        }
    }

    // Método para exibir saldo
    public void exibirSaldo() {
        System.out.println("Titular: " + titular);
        System.out.println("Conta: " + numeroConta);
        System.out.println("Saldo: R$ " + saldo);
    }
}
```

## Código do Main

```java
public class Main {
    public static void main(String[] args) {

        // Criando o objeto
        ContaBancaria conta1 = new ContaBancaria();

        // Definindo os atributos
        conta1.titular = "João Victor";
        conta1.numeroConta = 2026220108;
        conta1.saldo = 1000;

        // Exibindo saldo inicial
        conta1.exibirSaldo();

        // Realizando depósito
        conta1.depositar(200);

        // Realizando saque
        conta1.sacar(100);

        // Exibindo saldo atualizado
        conta1.exibirSaldo();
    }
}
```
