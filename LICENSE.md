      playGame(secretNumber, attempts);
    }

    public static void playGame(int secretNumber, int attempts) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Введите число: ");
        int guess = scanner.nextInt();
        attempts++;
