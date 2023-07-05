#include <iostream> 
 
int main() { 
// Создаем и инициализируем исходный массив 
int arr[] = {5, 2, 7, 8, 5, 9, 3}; 
int size = sizeof(arr) / sizeof(arr[0]); 
 
// Находим максимальный элемент 
int maxElement = arr[0]; 
for (int i = 1; i < size; i++) { 
if (arr[i] > maxElement) { 
maxElement = arr[i]; 
} 
} 
 
// Создаем новый массив без максимального элемента 
int newArr[size]; 
int newSize = 0; 
for (int i = 0; i < size; i++) { 
if (arr[i] != maxElement) { 
newArr[newSize] = arr[i]; 
newSize++; 
} 
} 
 
// Выводим новый массив 
for (int i = 0; i < newSize; i++) { 
std::cout « newArr[i] « " "; 
} 
return 0; 
}
