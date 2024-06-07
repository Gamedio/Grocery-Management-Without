import java.util.Scanner;

public class GroceryShop implements GroceryShopOperations{
	String shopName;
	Grocery groceries[];
	Scanner input = new Scanner(System.in);


	int counter;

	

	public GroceryShop() {

		System.out.println("Type in Grocery Shop Name -");
		this.shopName = input.nextLine();
		System.out.println("Grocery Shop Name set to  : " +  this.shopName );
		groceries = new Grocery[100];



	}

	@Override
	public void showName(){
		System.out.println("Grocery Shop   : " +  this.shopName );
	}

	@Override
	public boolean insertGrocery(Grocery b) {
		if (counter < this.groceries.length) {
			this.groceries[counter] = b;
			counter++;
			
			return true;

		} else
			return false;
	}

	

		



	

	@Override
	public  int searchGroceryName( String Name){
		for (int i=0; i<counter ; i++){
			if(groceries[i].getGroceryName().equals(Name)){
				return i;
			}
		}
		return -1;
	}

	@Override
	public  void searchGrocery(String Name){
		int i = searchGroceryName(Name);
		if( i == -1){

			System.out.println("No match found");
		}
		else {
			System.out.println("\n Found The Grocery Item!");
			 groceries[i].showList();


		}
	}

	@Override
	public  void deleteGrocery(String Name){
		int i = searchGroceryName(Name);
		if( i == -1){

			System.out.println("No match found");
		}
		else {
			groceries[i] = groceries[--counter];
			System.out.println("\n Grocery Item Has been deleted!\n");
		}
	}
	

	@Override
	public  void sellGrocery(String Name){
		int i = searchGroceryName(Name);
		if( i == -1){

			System.out.println("No match found");
		}
		else {


			do {
				System.out.println("Type in Grocery quantity To Sell (numbers only) -"  );
				while (!input.hasNextInt()) {
						System.out.println("Sell Quantity can only be positive number! I can't sell a product that doesnt exist or exist in a different dimension because of negative quantity.  Please type in proper positive quantity- ");
						input.next(); 
				}
				int amount = input.nextInt();
				input.nextLine();
				
				groceries[i].sell(amount);
				
		} while (groceries[i].getavailableQuantity() < 0);
		
		



		}
	}



	@Override
	public  void restockGrocery(String Name){
		int i = searchGroceryName(Name);
		if( i == -1){

			System.out.println("No match found");
		}
		else {


			do {
				System.out.println("Type in Grocery quantity To Restock (numbers only) -"  );
				while (!input.hasNextInt()) {
						System.out.println("Restock Quantity can only be positive number! I can't sell a product that doesnt exist or exist in a different dimension because of negative quantity.  Please type in proper positive quantity- ");
						input.next(); 
				}
				int amount = input.nextInt();
				input.nextLine();
				
				groceries[i].restock(amount);
				
		} while (groceries[i].getavailableQuantity() <= 0);
		
		



		}
	}




	

	@Override
	public void showAllGroceries() {
		System.out.println("\n >>>>Groceries List<<<<");
		System.out.println("Shop Name: " + this.shopName);
		for (int i = 0; i < counter; i++) {
			this.groceries[i].showList();
		}
	}

}
