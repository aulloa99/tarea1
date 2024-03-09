
using System;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Bienvenido al programa de cálculo de precios");

        double precioTotal = 0;

        for (int i = 1; i <= 3; i++)
        {
            Console.Write($"Ingrese el precio del producto {i} en céntimos: ");
            double precioProducto = Convert.ToDouble(Console.ReadLine());
            precioTotal += precioProducto;
        }

        double descuento = precioTotal > 500 ? precioTotal * 0.1 : 0;
        double precioFinal = precioTotal - descuento;

        Console.WriteLine($"El total de los productos es: {precioTotal} céntimos");

        if (descuento > 0)
        {
            Console.WriteLine($"Se aplicó un descuento del 10%: {descuento} céntimos");
        }

        Console.WriteLine($"El precio final a pagar es: {precioFinal} céntimos");
    }
}
