# Candy-Machineimport java.util;

public class CandyMachine{

  static Scanner console= new Scannner(System.in);

  

  public static void main(String[]args)

  {

    CashRegister cashRegister= new CashRegister();

    Dispenser candy = new Dispenser(50,10);

    Dispenser chips= new Dispenser (50,20);

    Dispenser gum= new Dispenser(20,10);

    Dispenser cookies= new Dispenser(50,35);

    

    

    int choice;

    

    showSelection();

    choice= console.nextlnt();

    

        while(choice !=15)

        {

          switch(choice)

          {

            case 1:

              sellProduct(candy,cashRegister);

              break;

            case 2:

              sellProduct(chips,cashRegister);

              break;

            case 3:

              sellProduct(gum,cashRegister);

              break;

            case 4:

              sellProduct(cookies,cashRegister);

              break;

              

              default:

                System.out.println("Invalid selection, please select again");

                 }

          

          showSelection();

          choice= console.nextlnt();

          }

 

       public static void showSelection()

       {

            {

              System.out.println("Good day,"+"Welcome to our Candy Machine!");

              System.out.println("To get treats, please enter");

              System.out.println("1 for Candy");

              System.out.println("2 for Chips");

              System.out.println("3 for Gum");

              System.out.println("4 for Cookies");

              System.out.println("15 to exit");

            }

          

     public static void sellProduct(Dispenser product, CashRegister cRegister)

          {

            int price;

            int coinsInserted;

            int coinsRequired;

            

              if(product.getCount()>0)

              {

                price= product.getProductCost();

                coinsRequired= price;

                coinsInserted= 0;

                

              while(coinsRequired>0)

              {

                System.out.println("Please insert"+ coinsRequired + "peso:");

                

                coinsInserted= coinsInserted

                                   + console.nextlnt();

                coinsRequired= price

                                - coinsInserted;

              }

              System.out.println();

              

              

              cRegistet.acceptAmount(coinsInserted);

              product.makeSale();

              

                System.out.println("Here's your treat"+"enjoy!");

                }

                

                else

                   System.out.println("Please select other treats because your choice is already sold out.");

             }

         

              }

  }

  }

          
