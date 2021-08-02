# Guessing-a-number
import java.util.Random;
import java.util.Scanner;

class Game
{
    public int number;
    public int noOfGuesses;
    public int inputNumber;
    public int getNoOfGuesses() {
        return noOfGuesses;
    }

    public void setNoOfGuesses(int noOfGuesses) {
        this.noOfGuesses = noOfGuesses;
    }


     Game() {
        Random r= new Random();
        this.number = r.nextInt(100);
    }
    void takeUserInput()
    {
        System.out.println("Guess the number");
        Scanner sc=new Scanner(System.in);
        inputNumber= sc.nextInt();
    }
    boolean isCorrectNumber()
    {
        if (inputNumber==number)
        {
            System.out.println("Yes that is the correct number");
         return true;
        }
        else if(inputNumber<number)
        {
            System.out.println("Too less");
        }
        else if(inputNumber>number)
        {
            System.out.println("Too high");
        }
        return false;
    }
}
public class guessnumber {

    public static void main(String[] args)
    {

        Game g=new Game();
        boolean b=false;
        while(!b) {
            g.takeUserInput();
            b = g.isCorrectNumber();
            System.out.println(b);
        }
    }
}
