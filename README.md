//https://github.com/lucaswustten/bmi.c.git

#include <stdio.h>
#define TAM 5

int main(void) {
	
	int codigos[TAM];
	float precios[TAM];
	float mayor_precio=0;
	int codigo_mayor;
	float menor_precio=999999999;
	int codigo_menor;
	
	for(int i=0; i<TAM; i++){
		do{
		printf("\nIngrese el codigo de barras (1-999999999): ");
		scanf("%d", &codigos[i]);
		if(codigos[i]<1 || codigos[i]>999999999)
			printf("\nError. El codigo de barras debe estar entre 1-999999999");
		
		}while(codigos[i]<1 || codigos[i]>999999999);
		
		do{
		printf("\nIngrese el precio del producto: ");
		scanf("%f", &precios[i]);
		if(precios[i]<0)
			printf("\nEl precio debe ser positivo.");
		}while(precios[i]<0);
		
	}
	
	printf("\ncodigos		Precios");
	for(int i=0; i<TAM; i++){
		printf("\n%d		%.2f", codigos[i], precios[i]);
		if(precios[i]>mayor_precio)
		{mayor_precio=precios[i];
		codigo_mayor=codigos[i];
		}
		if(precios[i]<menor_precio)
		{menor_precio=precios[i];
		codigo_menor=codigos[i];
		}
	}
	
	printf("\nMas caro: %.2f [%d]", mayor_precio, codigo_mayor);
	printf("\nMas barato: %.2f [%d]", menor_precio, codigo_menor);
	
	return 0;
}

