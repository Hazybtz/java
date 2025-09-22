```java
public class UserInterface {

	CheckInput input = new CheckInput();
	Lab1 lab = new Lab1();

	private void showArray(int[] arr) {
		System.out.print("Результат: ");
		for (int j : arr) {
			System.out.print(j + " ");
		}
	}

	// Задание 1. Методы
	// Задача 1
	private void t1E1() {
		System.out.println("Задача 1:");
		double value = input.inputDouble("Введите дробное число: ");
		double result = 0;
		result = lab.fraction(value);
		System.out.println("Результат: " + result);
	}
	
	// Задача 3
	private void t1E3() {
		System.out.println("Задача 3:");
		char value = input.inputCharDigit();
		int result = 0;
		result = lab.charToNum(value);
		System.out.println("Результат: " + result);
	}
	
	// Задача 5
	private void t1E5() {
		System.out.println("Задача 5:");
		int value = input.inputInt();
		boolean result = false;
		result = lab.is2Digits(value);
		System.out.println("Результат: " + result);
	}
	
	// Задача 7
	private void t1E7() {
		System.out.println("Задача 7:");
		int  a = input.inputInt();
		int b = input.inputInt();
		int num = input.inputInt();
		boolean result = false;
		result = lab.isInRange(a, b, num);
		System.out.println("Результат: " + result);
	}

    // Задача 9
    private void t1E9() {
		System.out.println("Задача 9:");
		int a = input.inputInt();
		int b = input.inputInt();
		int c = input.inputInt();
		boolean result = false;
		result = lab.isEqual(a, b, c);
		System.out.println("Результат: " + result);
	}
	
	// Задание 2. Условия
	//Задача 1
	private void t2E1() {
		System.out.println("Задача 1:");
		int value = input.inputInt();
		int result = 0;
		result = lab.abs(value);
		System.out.println("Результат: " + result);
	}
	
	// Задача 3
	private void t2E3() {
		System.out.println("Задача 3:");
		int value = input.inputInt();
		boolean result = false;
		result = lab.is35(value);
		System.out.println("Результат: " + result);
	}
	
	// Задача 5
	private void t2E5() {
		System.out.println("Задача 5:");
		int x = input.inputInt();
		int y = input.inputInt();
		int z = input.inputInt();
		int result = 0;
		result = lab.max3(x, y, z);
		System.out.println("Результат: " + result);
	}
	
	// Задача 7
	private void t2E7() {
		System.out.println("Задача 7:");
		int x = input.inputInt();
		int y = input.inputInt();
		int result = 0;
		result = lab.sum2(x, y);
		System.out.println("Результат: " + result);
	}
	
	//Задача 9
	private void t5C2() {
		System.out.println("Задача 9:");
		int value = input.inputInt();
		String result = "";
		result = lab.day(value);
		System.out.println("Результат: " + result);
	}
	
	// Задание 3. Циклы
    // Задача 1
	private void t3E1() {
		System.out.println("Задача 1:");
		int value = input.inputIntRangeMin("Введите целое число больше или равное нулю: ", -1);
		String result = "";
		result = lab.listNums(value);
		System.out.println("Результат: " + result);
	}
	
	// Задача 3
	private void t3E3() {
		System.out.println("Задача 3:");
		int value = input.inputIntRangeMin("Введите целое число больше или равное нулю: ", -1);
		String result = "";
		result = lab.chet(value);
		System.out.println("Результат: " + result);
	}
	
	// Задача 5
	private void t3E5() {
		System.out.println("Задача 5:");
		long value = input.inputInt();
		int result = 0;
		result = lab.numLen(value);
		System.out.println("Результат: " + result);
	}
	
	// Задача 7
	private void t3E7() {
		System.out.println("Задача 7:");
		int value = input.inputIntRangeMin("Введите целое число больше нуля:", 0);
		lab.square(value);
	}
	
	//Задача 9
	private void t3E9() {
		System.out.println("Задача 9:");
		int value = input.inputIntRangeMin("Введите целое число больше нуля:", 0);
		lab.rightTriangle(value);
    }
    
    // Задание 4. Массивы
    // Задача 1
	private void t4E1() {
		System.out.println("Задача 1:");
		int[] arr = input.createArrInt();
		int value = input.inputInt();
		int result = lab.findFirst(arr, value);
		System.out.println("Результат: " + result);
	}

	// Задача 3
	private void t4E3() {
		System.out.println("Задача 3:");
		int[] arr = input.createArrInt();
		int result = lab.maxAbs(arr);
		System.out.println("Результат: " + result);
	}

	// Задача 5
	private void t4E5() {
		System.out.println("Задача 5:");
		int[] result;
		int[] arr = input.createArrInt("Создание массива 1");
		int[] ins = input.createArrInt(
				"Создание массива 2");
		int pos = input.inputIntRange("Введите позицию элемента от 0 до " + (arr.length) + ": ", -1,
				arr.length + 1);
		result = lab.add(arr, ins, pos);
		System.out.println("Позиция " + pos);
		showArray(result);
	}

	// Задача 7
	private void t4E7() {
		System.out.println("Задача 7:");
		int[] arr = input.createArrInt();
		int[] result = lab.reverseBack(arr);
		showArray(result);
	}
	
	// Задача 9
	private void t4E9() {
		System.out.println("Задача 9:");
		int[] arr = input.createArrInt();
		int value = input.inputInt();
		int[] result = lab.findAll(arr, value);
		showArray(result);
	}

	public void choiceTask() {
		int task;
		int exercise;
		System.out.println("Выберите задание: ");
		System.out.println("1 - Методы\n2 - Условия\n3 - Циклы\n4 - Массивы");
		task = input.inputIntRange("Выбор: ", 0, 5);
		exercise = input.inputIntRange("Введите номер задачи от 1 до 5: ", 0, 6);

		switch (task) {
			case 1:
	            System.out.println("==Методы==");
				switch (exercise) {
					case 1:
						t1E1();
						break;
					case 2:
						t1E3();
						break;
					case 3:
						t1E5();
						break;
					case 4:
						t1E7();
						break;
					case 5:
						t1E9();
						break;
				}
				break;
			case 2:
			    System.out.println("==Условия==");
				switch (exercise) {
					case 1:
						t2E1();
						break;
					case 2:
						t2E3();
						break;
					case 3:
						t2E5();
						break;
					case 4:
						t2E7();
						break;
					case 5:
					    t2E9();
					    break;
				}
				break;
			case 3:
			    System.out.println("==Циклы==");
				switch (exercise) {
					case 1:
						t3E1();
						break;
					case 2:
						t3E3();
						break;
					case 3:
						t3E5();
						break;
					case 4:
						t3E7();
						break;
					case 5:
					    t3E9();
					    break;
				}
				break;
			case 4:
			    System.out.println("==Массивы==");
				switch (exercise) {
					case 1:
						t4E1();
						break;
					case 2:
						t4E3();
						break;
					case 3:
						t4E5();
						break;
					case 4:
						t4E7();
						break;
					case 5:
					    t4E9();
					    break;
				}
				break;
		}
	}
}