Exercicio 4 
Não está rodando acredito que seja por conta da atualização, mas fiz de outra forma tbm #include <stdio.h>
#include <locale.h>

int absoluto(int n) {
    return (n < 0) ? -n : n;
}

int main() {
    setlocale(LC_ALL, "Portuguese");
    int num;
    
    int i;
    for (i = 0; i < 5; i++) {
        printf("Digite um número inteiro: ");
        if (scanf("%d", &num) != 1) {
            printf("Entrada inválida! Por favor, digite um número inteiro.\n");
            while (getchar() != '\n');
            i--; 
            continue;
        }
        printf("O valor absoluto de %d é %d\n", num, absoluto(num));
    }
    return 0;
}
