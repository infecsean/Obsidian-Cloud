Assignment 1 trashed
- int numberOfCoins = -1;

while(numberOfCoins <= 0) {

Scanner input = new Scanner(System.in);

System.out.println("Please input the number of coins: ");

String inputString = input.nextLine();

try {

numberOfCoins = Integer.parseInt(inputString);

}catch(Exception Error) {

input = new Scanner(System.in);

System.out.println("Error: Input is not a NUMBER");

}

}

System.out.println("You entered: " + numberOfCoins);

