import java.util.Scanner;

public class NumberGuessingGame {

    public static void main(String[] args) {
        // Generate a random number from 1 to 100
        int randomNumber = (int)(Math.random() * 100) + 1;

        // Create a Scanner object to read user input
        Scanner scanner = new Scanner(System.in);

        // Initialize the number of attempts
        int attempts = 0;

        // Initialize the number of rounds
        int rounds = 5;

        // Start the game loop
        while (rounds > 0) {
            // Prompt the user to enter their guess
            System.out.print("Enter your guess: ");
            int guess = scanner.nextInt();

            // Check if the guess is correct
            if (guess == randomNumber) {
                // The user guessed correctly, so break out of the loop
                System.out.println("Congratulations, you guessed the number correctly!");
                rounds--;
            } else {
                // The guess is incorrect, so increment the number of attempts
                attempts++;

                // Tell the user if their guess is higher or lower than the random number
                if (guess < randomNumber) {
                    System.out.println("Too Low");
                } else {
                    System.out.println("Too High");
                }
            }
        }

        // Calculate the score
        int score = rounds * attempts;

        // Display the score
        System.out.println("You guessed the number in " + attempts + " attempts.");
        System.out.println("Your score is " + score + ".");
    }
}# NumberGuessingGame.java
