import java.util.Scanner;

//Criar um Programa que mostre qual é o maior e o menor número inteiro digitado em uma sequência.
//O programa deverá receber a quantidade de elementos a serem digitados, bem como entrar com esses elementos.
//Em seguida, deverá exibir o maior e o menor número!
//Para isso deverá adotar os seguintes requisitos:
//Criar uma sub-rotina que recebe, como parâmetro, o vetor de inteiros, e preencher cada posição utilizando
//entrada padrão (Scanner);
//Criar uma sub-rotina chamada printMaiorNumero(), que recebe o vetor como parâmetro, verifique e
//imprima o maior número;
//Criar uma sub-rotina chamada printMaiorNumero(), que recebe o vetor como parâmetro, verifique e
//imprima o menor número;
//O método  principal (main) deverá:
//receber via teclado, a quantidade de elementos a serem preenchidos e criar um vetor de inteiros;
//Em seguida, deverá efetuar o preenchimento deste vetor;
//Com o uso das sub-rotinas (métodos) criadas, imprimir o maior e menor número digitado.

public class exercicios03 {

	public static void main(String[] args) {
		Scanner leitor = new Scanner(System.in);
		
		System.out.print("Digite a quantidade de elementos do vetor: ");
		int n = leitor.nextInt();
		
		int numeros[] = new int[n];
		
		preencherVetor(numeros);
		
		printMaiorNumero(numeros);
		
		printMenorNumero(numeros);		
		
		
		leitor.close();
		
	}
	
	public static void preencherVetor(int v[]) {
		Scanner leitor = new Scanner(System.in);
		
		for (int i = 0; i < v.length; i ++) {
			System.out.printf("v[%d] = ", i);
			v[i] = leitor.nextInt();
			
		}
		
		leitor.close();
		
	}
	
	public static void printMaiorNumero(int v[]) {
		
		int maior = 0;
		
		for (int i = 0; i < v.length; i ++) {
			
			if (i == 0) maior = v[i];
			
			if (v[i] > maior) maior = v[i];
			
		}
		
		System.out.printf("Maior número digitado: %d\n", maior);
		
	}
	
	public static void printMenorNumero(int v[]) {
		
		int menor = 0;
		
		for (int i = 0; i < v.length; i ++) {
			
			if (i == 0) menor = v[i];
			
			if (v[i] < menor ) menor = v[i];
			
		}
		
		System.out.printf("Menor número digitado: %d\n", menor);
	}

}
