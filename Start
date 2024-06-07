import java.util.Scanner;

public class Start {
	public static void main(String[] args) {
		
		Scanner input = new Scanner(System.in);
		System.out.println("\n ====== Welcome To the useless Grocery Shop Management Program ====== \n");

		
			GroceryShop G1 = new GroceryShop();
			G1.showAllGroceries();
			





		boolean isProgrameOpen = true;
while (isProgrameOpen) {
  


	

				int option2 ;

				do {
					System.out.println("\n What Do you want to Do? \n 1. Add Grocery Item \n 2. Search Grocery Item (sell/restock/delete) \n 3. populate shop with dummy Groceries \n 4. Close Program");
					while (!input.hasNextInt()) {
							System.out.println("\nInvalid Option. Plz Try again! \n 1. Add Grocery Item \n 2. Search Grocery Item (sell/restock/delete) \n 3. populate shop with dummy Groceries \n 4. Close Program");
							input.next(); 
					}
					option2 = input.nextInt();
					input.nextLine();
			} while (option2 <= 0 && option2>4);

			




				switch (option2) {
					case 1:
					// Add Grocery Item






					boolean inAddingItem = true;
					while (inAddingItem) {
		
						int option3 ;
		
						do {
							System.out.println("\n What Do you want to Do? \n 1. Add Edible Grocery  \n 2. Add NonEdible Grocery \n 3. Go Back");
							while (!input.hasNextInt()) {
									System.out.println("\nInvalid Option. Plz Try again! \n What Do you want to Do? \n 1. Add Edible Grocery  \n 2. Add NonEdible Grocery \n 3. Go Back");
									input.next(); 
							}
							option3 = input.nextInt();
							input.nextLine();
					} while (option3 <= 0 && option3>3);
					
		
		
		
		
						switch (option3) {
							case 1:
							// Add Edible Grocery Item


							Edibles id1 = new Edibles();

					if (G1.insertGrocery(id1)) {
						System.out.println("\nAdding Edible Grocery was Successful \n");
					} else {
						System.out.println("\nSorry Edible Grocery Stock Full. Plz sell the grocery product in a different shop. You can always create a new shop..... \n");
					}
			

							break;
							case 2:
							// Add NonEdible Grocery Item
		
							NonEdibles id2 = new NonEdibles();
			
							if (G1.insertGrocery(id2)) {
								System.out.println("\nAdding NonEdible Grocery was Successful\n");
							} else {
								System.out.println("\nSorry NonEdible Grocery Stock Full. Plz sell the grocery product in a different shop. You can always create a new shop..... \n");
							}
					

							break;
							case 3:
							inAddingItem=false;
							break;
							default: 
							System.out.println("\nSomething Went Wrong!!\n");
		
		

						}
					}

			
						break;
					case 2:
					// Search Grocery Item
					G1.showAllGroceries();


					boolean inManagingAndSearching = true;
					while (inManagingAndSearching == true) {

		
						int option4 ;
		
						do {
							System.out.println("\n What Do you want to Do? \n 1. Show All Grocery \n 2. Search Grocery  \n 3. Delete Grocery \n 4. Sell Grocery \n 5. Restock Grocery \n 6. Go Back");
							while (!input.hasNextInt()) {
									System.out.println("\nInvalid Option. Plz Try again! \n What Do you want to Do? \n 1. Show All Grocery \n 2. Search Grocery  \n 3. Delete Grocery \n 4. Sell Grocery \n 5. Restock Grocery \n 6. Go Back");
									input.next(); 
							}
							option4 = input.nextInt();
							input.nextLine();
							
					} while (option4 <= 0 && option4>6);
					
					
		
						switch (option4) {
							case 1:
							G1.showAllGroceries();

							break;
							case 2:
							// Search Grocery Item
							System.out.println("\nType in Grocery Name for searching - ");
							
							String SearchGroceryText = input.nextLine();
							G1.searchGrocery(SearchGroceryText);


			

							break;
							case 3:
							// Delete Grocery Item
							System.out.println("\nType in Grocery Name for Deleting -\n");
							
							String deleteGroceryText = input.nextLine();
							G1.deleteGrocery(deleteGroceryText);
							break;


							
							case 4: 
							// sell grocery
							

							System.out.println("\nType in Grocery Name for selling -\n");
							
							String sellGroceryText = input.nextLine();
							G1.sellGrocery(sellGroceryText); 

							break;
							case 5: 
							// restock grocery
							System.out.println("\nType in Grocery Name for restocking -");
							
							String restockGroceryText = input.nextLine();
							G1.restockGrocery(restockGroceryText);

							break;

							case 6:
							inManagingAndSearching=false;
							break;
							default: 
							System.out.println("\nSomething Went Wrong!!\n");

						}
		
					}
						break;
						case 3:
						// populate shop 
						
						

			
							System.out.println("\n Adding dummy Grocery Items to populate the shop . . . . . .\n");

							String[] dummy= {"Apple", "Orange", "Tomatoes", "Potaotes" , "Bread", "Frying Pan", "Kitchen Knife", "Soap", "Shampoo", "ToothPaste"};
				
							for (int i=0; i<10; i++){
								if(i<5){

									Edibles ed1 = new Edibles(dummy[i], "BestFood", 25, 50, 5);
						
										if (G1.insertGrocery(ed1)) {
											System.out.println("\nAdding dummy Edible Grocery was Successful \n");
										} else {
											System.out.println("\nSorry NonEdible Grocery Stock Full. Plz sell the grocery product in a different shop. You can always create a new shop..... \n"); 
										}
								} else {

									
									NonEdibles Ned1 = new NonEdibles(dummy[i], "BestBrand", 25, 50, "materials");
									
									if (G1.insertGrocery(Ned1)) {
										System.out.println("\nAdding dummy NonEdible Grocery was Successful \n");
									} else {
												System.out.println("\nSorry NonEdible Grocery Stock Full. Plz sell the grocery product in a different shop. You can always create a new shop..... \n");
								}
								
							}
				
						}
						System.out.println("\n Populating the shop with dummy values has been successful. . . . . . .\n");
				
				
							

						break ;
					case 4:
					
					// 4. Close the Program

			int option1;
			do {
				System.out.println("\nAre you sure you want to quit? \n 1. Yes \n 2. No \n");
				while (!input.hasNextInt()) {
						System.out.println("\nInvalid Option. Plz Try again! \n Are you sure you want to quit? \n 1. Yes \n 2. No ");
						input.next(); 
				}
				option1 = input.nextInt();
				input.nextLine();
			} while (option1 <= 0 && option1>2);
	
			switch(option1) {
				case 1:
					// 1. Will Go to Close Program Route
					isProgrameOpen = false;
					System.out.println("\nThank you for using the Program. In order to initiate the program again, type 'java Start' \n");

					
					break;

				case 2:
					// 2. Continue Programe 

					
					break;
	
				default:
					System.out.println("\nSomething Went Wrong. Please try again!\n");

				}
							
				}
			

}	


	}
}
