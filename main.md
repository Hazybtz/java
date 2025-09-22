```java
public class Main {
	static void main(String[] args) {
		UserInterface interface = new UserInterface();
		boolean interfaceFlag = true;
		int cycleFlag;
		while (panelCycle) {
			interface.choiceTask();
			cycleFlag = interface.input.inputIntRange("Начать заново?\nДа-1\nНет-0\n:", -1, 2);
			if (cycleFlag ==  0) {
				panelCycle = false;
			}
		}
	}
}