# questoes-da-lista-
questao 2:

#include <stdio.h>

void conversao(int h, int m, int s);

int main() {
  int h, m, s;
  
  printf("Converta as horas e minutos em segundos:\n\n");
  
  printf("Digite a hora: ");
  scanf("%d", &h);
  
  printf("Digite os minutos: ");
  scanf("%d", &m);
  
  printf("Digite os segundos: ");
  scanf("%d", &s);
  
  conversao(h, m, s);
  
  return 0;
}

void conversao(int h, int m, int s) {
  int c;
  
  c = (h * 60 * 60) + (m * 60) + (s);
  
  printf("\nO valor convertido corresponde a: %d segundos.", c);
  
}

questao 5:

#include <stdio.h>
#include <locale.h>

void numero();

int main() {
  setlocale(LC_ALL, "Portuguese_Brazil");
  
  numero();
}

void numero() {
  int valor;
  
  printf("Digite um valor: ");
  scanf("%d", &valor);
  
  if(valor < 0) {
    printf("Este número é negativo.");
  } else {
    printf("Este número é positivo.");
    
  }
  
}

questao 9.

#include <stdio.h>
#include <stdlib.h>
#include <locale.h>

int divisores(int num);

int main() {
  setlocale(LC_ALL, "Portuguese_Brazil");
  
  int N, R;
  
  printf("Digite um número inteiro e positivo: ");
  scanf("%d", &N);
  
  R = divisores(N);
  
  printf("A soma dos divisores do número é: %d", R);
}

int divisores(int num) {
  int div, soma = 0; 
  
  for(div = 1; div <= num; div++) {
    if(num % div == 0) {
      soma = soma + div; 
    }
  }
  
  return soma;
  
}
