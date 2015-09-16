



import java.util.Scanner;

public class Simpletron {
   
     
    final int READ = 10;
    final int WRITE = 11;
    final int LOAD = 20;
    final int STORE = 21;
    final int ADD = 30;
    final int SUBTRACT = 31;
    final int DIVIDE = 32;
    final int MULTIPLY = 33;
    final int BRANCH = 40;
    final int BRANCHNEG = 41;
    final int BRANCHZERO = 42;
    final int HALT = 43;

   
    int accumulator = 0;

 static int programCounter = 0;
    int operationCode = 0;
    int operand = 0;
    int instructionRegister;
     
            static  int memory[] = new int[ 100 ];
   
      
      public static void main (String[] args){

        String welcome = "*** Welcome to Simpletron! ***" +
                     "\n*** Please enter your program one instruction  ***" +
                     "\n*** (or data word) at a time into the input    ***" +
                     "\n*** I will tyoe the location    ***" +
                     "\n*** number and a question mark (?). You then   ***" +
                     "\n*** type the word for that location. Press the ***" +
                     "\n*** GO button to execute  your program  **"+
                      "\n*** 0 ? **"       ;
 
                  System.out.println(welcome);
    

		         Scanner input = new Scanner( System.in ); //create a Scanner
                         //recieve an input
                          int instruction = input.nextInt();
                              if( instruction > 9999 ) return;
                               if( instruction < -9999 ) return;
                        System.out.println(programCounter);
                   while (instruction !=43){
                          System.out.println(programCounter);
                       instruction = input.nextInt();
            
                    if( instruction <= 9999 && instruction >= -9999 )    { 
                           
                        memory[programCounter] = instruction;
                        
                        programCounter++;
                        
                     if (programCounter==99) { 
                     
                   String abort  = "*** Memory Loaded  ***";
 
                    System.out.println(abort);
                         
                         
                         return;
                     
       
                    
                     }
                    
                    
                    
                    }  else {
                        break;
                    
                    }
       
     } 
                   
                   }
                 
    
    
    }




     
     
 
 





