# NIF-o-letra-asociada-a-un-dni
#programa de nif de un dni en java


package Mendoza_Ramirez_Edson;

import java.util.Scanner;

public class Dos_en_Consola {
    public static void main(String[] args) {
       Scanner entrada=new Scanner(System.in);
       int dni,resto;
       String op="si";
       while(op.equalsIgnoreCase("si")){
       do{
            System.out.print("Ingrese dni: ");
             dni=entrada.nextInt();
            if (String.valueOf(dni).length() == 8) {
                String arreglo[] = {"T","R","W","A","G","M","Y","F","P","D","X","B","N","J","Z","S","Q","V","H","L","C","K","E"};
                resto = dni % 23;
                System.out.println("su NIF es: '"+arreglo[resto]+"'");
            } else {
                System.out.println("El dni debe contener 8 digitos");
            }
    }while(String.valueOf(dni).length() != 8);
           System.out.print("Desea continuar(si) o Salir(cualquier letra): ");
           op=entrada.next();
    }
    } 
}
