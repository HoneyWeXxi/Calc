import java.util.Scanner;

class Main {
    public static String calc(String input) {
        String[] parts = input.trim().split(" ");
        if (parts.length != 3) {
            throw new IllegalArgumentException("Invalid input format.");
        }

        int a = Integer.parseInt(parts[0]);
        int b = Integer.parseInt(parts[2]);
        String operation = parts[1];

        if (a < 1 || a > 10 || b < 1 || b > 10) {
            throw new IllegalArgumentException("Numbers must be between 1 and 10.");
        }

        switch (operation) {
            case "+":
                return String.valueOf(a + b);
            case "-":
                return String.valueOf(a - b);
            case "*":
                return String.valueOf(a * b);
            case "/":
                if (b == 0) {
                    throw new IllegalArgumentException("Division by zero is not allowed.");
                }
                return String.valueOf(a / b);
            default:
                throw new IllegalArgumentException("Invalid operation.");
        }
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Введите выражение (например, 3 + 4): ");
        String input = scanner.nextLine();

        try {
            String result = calc(input);
            System.out.println("Результат: " + result);
        } catch (Exception e) {
            System.out.println("Ошибка: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }
}
