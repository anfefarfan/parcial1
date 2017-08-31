#include <iostream>
#include <stdio.h>

int main() {
	
	int vector[100][100];
	int *pfibo;
	int filas, columnas;
	
	printf("Ingrese la cantidad de filas");
	scanf("%d", &filas);
	printf("Ingrese la cantidad de Columnas");
	scanf("%d", &columnas);
	
	pfibo=&vector[filas][columnas];
	
	int ant=0;
	int des=1;
	int fin =0;
	
	for (int i=0;i<filas;i++){
		for(int j=0;j<columnas;j++){
			
			fin = ant + des ;
			ant=des;
			des=fin;
			pfibo=&fin;
			
			printf("%d",*(pfibo+i));	
			
		}
		printf("\n");
		
	}	
	return 0;
}
