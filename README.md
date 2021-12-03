# Input-Output-array
#ask user to input data and display it using array
#include<iostream>
using namespace std;
int main()
{
	int num[5];   //declaring array with index 5 and datatype integer
	cout << "Enter 5 integer values: "<<endl;
	for (int j = 0; j < 5; j++)       //using for loop
	{
		cin >> num[j];
		while (cin.fail() != 0)  //if user enters a character or symbol then it will display a message 'Incorrect command' and will ask the user to enter the number again
		{
			cin.clear();
			cin.ignore();
			cout << "\aInvalid command! \nEnter the number again: ";
			cin >> num[j];   
		}
	}
	cout << "\nNumbers entered by the user are: " << endl;  
	for (auto number : num)  

	{
		cout << number << endl;  //display the numbers entered by the user
	}
	return 0;
}
