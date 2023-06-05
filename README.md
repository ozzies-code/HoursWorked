# HoursWorked
Program in C that calculates Hours Worked. 
#include <stdio.h>
#include <stdlib.h>

int main(int argc, char *argv[])
{
  float horas, precioHora, salario;
   char nombre[81];
   char masDatos;

    puts("\tCalcula Salario");
    puts("Introducir Horas, precio hora y nombre. \n");

    do{
        printf("Nombre: ");
        gets(nombre);
        printf("Horas Trabajadas: ");
        scanf("%f", &horas);
        printf("Precio Hora: ");
        scanf("%f%*c", &precioHora);

        if (horas <= 40.0)
        salario = horas * precioHora;
        else
        salario = 40 * precioHora + 
                  1.5 * (horas - 40.0) * precioHora;
        
        printf("Salario de %s %.1f\n", nombre, salario);
        printf("\nMas Trabajadores  (S/N): ");
        scanf("%c%*c", &masDatos);
    }while (masDatos == 'S' || masDatos == 's');
  system("PAUSE");	
  return 0;
}


