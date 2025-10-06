void swap (int *a, int *b);
int longitudCadena ( char * cadena);
void invertirArreglo (int *arr , int size);
int cuentaPares (int *arr , int size);

void main(){
int a = 4, b = 25;
printf("Antes del swap: a = %d, b = %d\n", a,b);
scanf(&a,&b);
printf("Despues del swap: a = %d, b = %d\n", a,b);
}

void swap (int *a, int *b){
  int temp = *a;
  *a = *b;
  *b = temp;
}

