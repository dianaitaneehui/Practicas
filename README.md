void swap (int *a, int *b);
int longitudCadena ( char * cadena);
void invertirArreglo (int *arr , int size);
int cuentaPares (int *arr , int size);

void main(){
int a = 4, b = 25;
printf("Antes del swap: a = %d, b = %d\n", a,b);
swap(&a,&b);
printf("Despues del swap: a = %d, b = %d\n", a,b);

//fucion longitud
char cadena[] = "peperoni";
int lon = longitudCadena(cadena);
printf("Longitud de la cadena '%s': %d\n", cadena,lon);

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
