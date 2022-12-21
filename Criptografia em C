#include <stdio.h>
#include <string.h>
#include <stdlib.h>

int main(void) {
  
  int i, tamanho = 0, numero, escolha = 3, n;
  int codigo[60], decodigo[60];
  char mensagem[60], mensagem2[60];
  char *chave, *confirmacaochave; //valor fixo

  printf("digite o tamanho da chave: ");
  scanf("%d", &n);  
    
  chave = (char *) malloc (n * sizeof(char));
    
  printf("digite a chave: ");
  scanf("%s", chave);
    
  confirmacaochave = (char *) malloc (n * sizeof(char));
    
  printf("confirme a chave: ");
  scanf("%s", confirmacaochave);

  
  for (i=0; i<n; i++) {
    if (chave[i] == confirmacaochave[i]) {
      printf("");
    } else {
      do {
        chave = (char *) malloc (n * sizeof(char));
    
    printf("digite a chave: ");
    scanf("%s", chave);
    
    confirmacaochave = (char *) malloc (n * sizeof(char));
    
    printf("confirme a chave: ");
    scanf("%s", confirmacaochave);
      } while (chave[i] != confirmacaochave[i]);
    }
  }

  printf("ok, chave verificada! \n");


  do {
  printf("\n \nescolha uma das opções abaixo: \n1 - Codificar \n2 - Decodificar \n3 - Sair \n");
  scanf("%d", &escolha);

//CODIFICANDO  
  if (escolha == 1) {
    printf("codificando... \nDigite a mensagem: ");
    scanf("%s", mensagem);
    tamanho = strlen(mensagem);
    printf("tamanho da mensagem: %d  \n", tamanho);
    
    for (i=0; i<tamanho; i++) {
      codigo[i] = mensagem[i]^chave[i%n];
    }

    printf("sua mensagem codificada é: ");
    for (i=0; i<tamanho; i++) {
      printf("%d  ", codigo[i]);
    }
  } else if (escolha == 2) {

//DECODIFICANDO
      printf("decodificando... \nDigite o numero de caracteres: ");
      scanf("%d", &numero);

      printf("Digite o codigo a ser decodificado: ");
      for (i=0; i<numero; i++) {
        scanf("%i", &decodigo[i]);
      }
  
      for (i=0; i<numero; i++) {
        mensagem2[i] = decodigo[i]^chave[i%n];
      }

      printf("sua mensagem decodificada é: ");
      for (i=0; i<numero; i++) {
        printf("%c", mensagem2[i]);
      }
    }
  } while (escolha != 3);
  
  return 0;
}
