import java.util.Scanner;

public class Temperature {

//set variable field
private double ftemp;

//set constructor
public Temperature(double farGiven)
{
ftemp = farGiven;
}

//set mutator
public void setFahrenheit(double farGiven)
{
ftemp = farGiven;
}

//set accessor
public double getFahrenheit()
{
return ftemp;
}

public double getCelsius()
{
return ((double) 5/9) * (ftemp - 32);
}

public double getKelvin()
{
return ((5/(double)9) * (ftemp - 32)) + 273;
}

//get user entry
public static void main(String[] args)
{
//create new scanner object
Scanner scanner = new Scanner(System.in);

//set input variable
double farInput;

//get user input
System.out.print("Enter a Fahrenheit temperature:");
farInput = scanner.nextDouble();

Temperature temp1 = new Temperature(farInput);

//show Fahrenheit, Celius and Kelvin temperatures
System.out.println("The temperature in Fahrenheit is " + temp1.getFahrenheit());
System.out.println("The temperature in Celsius is " + temp1.getCelsius());
System.out.println("The temperature in Kelvin is " + temp1.getKelvin());
}

}
