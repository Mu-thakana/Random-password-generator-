
import java.util.Scanner;
import java.util.Random;
public class Password1{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        System.out.println("enter the length of the password:");
        int n=sc.nextInt();
        String up="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
        String lc="abcdefghijklmnopqrstuvwxyz";
        String num="0123456789";
        String sp="!@#$%^&*<>";
        String mix=up+lc+num+sp;
        char[] password=new char[n];
        Random r=new Random();
        for(int i=0;i<n;i++){
        password[i]=mix.charAt(r.nextInt(mix.length()));
        }
System.out.println("generated password is :"+new String(password));
    System.out.println(complexity(n));
}
       public static String complexity(int n){
        if(n<6){
        return "weak password";
        }
        else if(n<8){
        return "medium password";
        }
        else{
        return "Strong password";
        }
      }
}

