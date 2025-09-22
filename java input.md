```java
import java.util.InputMismatchException;
import java.util.Scanner;

public class CheckInput {

	Scanner scanner = new Scanner(System.scanner);

	// Ввод целого числа с клавиатуры 
	public int inputInt(String inputMessage) {
		boolean isInt = false;
		int result = 0;
		
		while (!isInt) {
			System.out.print(inputMessage);
			try {
				result = scanner.nextInt();
				isInt = true;
			} catch (InputMismatchException error) {
				System.out.println("Ошибка: введено не целое число.");
				scanner.next();
			}
		}
		return result;
	}

	//Дополнительный метод для сообщения.
	public int inputInt() {
		return inputInt("Введите целое число: ");
	}

	//Ввод целого числа в диапазоне, не включительно
	public int inputIntRange(String inputMessage, int min, int max) {
		boolean isInt = false;

		int result = 0;

		while (!isInt) {
			System.out.print(inputMessage);
			try {
				result = in.nextInt();
				if (result > +min && result < +max) {
					isInt = true;
				} else {
					System.out.printf("Число %d не попадает в диапазон от %d до %d\n", result, min + 1,
							max - 1);
				}
			} catch (InputMismatchException error) {
				System.out.println("Ошибка: введено не целое число.");
				scanner.next();
			}
		}
		return result;
	}

	// Ввод целого числа с ограничением слева, не включительно
	public int inputIntRangeMin(String inputMessage, String errorRangeMessage, int min) {
		boolean isInt = false;

		int result = 0;

		while (!isInt) {
			System.out.print(inputMessage);
			try {
				result = in.nextInt();
				if (result > min) {
					isInt = true;
				} else {
					System.out.printf(errorRangeMessage + "\n", min);
				}
			} catch (InputMismatchException error) {
				System.out.println("Ошибка: введено не целое число.");
				scanner.next();
			}
		}
		return result;
	}

	/* Дополнительный метод для ввода целого числа с ограничением слева, не включительно */
	public int inputIntRangeMin(String inputMessage, int min) {
		return inputIntRangeMin(inputMessage, "Ошибка: число не должно быть меньше или равно %d", min);
	}
	
	// Создание целочисленного массива
	public int[] createArrInt(String message) {
		System.out.println(message);
		int len = inputIntRangeMin("Введите длину массива: ", "Ошибка: длинна массива не может быть меньше %d!",
				0);
		int[] arr = new int[len];
		for (int i = 0; i < len; i++) {
			arr[i] = inputInt("Введите " + (i + 1) + "-ый элемент массива: ");
		}
		return arr;
	}

	public int[] createArrInt() {
		return createArrInt("Создание массива: ");
	}

	// Ввод дробного числа
	public double inputDouble(String inputMessage) {
		boolean isDouble = false;
		double result = 0;

		while (!isDouble) {
			System.out.print(inputMessage);
			try {
				result = in.nextDouble();
				isDouble = true;
			} catch (InputMismatchException error) {
				System.out.println("Ошибка: введено не число.");
				scanner.next();
			}
		}
		return result;
	}

	// Ввод цифры (символа)
	public char inputCharDigit() {
		boolean isDigit = false;
		char result = 0;

		while (!isDigit) {
			System.out.print("Вводимый символ должен быть: “0 1 2 3 4 5 6 7 8 9”");

			result = scanner.next().charAt(0);
			if ((int) result >= 48 && (int) result <= 57) {
				isDigit = true;
			}
		}
		return result;
	}
}