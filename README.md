# Task-1-Temperature-Converter
Create a program that converts temperatures between Celsius and Fahrenheit. Prompt the user to enter a temperature value and the unit of measurement, and then perform the conversion. Display the converted temperature.  Skills: Basic input/output operations, arithmetic operations.
import java.util.Scanner;

public class TemperatureConverter {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Temperature Converter");
        System.out.print("Enter the temperature value: ");
        double temperature = scanner.nextDouble();

        System.out.print("Enter the unit (C for Celsius or F for Fahrenheit): ");
        char unit = scanner.next().charAt(0);

        if (unit == 'C' || unit == 'c') {
            double fahrenheit = (temperature * 9 / 5) + 32;
            System.out.println("Converted temperature: " + fahrenheit + " Fahrenheit");
        } else if (unit == 'F' || unit == 'f') {
            double celsius = (temperature - 32) * 5 / 9;
            System.out.println("Converted temperature: " + celsius + " Celsius");
        } else {
            System.out.println("Invalid unit. Please enter C or F.");
        }

        scanner.close();
    }
}
