
import java.util.Scanner;

class ATMInterface{

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
         
         double balance = 100000000.0;
         int choice;

         do { 
             System.out.println("\n========== ATM MENU ============");
             System.out.println("1.Check Balance");
             System.out.println("2.Doposite Money");
             System.out.println("3.Withdraw Money");
             System.out.println("4.Exit");
             System.out.println("Enter your choice");
             
             choice = sc.nextInt();

             switch (choice) {
                 case 1:
                    System.out.println("Current Balance: " + balance);
                    break;

                 case 2:
                    System.out.println("Enter Amount to deposite: ");
                    double deposit = sc.nextDouble();
                    balance += deposit;
                    System.out.println("Ru" + deposit + "deposited Successfully.");
                     break;

                 case 3:
                    System.out.println("Enter amount to withdraw: ");
                    double withdraw = sc.nextDouble();

                    if (withdraw <= balance) {
                        balance -= withdraw;
                        System.out.println("Ru" + withdraw + "deposited Successfully.");

                    } else {
                        System.out.println("Insufficient Balance");
                    }
                    break;

                 case 4:
                    System.out.println("Thank you for using the ATM");
                    

                 default:
                    System.out.println("Invalid choice...!");
             }
         } while (choice != 4);

    }
}
