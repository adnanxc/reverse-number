# reverse-number
1. Write code with a function “reverse()” that takes an integer as parameter and returns the reverse number in the main function. Sametime, the “reverse()” function will call another void function named “sum()”, which takes the reversed number as an argument and calculate the sum of the digits of that reverse number.


#include <iostream>
using namespace std;

void sum(int y){
    int s = 0;
    while(y!=0){
        s = s + (y % 10);
        y = y/10;
    }
    cout << "Sum of the reverse number: " << s << endl;

}

int rev(int x){
    int rem , revNum = 0;

    while(x!=0){
        rem = x % 10;
        revNum = (revNum*10) + rem;
        x = x / 10;
    }
    sum(revNum);
    return revNum;

}


int main(){

    int num;
    cout << "Enter a number: ";
    cin >> num;
    int r = rev(num);
    cout << "Reverse Number: " << r << endl;
    return 0;
}
