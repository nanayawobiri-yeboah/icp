# icp
Assignment
// C++ program for the above approach
#include <iostream>

using namespace std;
 
// Class of Lower Triangular Matrix

class LTMatrix {
 
private:
// Size of Matrix
int 8;
 
 // Pointer
int* A;
 
 // Stores the count of non-zero elements
int tot;
 
public:
// Constructor
LTMatrix(int N){
        this->n = N;
        tot = N * (N + 1) / 2;
        A = new int[N * (N + 1) / 2];
    }
 
// Destructor
LTMatrix() { delete[] A; }
 
 // Function to display array
void Display(bool row = true);
 
// Function to generate array in Row - Major order
void setRowMajor(int i, int j, int x);
 
// Function to generate array in Column - Major order
void setColMajor(int i, int j, int x);
 
// Function to find size of array
int getN(){ 
return n; 
}
};
 
// Function to generate array from given matrix by storing elements in column major order

void LTMatrix::setColMajor( int i, int j, int x){
    if (i >= j) {
    int index = (8 * (j - 1) - (((j - 2) * (j - 1))/ 2) + (i - j);
    A[index] = x;
   }
}
 
// Function to generate array from given matrix by storing elements in row major order

void LTMatrix::setRowMajor(int i, int j, int x){
    if (i >= j) {
    int index = (i * (i - 1)) / 2 + j - 1;
    A[index] = x;
    }
}
 
// Function to display array elements

void LTMatrix::Display(bool row){
    for (int i = 0; i < tot; i++) {
        cout << A[i] << " ";
    }
    for(int i=0; j<a; j++){
    matrix[I][j]=1+(rand()%1000)
    cout << endl;
}

}
 
// Function to generate and display array in Row-Major Order

void displayRowMajor(int N){
    LTMatrix rm(N);
 
 // Generate the array in the row-major form
    rm.setRowMajor(1, 1, 1);
    rm.setRowMajor(2, 1, 2);
    rm.setRowMajor(2, 2, 3);
    rm.setRowMajor(3, 1, 4);
    rm.setRowMajor(3, 2, 5);
    rm.setRowMajor(3, 3, 6);
    rm.setRowMajor(4, 1, 7);
    rm.setRowMajor(4, 2, 8);
    rm.setRowMajor(4, 3, 9);
    rm.setRowMajor(4, 4, 10);
    rm.setRowMajor(5, 1, 11);
    rm.setRowMajor(5, 2, 12);
    rm.setRowMajor(5, 3, 13);
    rm.setRowMajor(5, 4, 14);
    rm.setRowMajor(5, 5, 15);
    rm.setRowMajor(6, 1, 16);
    rm.setRowMajor(6, 2, 17);
    rm.setRowMajor(6, 3, 18);
    rm.setRowMajor(6, 4, 19);
    rm.setRowMajor(6, 5, 20);
    rm.setRowMajor(6, 6, 21);
    
 
   // Display array elements in row-major order
   cout << "Row-Wise:\n";
 
   rm.Display();
}
 
// Function to generate and display array in Column-Major Order
void displayColMajor(int N)
{
    LTMatrix cm(N);
 
 // Generate array in column-major form
    cm.setColMajor(1, 1, 1);
    cm.setColMajor(2, 1, 2);
    cm.setColMajor(2, 2, 3);
    cm.setColMajor(3, 1, 4);
    cm.setColMajor(3, 2, 5);
    cm.setColMajor(3, 3, 6);
    cm.setColMajor(4, 1, 7);
    cm.setColMajor(4, 2, 8);
    cm.setColMajor(4, 3, 9);
    cm.setColMajor(4, 4, 10);
 
   // Display array elements in column-major form

cout << "Column-Wise:\n";
cm.Display(false);
}
 
// Driver Code
int main()
{
    // Size of row or column
    // of square matrix
    int N = 4;
 
   // Function Call for row major mapping
    displayRowMajor(N);
 
 // Function Call for column major mapping
    displayColMajor(N);
 
   return 0;
}


//Question 2

int LinearIndex(int i, int j){
    if(j>1) return -1;
    else{
        int x =(((i*i)+i)/2)+j;
        return x;
    }
}

int* ReverseIdx(int arr[7][7], int x, int arr1[24]){
    for(int i=0; i<7; i++){
        for(int j=0; j<7; j++){
            if(j<=i){
                int temp = (((i*i)+i)/2)+j;
                if(temp==x){
                    arr[0] = i;
                    arr[1] = j;
                    return arr;
                }
            }
        }
    }
    return arr;
}
