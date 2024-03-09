using System;

class Program
{
    static void Main(string[] args)
    {
        double totalConDescuento = 0;
        double totalSinDescuento = 0;

        for (int i = 1; i <= 3; i++)
        {
            Console.WriteLine($"Ingrese el precio del producto {i}:");
            double precio = double.Parse(Console.ReadLine());

            if (precio > 100)
            {
                totalConDescuento += AplicarDescuento(precio);
            }
            else
            {
                totalSinDescuento += precio;
            }
        }

        Console.WriteLine($"Total con descuento: {totalConDescuento}");
        Console.WriteLine($"Total sin descuento: {totalSinDescuento}");
    }

    static double AplicarDescuento(double precio)
    {
        double descuento = precio * 0.15;
        double precioConDescuento = precio - descuento;
        return precioConDescuento;
    }
}
