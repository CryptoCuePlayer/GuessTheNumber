# GuessTheNumber
GuessTheNumber
import java.util.Scanner;

public class GuessTheNumber {
    public static void main(String[] args) {
        int secretNumber = (int) (Math.random() * 100) + 1;
        int attempts = 0;
        
        System.out.println("Добро пожаловать в игру \"Угадай число\"!");
        System.out.println("Я загадал число от 1 до 100. Попробуйте угадать!");

        playGame(secretNumber, attempts);
    }

    public static void playGame(int secretNumber, int attempts) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Введите число: ");
        int guess = scanner.nextInt();
        attempts++;

        if (guess == secretNumber) {
            System.out.println("Поздравляю! Вы угадали число " + secretNumber + " за " + attempts + " попыток.");
        } else if (guess < secretNumber) {
            System.out.println("Загаданное число больше. Попробуйте ещё раз.");
            playGame(secretNumber, attempts);
        } else {
            System.out.println("Загаданное число меньше. Попробуйте ещё раз.");
            playGame(secretNumber, attempts);
        }
    }
}
