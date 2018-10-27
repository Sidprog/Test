# Test

Thsi my prog


def selectionSort(alist):
   for fillslot in range(len(alist)-1,0,-1):
       positionOfMax=0
       for location in range(1,fillslot+1):
           if alist[location]>alist[positionOfMax]:
               positionOfMax = location

       temp = alist[fillslot]
       alist[fillslot] = alist[positionOfMax]
       alist[positionOfMax] = temp

alist = [54,26,93,17,77,31,44,55,20]
selectionSort(alist)
print(alist)


#include <iostream>
#include <string>
using namespace std;
char caesar(char);
int main()
{
    string input;
    do
    {
        cout << "Enter cipertext and press enter to continue." << endl;
        cout << "Enter blank line to quit." << endl;
        getline(cin, input);
        string output = "";
        for (int x = 0; x < input.length(); x++)
        {
            output += caesar(input[x]);
        }
        cout << output << endl;
    }
    while (!input.length() == 0);
} //end main
 
char caesar(char c)
{
    if (isalpha(c))
    {
        c = toupper(c); //use upper to keep from having to use two seperate for A..Z a..z
        c = (((c - 65) + 13) % 26) + 65;
    }
    //if c isn't alpha, just send it back.
    return c;
}
