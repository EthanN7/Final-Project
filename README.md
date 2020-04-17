# Final-Project
final project for Java programming Spring 2020
import java.util.Scanner;//needed for Scanner class
import java.io.*;//needed for File IO classes

public class NguyenEProject1V1 {

	public static void main(String[] args) throws IOException {
		String option = "a"; //initializer for option variable
		while(!option.equalsIgnoreCase("D")) { // loop to run program that terminates if D character or any other character than those of the options is entered
			System.out.println("Thank you for choosing to use the Harvard Comprehensive Personality Test"); // welcome screen
			System.out.println("Option A - Append a personality test\nOption B - Evaluate the unprocessed personality tests\nOption C - Count and display how many people tested fell into each oersonality range\nOption D - Quit"); //displays menu options for user to choose
			Scanner keyboard = new Scanner(System.in); // creates scanner object for keyboard input
			System.out.println("Enter the letter of the option you would like to use. Warning if you enter any other character the program will terminate."); // prompts user to enter their option
			option = keyboard.nextLine(); //gets option input from user
			
			if (option.equalsIgnoreCase("A")) // runs option A
			{
				PrintWriter outputFile = new PrintWriter ("UnprocessedTests.txt"); //creates file StudentData.txt and opens it
				String runAgain = "y";
				while (runAgain.equalsIgnoreCase("y")) // loop that asks if user would like to run option A again
				{
					String studentAnswer; //holds student answer input
					String studentName; //holds student name input
					
					System.out.println("Enter your name"); // displays message prompting user to enter their name
					studentName = keyboard.nextLine(); // sets variable StudentName to input by the user
					outputFile.println(studentName); // writes student name to file
					while(studentName.equals("")) { //validation loop for student name
						System.out.println("You input invalid data. Please enter your name");
						studentName = keyboard.nextLine();
						outputFile.println(studentName);
						
					}
					
					System.out.println("Answer the questions in letters such as A, B, C, or D"); //display message prompting users to answer following questions
					
					//the rest of the following code is questions and answers from the Harvard Personality test followed by answer choices. Then the user input is recorded into the Student answer variable and written to the file if it passes the validation loop.
					System.out.println("1. When you get up in the morning, what do you usually have for breakfast:\nA. Eggs and toast\nB. Cereal\nC. Pop Tart\nD. Nothing");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("2. If you could have anything you desired, what would you have for breakfast?\nA. Eggs and toast\nB. Something else\nC. Pop Tart\nD. Cake");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("3. It's lunch time. You:\nA. Skip a meal because you are too busy or worried about your weight\nB. Get what you have spent all morning thinking about.\nC. Eat the food you brought with you.\nD. Find out what your friends are having and tag along.");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("4. A friend offers you some of his/her food. You:\nA. Take a bite because you are starving\nB. Take a bite to be polite\nC. Refuse because you are watching your weight\nD. Take 2 bites instead of just 1");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("5. Your future boyfriend/girlfriend offers you something to eat. It is:\nA. A cookie\nB. An apple\nC. A slice of pizza\nD. A carrot");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("6. Your dog is begging you for a treat. You give him:\nA. A dog biscuit\nB. Some cake\nC. Nothing, but you pet him\nD. Nothing and you push him away. Treats are bad for him. ");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("7. In a dream, you are in the world's best restaurant. You order:\nA. Everything on the menu. It's a dream, right?\nB. A salad. A big one with everything in it.\nC. Steak.\nD. A rich dessert.");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("8. You are stranded alone on a tropical island. What are the foods you have to have with you?\nA. Fruits and vegetables\nB. Meat and potatoes\nC. Ice cream, chocolate, and cake\nD. Chinese food");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("9. You are an infant and your mother is feeding you:\nA. Baby Cereal or formula\nB. Broccoli\nC. A cookie\nD. Nothing, she is doing something else");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					
					System.out.println("10. You are 6 years old. Your dad is feeding you:\nA. Pizza\nB. Spaghetti-Os\nC. Bubble gum\nD. Carrots");
					studentAnswer = keyboard.nextLine();
					outputFile.println(studentAnswer);
					while(!studentAnswer.equalsIgnoreCase("a") && !studentAnswer.equalsIgnoreCase("b") && !studentAnswer.equalsIgnoreCase("c") && !studentAnswer.equalsIgnoreCase("d"))
					{
						System.out.println("You input invalid data. Please answer the questions in letters such as A, B, C, or D");
						studentAnswer = keyboard.nextLine();
						outputFile.println(studentAnswer);
					}
					System.out.println("Would you like to run option A again? Press \'Y\' for yes. Press any other key to exit program.");
					runAgain = keyboard.nextLine();
					
				}
			outputFile.close();} //close file
			
			else if(option.equalsIgnoreCase("B")) // runs option B
			{
				//opens new file
				PrintWriter resultFile = new PrintWriter ("resultTests.txt");
				
				//accumulator for the total score of each answer added together assigned to Total variable
				int total = 0;
				
				//open unprocessed tests file in read mode
				File StudentData = new File("UnprocessedTests.txt");
				
				//sets variable inputFile to input by the user
				Scanner inputFile = new Scanner(StudentData);
				
				//loop to read every line of the file until file ends
				while (inputFile.hasNext())
				{
					
				String name = inputFile.nextLine();//sets variable name to the first line of the file
				resultFile.println(name); //prints name to new file
				
				//answer 1
				String answer = inputFile.nextLine(); //reads first answer
				
				//decision structure determining the value of Total depending on which letter is read in file
				if (answer.equalsIgnoreCase("a")) 
				{
					total = 3;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total = 1;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total = 6;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total = 2;
				}
				//following code does the same for the rest of the answers
				
				//answer 2
				//answer 2 begins Total accumulator
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 2;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 1;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 3;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 4;
				}
				
				//answer 3
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 2;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 1;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 3;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 4;
				}
				
				//answer 4
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 3;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 1;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 2;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 6;
				}
				
				//answer 5
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 1;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 2;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 5;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 3;
				}
				
