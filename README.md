# Exp-20

## Aim:
To implement and understand different sorting algorithms in C++, including selection sort, insertion sort, and bubble sort, and compare their operations.

## Software Used:
- Dev c++
  
## Theory:
Sorting is a fundamental operation in computer science that involves arranging data in a particular order. This assignment explores three sorting algorithms: Selection Sort, Insertion Sort, and Bubble Sort.

1.Selection Sort repeatedly finds the minimum element from the unsorted portion and swaps it with the first element of the unsorted portion.

2.Insertion Sort builds the final sorted array one element at a time by inserting each element in its correct position.

3.Bubble Sort repeatedly compares adjacent elements and swaps them if they are in the wrong order, effectively "bubbling" larger elements to the end. Each of these algorithms has different time complexities and efficiencies depending on the input size and order.

## Program 1: Selection Sort
<strong> Code: </strong>
<br>
```cpp
// Premish Ninawe
// 23070123092
// ENTC B1
#include <iostream>
using namespace std;

void swap(int *a, int *b){
    int temp;
    temp = *a;
    *a=*b;
    *b=temp;
}
void s_sort(int *a, int elements){
    int n=0;
    int *b;
    while (n != elements){
        b = a+1; 
        for(int i = 0; i < (elements-1)-n; i++){
            if(*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}
int main(){
    int no_el;
    cout << "How many elements in your array? "<<endl;
    cin >> no_el;
    int arr[no_el];
    cout << "Enter " << no_el << " Elements: "<<endl;
    for(int i=0; i<no_el; i++){
        cin >> arr[i];
    }
    cout << "Sorted Array: ";
    s_sort(&arr[0], no_el);
    for(int i=0; i<no_el; i++){
        cout << arr[i] << " ";
    }
    return 0;
}

```
<strong> Output: </strong>
<br>
![image](https://github.com/user-attachments/assets/5a34f3d2-ca77-4447-b985-1d3a275536fb)

## Program 2:  Insertion Sort
<strong> Code: </strong>
<br>
```cpp
// Premish Ninawe
// 23070123092
// ENTC B1
#include <iostream>
using namespace std;

void insertionsort(int arr[], int n){
    for (int i = 1; i < n; i++){
        int key = arr[i];
        int j = i - 1;
        while (j >= 0 && arr[j] > key){
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = key;
    }
}
int main(){
    int arr[] = {45, 39, 23, 67, 18};
    int n = sizeof(arr) / sizeof(arr[0]);
    cout << "Original array: ";
    for (int i = 0; i < n; i++){
        cout << arr[i] << " ";
    }
    insertionsort(arr, n);
    cout << "\nSorted array: ";
    for (int i = 0; i < n; i++){
        cout << arr[i] << " ";
    }
    return 0;
}

```
<strong> Output: </strong>
<br>
![image](https://github.com/user-attachments/assets/6c357a2e-fec5-4e47-b910-9917d5a2bdbf)

## Program 3: Bubble Sort
<strong> Code: </strong>
<br>
```cpp
// Premish Ninawe
// 23070123092
// ENTC B1
#include<iostream>
using namespace std;

void swap(int* a, int* b){
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}
int main(){
    int elements;
    cout << "How many elements in the array? : ";
    cin >> elements;
    int array[elements];
    cout << "Enter elements: ";
    for(int i = 0; i < elements; i++){
        cin >> array[i];
    }
    cout << "Original array: ";
    for(int i = 0; i < elements; i++){
        cout << array[i] << " ";
    }
    
    int n = 0;
    while(n != elements){
        for(int i = 0; i < elements - n - 1; i++){
            if(array[i] > array[i+1]){
                swap(&array[i], &array[i+1]);
            }
        }
        n++;
    }
    cout << "\nSorted array is: ";
    for(int i = 0; i < elements; i++){
        cout << array[i] << " ";
    }
    return 0;
}

```
<strong> Output: </strong>
<br>
![image](https://github.com/user-attachments/assets/d83f7605-06f9-473c-b75c-0141c22de2ea)

## Conclusion:
We learned to implement three sorting and they are Selection Sort, Insertion Sort, and Bubble Sort and understand their operational principles. 
