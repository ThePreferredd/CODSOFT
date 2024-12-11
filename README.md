//Number Guessing Game

#include <iostream>         
#include <cstdlib> 
using namespace std; 

int main() 
{ 

	int num, guess, numoftries = 0;
	
//	srand(time(0)); //this function sets the starting point for producing a series of pseudo-random integers
	
	num = rand() % 100 + 1; // generates random numbers between 1 and 100
	

 	cout <<"Welcome to Number Guessing Game!"<< endl;
 	cout<<"Please press enter after every entry until the correct answer"<<endl; 
    
    do //using the do while loop 
    {
    	cout<< "Guess a number between 1 and 100. "<< endl;
    	cin>> guess;
    	numoftries++;
    	
    	
    	if (guess > num)
    	cout<< "Too high, please try again"<<endl;
    	
    	else if (guess < num)
    	cout<< "Too Low, please try again"<<endl;
    	
    	else
    	cout<< "You got it in " << numoftries << "guesses"  	<<endl;
    
     } while (guess != num);
     
     
	return 0; 
}
