#include <stdio.h>
void swap (int *a, int *b);
int longitudCadena ( char * cadena);
void invertirArreglo (int *arr , int size);
int cuentaPares (int *arr , int size);

void main(){
//fincion swap
int a = 4, b = 25;
printf("Antes del swap: a = %d, b = %d\n", a,b);
swap(&a,&b);
printf("Despues del swap: a = %d, b = %d\n", a,b);

//fucion longitud
char cadena[] = "peperoni";
int lon = longitudCadena(cadena);
printf("Longitud de la cadena '%s': %d\n", cadena,lon);

//funcion invertir
 int num[] = {25, 20, 15, 10, 5};
    int size = sizeof(num) / sizeof(num[0]);
    printf("Original: ");
    for (int i = 0; i < size; i++) {
    printf("%d ", num[i]);
    }
    invertirArreglo(num, size);
    printf("\nInvertido: ");
    for (int i = 0; i < size; i++) {
        printf("%d ", num[i]);
    }   
 return 0;

//funcion pares
int num[]={1,2,3,4,5,8};
int numSize= sizeof(num) / sizeof(num[0]);
int pares = cuentaPares(num,numSize);
printf("La cantidad de numeros pares son: %d\n", pares);

}




void swap (int *a, int *b){
  int temp = *a;
  *a = *b;
  *b = temp;
}

int longitudCadena ( char * cadena){
 int lon = 0;
 while(*cadena != '\0'){
   lon++;
   cadena++;
}
return lon;
}

void invertirArreglo(int *arr, int size) {
    int *inicio = arr;
    int *fin = arr + size - 1;
    int temp;
    
    while (inicio < fin) {
        temp = *inicio;
        *inicio = *fin;
        *fin = temp;
        
        inicio++;
        fin--;
        }
    }

 int cuentaPares (int *arr , int size){
  int contador = 0; 
  int i;
  for(i=0; i<size;i++){
    if( *(arr+i)%2==0){
      contador ++;
    }
    }
     return contador;
}
    
