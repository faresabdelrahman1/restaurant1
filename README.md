import java.util.ArrayList;
import java.util.HashMap;
import java.util.Scanner;

  public class waiter implements user {
      ArrayList<HashMap<String,Object>> wInfo = new ArrayList<>();
      Scanner input=new Scanner(System.in);
      customer object1;
     customer cust ;

      public waiter(customer cust){
          this.object1=cust;
          this.cust=cust;
          HashMap<String ,Object>waiter1=new HashMap<>();
          waiter1.put("name","Fares");
          waiter1.put("age",19);
          waiter1.put("id",1);
          wInfo.add(waiter1);

          HashMap<String ,Object>waiter2=new HashMap<>();
          waiter2.put("name","Abdelrahamn");
          waiter2.put("age",17);
          waiter2.put("id",2);
          wInfo.add(waiter2);

          HashMap<String ,Object>waiter3=new HashMap<>();
          waiter3.put("name","Ali");
          waiter3.put("age",18);
          waiter3.put("id",3);
          wInfo.add(waiter3);
      }

      public void signUp() {
          System.out.println("enter your id");
          int userId=input.nextInt();
          input.nextLine();

          boolean alreadyExist =false;
          for (HashMap<String,Object> waiters:wInfo){
              int id=(int) waiters.get("id");
              if (id==userId){
                  alreadyExist=true;
                  break;
              }
          }
          if (alreadyExist){
              System.out.println("you have already sign up");
          }
          else {
              System.out.println("enter your name ");
              String wName=input.nextLine();
              System.out.println("enter your age ");
              int wAge=input.nextInt();
              System.out.println("you have been signed up successfully");

              HashMap<String,Object> newWaiter=new HashMap<>();
              newWaiter.put("name",wName);
              newWaiter.put("age",wAge);
              newWaiter.put("id",userId);
              wInfo.add(newWaiter);


              System.out.println("name  "+wName);
              System.out.println("age  "+wAge);
              System.out.println("id  "+userId);
          }


      }

      chef object ;




      void viewOrder() {
          object1.listOrder();
      }

      boolean checkDelivrey() {
          if (object.iscooked()) {
              System.out.println("you shold delivrey the order");
          return true;
          } else {
              System.out.println(" wait until order be ready");
              return false;
          }

         }

      }

