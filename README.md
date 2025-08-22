#include <stdio.h>
#include <math.h>
#define PI 3.1416

double calcularAreaRectangulo (double longitud, double altura){
	double area= longitud*altura;
	return area;
}

double calcularPerimetroRectangulo (double longitud, double altura){
	double perimetro= 2*(longitud+altura);
	return perimetro;
}
double calcularDiagonalRectangulo (double longitud, double altura){
	double diagonal= sqrt(longitud*longitud+altura*altura);
	return diagonal;
}

double	calcularAreaCirculo (double radio){
	double area= PI* (radio*radio);
	return area;
}

double	calcularPerimetroCirculo (double radio){
	double perimetro= 2*PI*radio;
	return perimetro;
}
	
void imprimirResultados (int area, int perimetro){
	printf("\nEl area es: %d", area);
	printf("\nEl perimetro es: %d", perimetro);
	
}
int main(void) {
	
	int figura;
	double area;
	double perimetro;
	
	do{printf("\nSelecciona que figura deseas calcular (1=rectangulo; 2=circulo):");
	scanf("%d", &figura);}
	while (figura!=1 && figura!=2);
	
	if(figura==1){
		printf("\nHa seleccionado rectangulo");
		double longitud;
		double altura;
		
		printf("\nIngrese la longitud:");
		scanf("%lf", &longitud);
		printf("Ingrese la altura:");
		scanf("%lf", &altura);
		
		area=calcularAreaRectangulo (longitud, altura);
		perimetro=calcularPerimetroRectangulo (longitud, altura);}
		
		else {
		printf("\nHa seleccionado circulo");
		double radio;
		printf("\nIngrese el radio:");
		scanf("%lf", &radio);
		
		area=calcularAreaCirculo (radio);
		perimetro=calcularPerimetroCirculo (radio);
		}
	
		imprimirResultados (area, perimetro);
	
	
		
	
	
	
	
	
	return 0;
}
