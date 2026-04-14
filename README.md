# 🧮 Calculadora Simples em Java

Este é um projeto básico de uma calculadora desenvolvida em Java. A aplicação funciona via terminal e permite realizar as quatro operações matemáticas fundamentais: adição, subtração, multiplicação e divisão.

## 📌 Funcionalidades

- ➕ Adição
- ➖ Subtração
- ✖️ Multiplicação
- ➗ Divisão
- ⌨️ Entrada de dados pelo teclado
- 📟 Exibição do resultado no console
- ⚠️ Tratamento de operação inválida

## 🛠️ Tecnologias Utilizadas

- Java
- Biblioteca Scanner (java.util.Scanner)
- Estrutura de decisão switch-case
- Programação básica em linha de comando

## 📂 Estrutura do Projeto

Calculadora-Java/
│── src/
│   └── Main.java
└── README.md

## 📜 Código-Fonte

```java
import java.util.Scanner;

// click the <icon src="AllIcons.Actions.Execute"/> icon in the gutter.
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.println("Enter the first number:");
        double num1 = scanner.nextDouble();
        
        System.out.println("Enter the second number:");
        double num2 = scanner.nextDouble();
        
        System.out.println("Select the operation (+, -, *, /): ");
        char operation = scanner.next().charAt(0);
        
        scanner.close();
        double result;

        switch (operation) {
            case '+':
                result = num1 + num2;
                break;
            case '-':
                result = num1 - num2;
                break;
            case '*':
                result = num1 * num2;
                break;
            case '/':
                result = num1 / num2;
                break;
            default:
                System.out.println("Invalid operation");
                return;
        }

        System.out.println("The result is: " 
                + num1 + " " + operation + " " + num2 + ": " + result);
    }
}
