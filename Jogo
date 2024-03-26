#include <stdio.h>
#include <stdlib.h>
#include <locale.h>
#include <time.h>

int main() {
    
    setlocale(LC_ALL, "Portuguese");
    
    printf("\n\n");
    printf("          P  /_\\  P                              \n");
    printf("         /_\\_|_|_/_\\                            \n");
    printf("     n_n | ||. .|| | n_n         Bem vindo ao     \n");
    printf("     |_|_|nnnn nnnn|_|_|     Jogo de Adivinhação! \n");
    printf("    |\" \"  |  |_|  |\"  \" |                     \n");
    printf("    |_____| ' _ ' |_____|                         \n");
    printf("          \\__|_|__/                              \n");
    printf("\n\n");
    

    srand(time(0));
    int numeroSecreto = rand() % 100;
    int chute;
    double pontos = 1000;
    
    int acertou;

    int nivel;
    printf("Qual o nível de dificuldade que gostaria de jogar:\n");
    printf("(1) Fácil (2) Médio (3) Difícil\n\n");
    printf("Escolha: ");
    
    scanf("%d", &nivel);

    int numeroDeTentativas;
    
    switch(nivel) {
        case 1:
        numeroDeTentativas = 20;
        break;
        
        case 2:
        numeroDeTentativas = 15;
        break;
        
        default:
        numeroDeTentativas = 6;
        break;
    }
    
    for (int i = 1; i <= numeroDeTentativas; i++) {
        
        printf("\nTentativa %d de %d", i, numeroDeTentativas);
        printf("\nQual é o seu chute? ");
        
        scanf("%d", &chute);
        printf("\nSeu chute foi %d\n", chute);
        
        if(chute < 0) {
            printf("A resposta não é um número negativo!\n");
            
            i--;
            continue;
        }
                
        acertou = chute == numeroSecreto;
        
        if (acertou) {
            break;
        }
        
        else if (chute > numeroSecreto) {
            printf("\nSeu chute foi maior que o número secreto!\n");
            }
            
        else {
                printf("\nSeu chute foi menor que o número secreto!\n");
            
            }
            
            double pontosPerdidos = abs(chute - numeroSecreto) / (double) 2;
            pontos = pontos - pontosPerdidos;
    }
    if (acertou) {
        printf("Parabéns! Você acertou!\n");
        printf("Total de pontos: %.1f\n", pontos);
    }
    
    else {

        printf("       \\|/ ____ \\|/    \n");   
        printf("        @~/ ,. \\~@      \n");   
        printf("       /_( \\__/ )_\\    \n");   
        printf("          \\__U_/        \n");

        printf("\nVocê perdeu! O número secreto era %d!\n\n", numeroSecreto);
    }
}