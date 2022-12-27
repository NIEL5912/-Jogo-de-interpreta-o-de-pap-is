#jogo-de-interpretar-papeis
Código criado por mim.

#include <stdio.h>
#include <stdlib.h>

int nivel_minimo ( int vit0, int inc, int vitd);

int main (void){
int c;
int i=0;
int vitdese;
printf ("Entre com a classe (1-arqueiro, 2-barbaro, 3-druida, 4-mago):\n");
scanf ("%d", &c);
if ( c>4) { printf ("Classe Invalida.\n"); return 0;}
printf ("Entre com a vitalidade desejada:\n");
scanf ("%d", &vitdese);

switch (c){
    case 1:  i= nivel_minimo(150, 10, vitdese);
     break;
    case 2:  i= nivel_minimo(180, 15, vitdese);
     break;
     case 3: i= nivel_minimo(100, 5, vitdese);
     break;
     case 4: i= nivel_minimo(100, 5, vitdese);
     break; }

    printf ("Nivel necessario: %d\n", i);

    return 0;}

int nivel_minimo ( int vit0, int inc, int vitd){int i=0;
 while ( vit0<vitd) { 
        vit0= vit0+inc; i++;
     if (i%inc==0) { vit0=vit0+inc;}};
     return i; }

