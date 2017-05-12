# BagelTest
//*******************************************************************
// Dear CompileJava users,
//
// CompileJava has been operating since 2013 completely free. If you
// find this site useful, or would otherwise like to contribute, then
// please consider a donation (link in 'More Info' tab) to support
// development of the new CompileJava website (stay tuned!).
//
// Most sincerely, Z.
//*******************************************************************

import java.lang.Math; // headers MUST be above the first class

// one class needs to have a main() method
public class HelloWorld
{
  
  public static void printRow(int n) {
    for(int i = 0; i < n; i++) {
    	System.out.print("O");
    }
    	//System.out.println("");
  }
  
  // arguments are passed using the text field below this editor
  public static void main(String[] args)
  {
    int bagels = 50;
    int levels = 4;
    int row = 1;
    boolean direction = true; //true for up, false for down
    
    while(true) {
      
      if(row == levels)
        direction = false;
      if(row == 1)
        direction = true;
      
      System.out.print(row + " ");
      
      if(bagels < row)
        printRow(bagels);
      else {
        printRow(row);
        //bagels -= row;
      }
      
      
      
      //printRow(row);
      bagels -= row;
      if(bagels < 0)
        break;
      System.out.print("           Bagels left: " + bagels);
      System.out.println("");
      
      
      
      if(direction)
        row++;
      else
        row--;
      
    }
    
  }
}
