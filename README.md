# coderscave-normal-task
import java.util.Scanner;

public class BMICalculator {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Welcome to the BMI Calculator!");

        // Input height in meters
        System.out.print("Enter your height in meters: ");
        double height = scanner.nextDouble();

        // Input weight in kilograms
        System.out.print("Enter your weight in kilograms: ");
        double weight = scanner.nextDouble();

        // Calculate BMI
        double bmi = calculateBMI(weight, height);

        // Interpret BMI
        String interpretation = interpretBMI(bmi);

        // Display BMI and interpretation
        System.out.println("Your BMI is: " + bmi);
        System.out.println("BMI Category: " + interpretation);

        scanner.close();
    }

    // Function to calculate BMI
    public static double calculateBMI(double weight, double height) {
        return weight / (height * height);
    }

    // Function to interpret BMI
    public static String interpretBMI(double bmi) {
        if (bmi < 18.5) {
            return "Underweight";
        } else if (bmi >= 18.5 && bmi < 25) {
            return "Normal Weight";
        } else if (bmi >= 25 && bmi < 30) {
            return "Overweight";
        } else {
            return "Obese";
        }
    }
}
