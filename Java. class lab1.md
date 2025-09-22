
```java
public class Lab1 {

	private void showArray(int[] arr) {
		System.out.print("Массив: ");
		for (int j : arr) {
			System.out.print(j + " ");
		}
	}

	private long abs(long value) {
		if (value < 0) {
			value = -value;
		}
		return value;
	}

	//1 Задание. Методы
	//1
	public double fraction(double x) {
		return x - (int) x;
	}

	//3
	public int charToNum(char x) {
		return (int) x - (int) '0';
	}

	//5
	public boolean is2Digits(int x) {
		int absValue = abs(x);
		return absValue / 10 != 0 && absValue / 100 == 0;
	}

	//7
	public boolean isInRange(int a, int b, int num) {
		return (num >= a && num <= b) || (num >= b && num <= a);
	}

	//9
	public boolean isEqual(int a, int b, int c) {
		return a == b && b == c;
	}


	//2 Задание. Условия
	//1
	public int abs(int x) {
		if (x < 0) {
			x = -x;
		}
		return x;
	}

	//3
	public boolean is35(int x) {
		int absValue = abs(x);
		return (absValue % 3 == 0 || absValue % 5 == 0) && absValue % 15 != 0;
	}

	//5
	public int max3(int x, int y, int z) {
		int maximus = x;
		if (y > maximus) {
			maxim = y;
		}
		if (z > maximus) {
			maximus = z;
		}
		return maximus;
	}

	//7
	public int sum2(int x, int y) {
		int sum = x + y;
		if (sum >= 10 && sum <= 19) {
			sum = 20;
		}
		return sum;
	}

	//9
	public String day(int x) {
		String result;
		switch (x) {
			case 1:
				result = "Понедельник";
				break;
			case 2:
				result = "Вторник";
				break;
			case 3:
				result = "Среда";
				break;
			case 4:
				result = "Четверг";
				break;
			case 5:
				result = "Пятница";
				break;
			case 6:
				result = "Суббота";
				break;
			case 7:
				result = "Воскресенье";
				break;
			default:
				result = "Это не день недели";
		}
		return result;
	}


	//3 Задание. Циклы
	//1
	public String listNums(int x) {
		String result = "";
		for (int i = 0; i <= x; i++) {
			result += i + " ";
		}
		return result;
	}

	//3
	public String chet(int x) {
		String result = "";
		for (int i = 0; i <= x; i = i + 2) {
			result += i + " ";
		}
		return result;
	}

	//5
	public int numLen(long x) {
		long temp = abs(x);
		int i = 1;
		while (temp / 10 != 0) {
			temp = temp / 10;
			i++;
		}
		return i;
	}

	//7
	public void square(int x) {
		String line = "";
		for (int i = 0; i < x; i++) {
			line += "*";
		}

		for (int i = 0; i < x; i++) {
			System.out.println(line);
		}
	}

	//9
	public void rightTriangle(int x) {
		String line;
		for (int i = 1; i <= x; i++) {
			line = "";
			for (int j = x - i; j > 0; j--) {
				line += " ";
			}

			for (int j = i; j > 0; j--) {
				line += "*";
			}
			System.out.println(line);
		}
	}


	//4 Задание. Массивы
	//1
	public int findFirst(int[] arr, int x) {
		int i = 0;
		int iArr = -1;
		while (iArr == -1 && i < arr.length) {
			if (arr[i] == x) {
				iArr = i;
			}
			i++;
		}
		return iArr;
	}

	//3
	public int maxAbs(int[] arr) {
		int max = arr[0];
		for (int i = 1; i < arr.length; i++) {
			if (abs(arr[i]) > abs(max)) {
				max = arr[i];
			}
		}
		return max;
	}

	//5
	public int[] add(int[] arr, int[] ins, int pos) {
		int[] newArr = new int[arr.length + ins.length];
		for (int iArr = 0, iIns = 0, iNewArr = 0; iNewArr < newArr.length; iNewArr++) {
			if (iArr < pos) {
				newArr[iNewArr] = arr[iArr];
				iArr++;
			} else if (iIns < ins.length) {
				newArr[iNewArr] = ins[iIns];
				iIns++;
			} else {
				newArr[iNewArr] = arr[iArr];
				iArr++;
			}
		}
		showArray(arr);
		showArray(ins);
		return newArr;
	}

	//7
	public int[] reverseBack(int[] arr) {
		int[] newArr = new int[arr.length];
		for (int i = 0; i < arr.length; i++) {
			newArr[i] = arr[arr.length - i - 1];
		}
		return newArr;
	}

	//9
	public int[] findAll(int[] arr, int x) {
		int lenNewArr = 0;
		for (int iArr = 0; iArr < arr.length; iArr++) {
			if (arr[iArr] == x) {
				lenNewArr++;
			}
		}

		int[] newArr = new int[lenNewArr];
		for (int iArr = 0, iNewArr = 0; iArr < arr.length; iArr++) {
			if (arr[iArr] == x) {
				newArr[iNewArr] = iArr;
				iNewArr++;
			}
		}
		return newArr;
	}

}

