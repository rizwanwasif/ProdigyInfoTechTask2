# ProdigyInfoTechTask2
import java.util.Scanner;
import java.util.Random;

public class GuessingGame {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Random random = new Random();
        int numberToGuess = random.nextInt(100) + 1;
        int numberOfAttempts = 0;
        int guess = 0;

        System.out.println("Welcome to the Guessing Game!");
        System.out.println("I'm thinking of a number between 1 and 100.");

        while (guess != numberToGuess) {
            System.out.print("Take a guess: ");
            guess = scanner.nextInt();
            numberOfAttempts++;

            if (guess < numberToGuess) {
                System.out.println("Too low! Try again.");
            } else if (guess > numberToGuess) {
                System.out.println("Too high! Try again.");
            } else {
                System.out.println("Congratulations! You've guessed the number in " + numberOfAttempts + " attempts.");
            }
        }

        scanner.close();
    }
}
