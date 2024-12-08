# Bubble-sort
#include<iostream>
using namespace std;

void bubble_sort(int arr[], int n) {
    bool is_sorted;  

    for (int i = 0; i < n-1; i++)  
    {
        is_sorted = true; 
        for (int j = 0; j < n-i-1; j++)  
        {
            if (arr[j] > arr[j+1])  
            {
                
                int t = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = t;
                is_sorted = false;  
            }
        }
        
        
        if (is_sorted) {
            cout << "Array is already sorted" << endl;
            return;  
        }
    }

    cout << "Array is sorted after the process." << endl;  
}

int main() {
    int arr[] = {23, 67, 89, 56, 34, 21};
    int n = sizeof(arr) / sizeof(arr[0]);  

    bubble_sort(arr, n);  

    
    cout << "Sorted array: ";
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
}