				//answer 6
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 3;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 1;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 4;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 2;
				}
				
				//answer 7
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 2;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 1;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 3;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 4;
				}
				
				//answer 8
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 4;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 3;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 2;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 5;
				}
				
				//answer 9
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 6;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 4;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 8;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 2;
				}
				
				//answer 10
				answer = inputFile.nextLine();
				if (answer.equalsIgnoreCase("a"))
				{
					total += 7;
				}
				else if (answer.equalsIgnoreCase("b"))
				{
					total += 5;
				}
				else if (answer.equalsIgnoreCase("c"))
				{
					total += 1;
				}
				else if (answer.equalsIgnoreCase("d"))
				{
					total += 3;
				}
				
				//personality decision structure
				//the total at the end of the answers determines what personality type is chosen by the decision structure
				if (total >= 12 && total <= 20)
				{
					resultFile.println("Personality 1");
				}
				else if (total >= 21 && total <= 30)
				{
					resultFile.println("Personality 2");
				}
				else if (total >= 31 && total <= 42)
				{
					resultFile.println("Personality 3");
				}
				else if (total >= 43 && total <= 53)
				{
					resultFile.println("Personality 4");
				}
				
				}// end while loop
				
				resultFile.close();	//closes results file
				
				inputFile.close(); //closes unprocessed tests file
				
				//clears unprocessed tests file by opening it to write then closing
				PrintWriter outputFile = new PrintWriter ("UnprocessedTests.txt");
				outputFile.close();
				
			}// end option b
			
			//option c
			else if(option.equalsIgnoreCase("C"))
			{
				//open results file
				File resultFile = new File("resultTests.txt");
				//initiating variables to accumulate each personality type read in file
				int pers1 = 0;
				int pers2 = 0;
				int pers3 = 0;
				int pers4 = 0;
				Scanner readFile = new Scanner(resultFile);
				//loop to read file until it reaches the end
				while (readFile.hasNext())
				{
				//assigns personality variable to the read file
				String personality = readFile.nextLine();
				//decision structure that reads through file and accumulates how many times each personality is read by the variable.
				if (personality.equalsIgnoreCase("Personality 1"))
				{
					pers1 += 1; //adds 1 to the total number of personality 1 read in file
				}
				else if (personality.equalsIgnoreCase("Personality 2"))
				{
					pers2 += 1; //adds 1 to the total number of personality 2 read in file
				}
				else if (personality.equalsIgnoreCase("Personality 3"))
				{
					pers3 += 1; //adds 1 to the total number of personality 3 read in file
				}
				else if (personality.equalsIgnoreCase("Personality 4"))
				{
					pers4 += 1; //adds 1 to the total number of personality 4 read in file
				}
				
				}// end while loop
		
				readFile.close(); //close result file
				
				//displays message to user of the total amount of each personality in the file
				System.out.println("Personality Type 1: " + pers1);
				System.out.println("Personality Type 2: " + pers2);
				System.out.println("Personality Type 3: " + pers3);
				System.out.println("Personality Type 4: " + pers4);
				
			}//end of option c
			
		}//end of menu option choose loop
		
	}//closes public static void object
	
	}//closes public class
