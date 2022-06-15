# Interfaces
Practica OpenBootcamp

package Interface;

public class Main {
    public static void main(String[] args) {

        EmpleadoCRUD empleadoCRUD= new EmpleadoCRUD();

        Empleado juanito= new Empleado("juanito", 30, 40000, true);
        Empleado patricia= new Empleado("Patricia", 30, 40000, true);
        Empleado roberto=new Empleado("Roberto", 30, 30000, true);
        System.out.println(juanito);

//guardar empleados
        empleadoCRUD.guardar(juanito);
        empleadoCRUD.guardar(patricia);
        empleadoCRUD.guardar(roberto);


    }
}

Package Interface;

public class Empleado {

    // 1 Atributos
    String nombre;
    int edad;
    double salario;
    boolean alta;

    // 2 constructores

    public Empleado(){}

    public Empleado(String nombre, int edad, double salario, boolean alta) {
        this.nombre = nombre;
        this.edad = edad;
        this.salario = salario;
        this.alta = alta;
    }

    @Override
    public String toString() {
        return "Empleado{" +
                "nombre='" + nombre + '\'' +
                ", edad=" + edad +
                ", salario=" + salario +
                ", alta=" + alta +
                '}';
    }
}


package Interface;

import java.util.ArrayList;
import java.util.List;

public class EmpleadoCRUD {

    // Estructura de datos
    List<Empleado> empleados= new ArrayList<>();


    public void guardar(Empleado empleado){
//crear empleado
        empleados.add(empleado);


        }



}
