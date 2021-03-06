# Algorithms βπ»

<div class="notice--primary" markdown="1">
β’ Definition    
: An algorithm is a finite set of instructions that accomplishes a particular task.   

β’ All algorithms must satisfy the following criteria:   
	β’	<strong><u>Input</u></strong> : There are zero or more quantities that are externally supplied    
	β’	<strong><u>Output</u></strong> : At least one quantity is produced    
	β’	<strong><u>Definiteness</u></strong> : Each instruction is clear and unambiguous   
	β’	<strong><u>Finiteness</u></strong> : If we trace out the instructions of an algorithm, then for all cases, the algorithm terminates after a finite number of step    
	β’	<strong><u>Effectiveness</u></strong> : Every instruction must be basic enough to be carried out. It must be feasible    
</div>



## π Sorting Algorithms

Sorting Algorithms are concepts that every competitive programmer must know. Sorting algorithms can be used for collections of numbers, strings, characters, or a structure of any of these types.   

μ λ ¬ μκ³ λ¦¬μ¦(sorting algorithm)μ΄λ μμλ€μ λ²νΈμμ΄λ μ¬μ  μμμ κ°μ΄ μΌμ ν μμλλ‘ μ΄κ±°νλ μκ³ λ¦¬μ¦μ΄λ€.   
ν¨μ¨μ μΈ μ λ ¬μ νμμ΄λ λ³ν© μκ³ λ¦¬μ¦μ²λΌ (μ λ ¬λ λ¦¬μ€νΈμμ λ°λ₯΄κ² λμνλ) λ€λ₯Έ μκ³ λ¦¬μ¦μ μ΅μ ννλ λ° μ€μνλ€. λ μ λ ¬ μκ³ λ¦¬μ¦μ λ°μ΄ν°μ μ κ·νλ μλ―Έμλ κ²°κ³Όλ¬Όμ μμ±νλ λ° νν μ μ©νκ² μ°μΈλ€. μ΄ μκ³ λ¦¬μ¦μ κ²°κ³Όλ λ°λμ λ€μ λ μ‘°κ±΄μ λ§μ‘±ν΄μΌ νλ€.

1. μΆλ ₯μ λΉ λ΄λ¦Όμ°¨μ(κ°κ°μ μμκ° μ  μμ μμμ λΉν΄ μ΄μ μ μμλ³΄λ€ μμ§ μμ μμ)μ΄λ€.   
2. μΆλ ₯μ μλ ₯μ μ¬λ°°μ΄νμ¬ λ§λ  μμ΄μ΄λ€.    

λλΆλΆ μ λ ¬μ μκ°λ³΅μ‘λλ <strong><u>O(n*logn)μ O(n^2)μ¬μ΄</u></strong>μ. 
νΉλ³ν κ²½μ° O(n)κΉμ§ κ°λ₯.

Internal sorting β main memoryμμ μΌμ΄λλ μ λ ¬
External sorting β secondary storage(νλλμ€ν¬)μμ μΌμ΄λλ μ λ ¬


## π Sorting Algorithm methods

**<u>Merge Sort</u>** and **<u>Quick Sort</u>** are the most popular algorithms.

### [1] Bubble Sort

Bubble sort is based on the idea of repeatedly comparing pairs of adjacent elements and then swapping their positions if they exist in the wrong order.   

<img width="206" alt="image" src="https://user-images.githubusercontent.com/63195670/149430315-b2b532ec-6ad4-427d-8a59-d60bbaec0044.png">

μ΄μλλ κ°λΌλ¦¬ λΉκ΅νμ¬ μλ¦¬λ₯Ό λ³κ²½ν΄λκ°λ λ°©μ!    
μ½κ° λ¨μμλ λΉκ΅ λμ μ€ κ°μ₯ ν° κ°μ λ§μ§λ§μ λ°°μΉνλ κ²μ λ°λ³΅νλ λλμ΄λΌκ³  μκ°νλ©΄ λ  λ―?   

#### π? Implementation

Assume that 
A[] is an unsorted array of n elements. This array needs to be sorted in ascending order. The pseudo code is as follows:

```cpp
void bubble_sort( int A[ ], int n ) {
    int temp;
    for(int k = 0; k< n-1; k++) {
        // (n-k-1) is for ignoring comparisons of elements which have already been compared in earlier iterations

        for(int i = 0; i < n-k-1; i++) {
            if(A[ i ] > A[ i+1 ] ) {
                // here swapping of positions is being done.
                temp = A[ i ];
                A[ i ] = A[ i+1 ];
                A[ i + 1 ] = temp;
            }
        }
    }
}
```

Lets try to understand the pseudo code with an example: A [ ] = { 7, 4, 5, 2 }   

<img width="710" alt="Screen Shot 2022-01-14 at 9 38 13 AM" src="https://user-images.githubusercontent.com/63195670/149431193-f674e858-9e3c-4745-ae9a-8f0d6910946c.png">

#### π? Performance 

The complexity of bubble sort is O(n^2) in both worst and average cases, because the entire array needs to be iterated for every element.   

β κΈ°λ³Έμ μΌλ‘ O(n^2). μ΄λ―Έ μ λ ¬μ΄ λμ΄ μμ κ²½μ°λ O(n).  


### [2] Selection Sort

The Selection sort algorithm is based on the idea of finding the minimum or maximum element in an unsorted array and then putting it in its correct position in a sorted array.   

Assume that the array A = [7, 5, 4, 2] needs to be sorted in ascending order.

The minimum element in the array (i.e. 2) is searched for and then swapped with the element that is currently located at the first position (i.e. 7). Now the minimum element in the remaining unsorted array is searched for and put in the second position, and so on.    

<img width="202" alt="image" src="https://user-images.githubusercontent.com/63195670/149432662-7f609e0a-1360-47a5-a4cb-de442cd3e645.png">

λλ arrayμμ κ°μ₯ ν° μλ₯Ό μ°Ύμ λ€μ, μ°Ύμ μλ₯Ό μ΄λ μ΄μ λ§¨ λμΈ nμλ¦¬μ λλλ€. 
λ€μ ν° μλ₯Ό μ°Ύμ λ€μ, μ΄λ μ΄μ n-1μλ¦¬μ λ£λλ€. μ΄ λ μ°Ύμ μμ ν΄λΉ μλ¦¬μ μλ μμ μλ¦¬λ₯Ό λ°κΎΌλ€.   

#### π? Implementation 

```cpp
void selection_sort (int A[ ], int n) {
        // temporary variable to store the position of minimum element

        int minimum;        
        // reduces the effective size of the array by one in  each iteration.

        for(int i = 0; i < n-1 ; i++)  {

           // assuming the first element to be the minimum of the unsorted array .
             minimum = i ;

          // gives the effective size of the unsorted  array .

            for(int j = i+1; j < n ; j++ ) {
                if(A[ j ] < A[ minimum ])  {                //finds the minimum element
                minimum = j ;
                }
             }
          // putting minimum element on its proper position.
          swap ( A[ minimum ], A[ i ]) ; 
        }
   }
```
At ith iteration, elements from position 0 to i-1 will be sorted.   

<img width="697" alt="Screen Shot 2022-01-14 at 10 00 05 AM" src="https://user-images.githubusercontent.com/63195670/149433085-35f3e3b5-5f59-443e-874e-48717d5ea68f.png">

#### π? Performance 

To find the minimum element from the array of N elements, N β 1 comparisons are required. After putting the minimum element in its proper position, the size of an unsorted array reduces to  
N β 1 and then N β 2 comparisons are required to find the minimum in the unsorted array.

Therefore (N β 1) + (N β 2) + ....... +  1 = (N β (N β 1))/2 comparisons and N swaps result in the overall complexity of O(N^2).

O(n^2)μ performanceκ° λμ΄. -> bubble sortμ λκ°μ΄ O(n^2)μ΄μ§λ§ bubble sortμ λΉν΄ κ°μ κ΅ν μκ° μ μ. μ΄λ―Έ μ λ ¬μ΄ λμ΄ μμ΄λ O(n^2)μ.   


### [3] Insertion Sort

Insertion sort is based on the idea that one element from the input elements is consumed in each iteration to find its correct position i.e, the position to which it belongs in a sorted array.

It iterates the input elements by growing the sorted array at each iteration. It compares the current element with the largest value in the sorted array. If the current element is greater, then it leaves the element in its place and moves on to the next element else it finds its correct position in the sorted array and moves it to that position. This is done by shifting all the elements, which are larger than the current element, in the sorted array to one position ahead

<img width="199" alt="image" src="https://user-images.githubusercontent.com/63195670/149433655-9c2bfee1-6582-47c0-b496-9db14220583a.png">

μλ‘μ΄ ν€λ₯Ό λ£μ λ, μ λ ¬μ νκ³  μλ arrayμμ μμ μ΄ μ΄λμ λ€μ΄κ°μΌ ν μ§ κ²°μ ν λ€μ λ§λ μλ¦¬μ λ£λλ€.

#### π? Implementation 

```cpp
void insertion_sort (int A[ ], int n) 
{
     for( int i = 0 ;i < n ; i++ ) {
    /*storing current element whose left side is checked for its 
             correct position .*/

	      int temp = A[ i ];    
	      int j = i;

       /* check whether the adjacent element in left side is greater or
            less than the current element. */

          while( j > 0  && temp < A[ j -1 ]) {

           // moving the left side element to one position forward.
                A[ j ] = A[ j-1 ];   
                j= j - 1;

           }
         // moving current element to its  correct position.
           A[ j ] = temp;       
     }  
}
```
Take array A[] = [7,4,5,2].   

<img width="700" alt="Screen Shot 2022-01-14 at 10 14 26 AM" src="https://user-images.githubusercontent.com/63195670/149434276-3b893c69-6e15-46a3-9733-f287538d99d6.png">   


#### π? Performance 

In worst case,each element is compared with all the other elements in the sorted array. For N elements, there will be N^2 comparisons. Therefore, the time complexity is O(n^2).

β O(n^2). μ΄λ―Έ λͺ¨λ  ν€κ° μ λ ¬λμ΄ μμΌλ©΄ O(n)  
μ§§μ listμμ λ¨μνκ³  μ’μ.   
μ΄λ―Έ λΆλΆμ μΌλ‘ μ λ ¬μ΄ λμ΄ μλ κ²½μ°μ μ’λ€.   


<div class="notice--primary" markdown="1">
π <strong><u>μ¬κΈ°μ μ κΉ!</u> : <u>Selection Sort vs Insertion Sort</u></strong>   

Selection sortλ μ λ ¬λμ΄ μμ§ μμ μλ₯Ό μ λΆ νμΈν΄ κ°μ₯ ν° μλ₯Ό μ°ΎμμΌ ν¨. μ λ ¬μ΄ μ λΆ λμ΄ μμ΄λ λͺ¨λ  μλ₯Ό λΉκ΅!     
Insertion sortλ μ νν μμΉμ λ€μ΄κ°λ κ²μ κ²°μ νκΈ° μν΄ μ λ ¬ μ€μΈ arrayλ₯Ό νμΈν΄μΌ ν¨. νμν κ°λ§ μ½κ³  μ λ ¬λ λ¦¬μ€νΈμμ λΉκ΅!   

Nκ°μ elementκ° μλ€κ³  κ°μ ν  λ,  Selectionμ nλ²λ§ μ°λ©΄ λ¨. λ€μμλΆν° μ°κΈ° λλ¬Έμ μ΄λ μ΄μ keyλ€μ΄ μ΄λν  νμκ° μμ§λ§, Insertionμ keyλ€μ΄ μ λΆ μ΄λν  μλ μκΈ° λλ¬Έμ writeκ° λ λ§μ΄ μΌμ΄λ¨. 
μλ₯Ό λ€μ΄, 2, 3, 4, 5, 1μ κ°μ insertion sortλ‘ μ λ ¬νλ€κ³  νλ©΄, λ§μ§λ§ 1μ μ λ ¬νκΈ° μν΄ 2, 3, 4, 5μ κ°μ΄ ν μΉΈμ© μ΄λν΄μΌ ν¨.
λ§μ½ writeλΉμ©μ΄ λΉμ κ²½μ° (μλ₯Ό λ€μ΄ flash memory) insertion sortλ³΄λ¨ selection sortκ° λ μ’μ.
</div>


<div class="notice--primary" markdown="1">
π <strong><u>μ¬κΈ°μ μ κΉ!</u> : <u>SUMMARY (Bubble, selection, insertion sort)</u></strong> 

Bubble, selection, insertion sortμ μκ°λ³΅μ‘λ worst caseλ O(n^2).   
λ§μ½ μ λΆ μ λ ¬λ λ¦¬μ€νΈλ₯Ό λΉκ΅νλ€λ©΄ bubble, insertion sortλ O(n)μ΄μ§λ§ selectionμ μ¬μ ν O(n^2).
</div>


### [4] Merge Sort

Merge sort is a **<u>divide-and-conquer algorithm</u> based on the idea of <u>breaking down a list into several sub-lists</u> until each sublist consists of a <u>single element</u> and merging those sublists in a manner that results into a sorted list.**

**<u>Idea</u>**:

- Divide the unsorted list into N sublists, each containing 1 element.
- Take adjacent pairs of two singleton lists and merge them to form a list of 2 elements. N will now convert into N/2 lists of size 2.
- Repeat the process till a single sorted list of obtained.

**<u>κ³Όμ  μ€λͺ</u>** : 

- λ¦¬μ€νΈμ κΈΈμ΄κ° 0 λλ 1μ΄λ©΄ μ΄λ―Έ μ λ ¬λ κ²μΌλ‘ λ³Έλ€. κ·Έλ μ§ μμ κ²½μ°μλ
- μ λ ¬λμ§ μμ λ¦¬μ€νΈλ₯Ό μ λ°μΌλ‘ μλΌ λΉμ·ν ν¬κΈ°μ λ λΆλΆ λ¦¬μ€νΈλ‘ λλλ€.
- κ° λΆλΆ λ¦¬μ€νΈλ₯Ό μ¬κ·μ μΌλ‘ ν©λ³ μ λ ¬μ μ΄μ©ν΄ μ λ ¬νλ€.
- λ λΆλΆ λ¦¬μ€νΈλ₯Ό λ€μ νλμ μ λ ¬λ λ¦¬μ€νΈλ‘ ν©λ³νλ€.

1. λΆν (Divide): μλ ₯ λ°°μ΄μ κ°μ ν¬κΈ°μ 2κ°μ λΆλΆ λ°°μ΄λ‘ λΆν νλ€.

2. μ λ³΅(Conquer): λΆλΆ λ°°μ΄μ μ λ ¬νλ€. λΆλΆ λ°°μ΄μ ν¬κΈ°κ° μΆ©λΆν μμ§ μμΌλ©΄ μν νΈμΆμ μ΄μ©νμ¬ λ€μ λΆν  μ λ³΅ λ°©λ²μ μ μ©νλ€.

3. κ²°ν©(Combine): μ λ ¬λ λΆλΆ λ°°μ΄λ€μ νλμ λ°°μ΄μ ν©λ³νλ€.


While comparing two sublists for merging, the first element of both lists is taken into consideration. While sorting in ascending order, the element that is of a lesser value becomes a new element of the sorted list. This procedure is repeated until both the smaller sublists are empty and the new combined sublist comprises all the elements of both the sublists.

<img width="713" alt="Screen Shot 2022-01-14 at 10 31 27 AM" src="https://user-images.githubusercontent.com/63195670/149435842-e0efc4b6-ce1e-460c-887c-5d16039b1d63.png">

#### π? Implementation 

```cpp
void merge(int A[ ] , int start, int mid, int end) {
 //stores the starting position of both parts in temporary variables.
	int p = start ,q = mid+1;
	
	int Arr[end-start+1] , k=0;
	
	for(int i = start ;i <= end ;i++) {
	    if(p > mid)      //checks if first part comes to an end or not .
	       Arr[ k++ ] = A[ q++] ;
	
	   else if ( q > end)   //checks if second part comes to an end or not
	       Arr[ k++ ] = A[ p++ ];
	
	   else if( A[ p ] < A[ q ])     //checks which part has smaller element.
	      Arr[ k++ ] = A[ p++ ];
	
	   else
	      Arr[ k++ ] = A[ q++];
	 }
	  for (int p=0 ; p< k ;p ++) {
	   /* Now the real array has elements in sorted manner including both 
	        parts.*/
	     A[ start++ ] = Arr[ p ] ;                          
	  }
}
```

π‘ **<u>2κ°μ μ λ ¬λ λ¦¬μ€νΈλ₯Ό ν©λ³(merge)νλ κ³Όμ </u>**

1. 2κ°μ λ¦¬μ€νΈμ κ°λ€μ μ²μλΆν° νλμ© λΉκ΅νμ¬ λ κ°μ λ¦¬μ€νΈμ κ° μ€μμ λ μμ κ°μ μλ‘μ΄ λ¦¬μ€νΈ(sorted)λ‘ μ?κΈ΄λ€.

2. λ μ€μμ νλκ° λλ  λκΉμ§ μ΄ κ³Όμ μ λνμ΄νλ€.

3. λ§μ½ λ μ€μμ νλμ λ¦¬μ€νΈκ° λ¨Όμ  λλκ² λλ©΄ λλ¨Έμ§ λ¦¬μ€νΈμ κ°λ€μ μ λΆ μλ‘μ΄ λ¦¬μ€νΈ(sorted)λ‘ λ³΅μ¬νλ€.

4. μλ‘μ΄ λ¦¬μ€νΈ(sorted)λ₯Ό μλμ λ¦¬μ€νΈ(list)λ‘ μ?κΈ΄λ€.


2 branched recursive function :

```cpp
void merge_sort (int A[ ] , int start , int end )
{
	if( start < end ) {
		int mid = (start + end ) / 2 ;           // defines the current array in 2 parts .
		merge_sort (A, start , mid ) ;                 // sort the 1st part of array .
		merge_sort (A,mid+1 , end ) ;              // sort the 2nd part of array.

         // merge the both parts by comparing elements of both the parts.
          merge(A,start , mid , end );   
   }                    
}
```

#### π? ν©λ³ μ λ ¬ (merge sort) μκ³ λ¦¬μ¦μ νΉμ§

π¬ **<u>λ¨μ </u>**  

- λ§μ½ λ μ½λλ₯Ό **<u>λ°°μ΄(Array)</u>**λ‘ κ΅¬μ±νλ©΄, μμ λ°°μ΄μ΄ νμνλ€.   
	- **<u>μ μλ¦¬ μ λ ¬(in-place sorting)</u>**μ΄ μλλ€.   
- λ ν¬λλ€μ ν¬κΈ°κ° ν° κ²½μ°μλ μ΄λ νμκ° λ§μΌλ―λ‘ λ§€μ° ν° μκ°μ  λ­λΉλ₯Ό μ΄λνλ€.    

π¬ **<u>μ₯μ </u>**

- μμ μ μΈ μ λ ¬ λ°©λ²   
	- λ°μ΄ν°μ λΆν¬μ μν₯μ λ λ°λλ€. μ¦, μλ ₯ λ°μ΄ν°κ° λ¬΄μμ΄λ  κ°μ μ λ ¬λλ μκ°μ λμΌνλ€. (O(nlogβn)λ‘ λμΌ)   
- λ§μ½ λ μ½λλ₯Ό **<u>μ°κ²° λ¦¬μ€νΈ(Linked List)</u>**λ‘ κ΅¬μ±νλ©΄, λ§ν¬ μΈλ±μ€λ§ λ³κ²½λλ―λ‘ **<u>λ°μ΄ν°μ μ΄λμ λ¬΄μν  μ μμ μ λλ‘ μμμ§λ€</u>**.   
	- **<u>μ μλ¦¬ μ λ ¬(in-place sorting)λ‘ κ΅¬ν</u>**ν  μ μλ€.   
- λ°λΌμ **ν¬κΈ°κ° ν° λ μ½λλ₯Ό μ λ ¬ν  κ²½μ°μ <u>μ°κ²° λ¦¬μ€νΈλ₯Ό μ¬μ©</u>νλ€λ©΄, ν©λ³ μ λ ¬μ ν΅ μ λ ¬μ ν¬ν¨ν <u>λ€λ₯Έ μ΄λ€ μ‘λ ¬ λ°©λ²λ³΄λ€ ν¨μ¨μ </u>μ΄λ€.**   


#### π? Performance 

The list of size N is divided into a max of logN parts, and the merging of all sublists into a single list takes O(N) time, the worst case run time of this algorithm is <strong><u>O(N*logN)</u></strong>

- **<u>λΆν  λ¨κ³</u>**
	- λΉκ΅ μ°μ°κ³Ό μ΄λ μ°μ°μ΄ μνλμ§ μλλ€.
- **<u>ν©λ³ λ¨κ³</u>**
	- **<u>λΉκ΅ νμ</u>**   
		<img width="475" alt="Screen Shot 2022-01-17 at 1 09 29 PM" src="https://user-images.githubusercontent.com/63195670/149706814-5875246c-c8a9-421c-af2f-a05f259d92ef.png">   

		- μν νΈμΆμ κΉμ΄ (ν©λ³ λ¨κ³μ μ)
			- λ μ½λμ κ°μ nμ΄ 2μ κ±°λ­μ κ³±μ΄λΌκ³  κ°μ (n=2^k)νμ λ, **<u>n=2^3μ κ²½μ°</u>**, 2^3 -> 2^2 -> 2^1 -> 2^0 μμΌλ‘ μ€μ΄λ€μ΄ μν νΈμΆμ κΉμ΄κ° 3μμ μ μ μλ€. μ΄κ²μ μΌλ°ννλ©΄ **n=2^kμ κ²½μ°, <u>k(k=logβn)</u>μ**μ μ μ μλ€.
			- **<u>k=logβn</u>**

		- κ° ν©λ³ λ¨κ³μ λΉκ΅ μ°μ°
			- ν¬κΈ° 1μΈ λΆλΆ λ°°μ΄ 2κ°λ₯Ό ν©λ³νλ λ°λ μ΅λ 2λ²μ λΉκ΅ μ°μ°μ΄ νμνκ³ , λΆλΆ λ°°μ΄μ μμ΄ 4κ°μ΄λ―λ‘ 24=8λ²μ λΉκ΅ μ°μ°μ΄ νμνλ€. λ€μ λ¨κ³μμλ ν¬κΈ° 2μΈ λΆλΆ λ°°μ΄ 2κ°λ₯Ό ν©λ³νλ λ° μ΅λ 4λ²μ λΉκ΅ μ°μ°μ΄ νμνκ³ , λΆλΆ λ°°μ΄μ μμ΄ 2κ°μ΄λ―λ‘ 4X2=8λ²μ λΉκ΅ μ°μ°μ΄ νμνλ€. λ§μ§λ§ λ¨κ³μμλ ν¬κΈ° 4μΈ λΆλΆ λ°°μ΄ 2κ°λ₯Ό ν©λ³νλ λ°λ μ΅λ 8λ²μ λΉκ΅ μ°μ°μ΄ νμνκ³ , λΆλΆ λ°°μ΄μ μμ΄ 1κ°μ΄λ―λ‘ 8X1=8λ²μ λΉκ΅ μ°μ°μ΄ νμνλ€. μ΄κ²μ μΌλ°ννλ©΄ νλμ ν©λ³ λ¨κ³μμλ μ΅λ nλ²μ λΉκ΅ μ°μ°μ μνν¨μ μ μ μλ€.
			- **<u>μ΅λ nλ²</u>**
		- μν νΈμΆμ κΉμ΄ λ§νΌμ ν©λ³ λ¨κ³ * κ° ν©λ³ λ¨κ³μ λΉκ΅ μ°μ° = **<u>nlogβn</u>**

	- **<u>μ΄λ νμ</u>**
		- μν νΈμΆμ κΉμ΄ (ν©λ³ λ¨κ³μ μ)
			- k=logβn
		- κ° ν©λ³ λ¨κ³μ μ΄λ μ°μ°
			- μμ λ°°μ΄μ λ³΅μ¬νλ€κ° λ€μ κ°μ ΈμμΌ λλ―λ‘ μ΄λ μ°μ°μ μ΄ λΆλΆ λ°°μ΄μ λ€μ΄ μλ μμμ κ°μκ° nμΈ κ²½μ°, λ μ½λμ μ΄λμ΄ 2nλ² λ°μνλ€.
		- μν νΈμΆμ κΉμ΄ λ§νΌμ ν©λ³ λ¨κ³ * κ° ν©λ³ λ¨κ³μ μ΄λ μ°μ° = 2nlogβn
- T(n) = nlogβn(λΉκ΅) + 2nlogβn(μ΄λ) = 3nlogβn = **<u>O(nlogβn)</u>**



### [5] Quick Sort

Quick sort is based on the divide-and-conquer approach based on the idea of **<u>choosing one element as a pivot element and partitioning the array around it</u>** such that: Left side of pivot contains all the elements that are less than the pivot element Right side contains all elements greater than the pivot

It reduces the space complexity and removes the use of the auxiliary array that is used in merge sort. Selecting a random pivot in an array results in an improved time complexity in most of the cases.

- λΆν  μ λ³΅ μκ³ λ¦¬μ¦μ νλλ‘, νκ· μ μΌλ‘ λ§€μ° λΉ λ₯Έ μν μλλ₯Ό μλνλ μ λ ¬ λ°©λ²
	- ν©λ³ μ λ ¬(merge sort)κ³Ό λ¬λ¦¬ ν΅ μ λ ¬μ λ¦¬μ€νΈλ₯Ό λΉκ· λ±νκ² λΆν νλ€.
	
	
**<u>κ³Όμ  μ€λͺ</u>** :    

- λ¦¬μ€νΈ μμ μλ ν μμλ₯Ό μ ννλ€. μ΄λ κ² κ³ λ₯Έ μμλ₯Ό νΌλ²(pivot) μ΄λΌκ³  νλ€.
- νΌλ²μ κΈ°μ€μΌλ‘ νΌλ²λ³΄λ€ μμ μμλ€μ λͺ¨λ νΌλ²μ μΌμͺ½μΌλ‘ μ?κ²¨μ§κ³  νΌλ²λ³΄λ€ ν° μμλ€μ λͺ¨λ νΌλ²μ μ€λ₯Έμͺ½μΌλ‘ μ?κ²¨μ§λ€. (νΌλ²μ μ€μ¬μΌλ‘ μΌμͺ½: νΌλ²λ³΄λ€ μμ μμλ€, μ€λ₯Έμͺ½: νΌλ²λ³΄λ€ ν° μμλ€)
- νΌλ²μ μ μΈν μΌμͺ½ λ¦¬μ€νΈμ μ€λ₯Έμͺ½ λ¦¬μ€νΈλ₯Ό λ€μ μ λ ¬νλ€.
	- λΆν λ λΆλΆ λ¦¬μ€νΈμ λνμ¬ μν νΈμΆ μ μ΄μ©νμ¬ μ λ ¬μ λ°λ³΅νλ€.
	- λΆλΆ λ¦¬μ€νΈμμλ λ€μ νΌλ²μ μ νκ³  νΌλ²μ κΈ°μ€μΌλ‘ 2κ°μ λΆλΆ λ¦¬μ€νΈλ‘ λλλ κ³Όμ μ λ°λ³΅νλ€.
- λΆλΆ λ¦¬μ€νΈλ€μ΄ λ μ΄μ λΆν μ΄ λΆκ°λ₯ν  λκΉμ§ λ°λ³΅νλ€.
	- λ¦¬μ€νΈμ ν¬κΈ°κ° 0μ΄λ 1μ΄ λ  λκΉμ§ λ°λ³΅νλ€.

1. λΆν (Divide): μλ ₯ λ°°μ΄μ νΌλ²μ κΈ°μ€μΌλ‘ λΉκ· λ±νκ² 2κ°μ λΆλΆ λ°°μ΄(νΌλ²μ μ€μ¬μΌλ‘ μΌμͺ½: νΌλ²λ³΄λ€ μμ μμλ€, μ€λ₯Έμͺ½: νΌλ²λ³΄λ€ ν° μμλ€)λ‘ λΆν νλ€.   
2. μ λ³΅(Conquer): λΆλΆ λ°°μ΄μ μ λ ¬νλ€. λΆλΆ λ°°μ΄μ ν¬κΈ°κ° μΆ©λΆν μμ§ μμΌλ©΄ μν νΈμΆ μ μ΄μ©νμ¬ λ€μ λΆν  μ λ³΅ λ°©λ²μ μ μ©νλ€.   
3. κ²°ν©(Combine): μ λ ¬λ λΆλΆ λ°°μ΄λ€μ νλμ λ°°μ΄μ ν©λ³νλ€.    

μν νΈμΆμ΄ νλ² μ§νλ  λλ§λ€ μ΅μν νλμ μμ(νΌλ²)λ μ΅μ’μ μΌλ‘ μμΉκ° μ ν΄μ§λ―λ‘, μ΄ μκ³ λ¦¬μ¦μ λ°λμ λλλ€λ κ²μ λ³΄μ₯ν  μ μλ€.   

#### π? Implementation 


**A[]** : array whose elements are to be sorted

**start** : Leftmost position of the array

**end** : Rightmost position of the array

**i** : Boundary between the elements that are less than pivot and those greater than pivot

**j** : Boundary between the partitioned and unpartitioned part of array

**piv** : Pivot element

```cpp
int partition ( int A[],int start ,int end) {
    int i = start + 1;
    int piv = A[start] ;            //make the first element as pivot element.
    for(int j =start + 1; j <= end ; j++ )  {
    /*rearrange the array by putting elements which are less than pivot
       on one side and which are greater that on other. */

          if ( A[ j ] < piv) {
                 swap (A[ i ],A [ j ]);
            i += 1;
        }
   }
   swap ( A[ start ] ,A[ i-1 ] ) ;  //put the pivot element in its proper place.
   return i-1;                      //return the position of the pivot
}
```

the recursive function Quick_sort :

```cpp
void quick_sort ( int A[ ] ,int start , int end ) {
   if( start < end ) {
        //stores the position of pivot element
         int piv_pos = partition (A,start , end ) ;     
         quick_sort (A,start , piv_pos -1);    //sorts the left side of pivot.
         quick_sort ( A,piv_pos +1 , end) ; //sorts the right side of pivot.
   }
}
```

Here we find the proper position of the pivot element by rearranging the array using partition function. Then we divide the array into two halves left side of the pivot (elements less than pivot element) and right side of the pivot (elements greater than pivot element) and apply the same step recursively.

Below `randpartition()` function chooses pivot randomly.

Letβs see the randomized version of the partition function :

```cpp
int rand_partition ( int A[ ] , int start , int end ) {
    //chooses position of pivot randomly by using rand() function .
     int random = start + rand( )%(end-start +1 ) ;

      swap ( A[random] , A[start]) ;        //swap pivot with 1st element.
     return partition(A,start ,end) ;       //call the above partition function
}
```
Use randpartiton() instead of partition() function in quicksort() function to reduce the time complexity of this algorithm!    


#### π? ν΅ (Quick sort) μκ³ λ¦¬μ¦μ νΉμ§

π¬ **<u>λ¨μ </u>**  

- μ λ ¬λ λ¦¬μ€νΈμ λν΄μλ ν΅ μ λ ¬μ λΆκ· ν λΆν μ μν΄ μ€νλ € μνμκ°μ΄ λ λ§μ΄ κ±Έλ¦°λ€.

π¬ **<u>μ₯μ </u>**   

- μλκ° λΉ λ₯΄λ€.
	- μκ° λ³΅μ‘λκ° O(nlogβn)λ₯Ό κ°μ§λ λ€λ₯Έ μ λ ¬ μκ³ λ¦¬μ¦κ³Ό λΉκ΅νμ λλ κ°μ₯ λΉ λ₯΄λ€.
- μΆκ° λ©λͺ¨λ¦¬ κ³΅κ°μ νμλ‘ νμ§ μλλ€.
	- ν΅ μ λ ¬μ O(log n)λ§νΌμ λ©λͺ¨λ¦¬λ₯Ό νμλ‘ νλ€.

π¬ ν΅ μ λ ¬μ λΆκ· ν λΆν μ λ°©μ§νκΈ° μνμ¬ νΌλ²μ μ νν  λ λμ± λ¦¬μ€νΈλ₯Ό κ· λ±νκ² λΆν ν  μ μλ λ°μ΄ν°λ₯Ό μ ννλ€.

- EX) λ¦¬μ€νΈ λ΄μ λͺ κ°μ λ°μ΄ν° μ€μμ ν¬κΈ°μμΌλ‘ μ€κ° κ°(medium)μ νΌλ²μΌλ‘ μ ννλ€.



#### π? Performance 

The worst case time complexity of this algorithm is O(N^2), but as this is randomized algorithm, its time complexity fluctuates between O(N^2) and O(NlogN) and mostly it comes out to be O(NlogN).

- **<u>μ΅μ μ κ²½μ°</u>**
	- **<u>λΉκ΅ νμ</u>**   
		<img width="463" alt="Screen Shot 2022-01-17 at 1 36 46 PM" src="https://user-images.githubusercontent.com/63195670/149708777-c59b0a5d-9143-4938-8c0c-a1f34d80510f.png">   

		- μν νΈμΆμ κΉμ΄
			- λ μ½λμ κ°μ nμ΄ 2μ κ±°λ­μ κ³±μ΄λΌκ³  κ°μ (n=2^k)νμ λ, n=2^3μ κ²½μ°, 2^3 -> 2^2 -> 2^1 -> 2^0 μμΌλ‘ μ€μ΄λ€μ΄ μν νΈμΆμ κΉμ΄κ° 3μμ μ μ μλ€. μ΄κ²μ μΌλ°ννλ©΄ n=2^kμ κ²½μ°, **<u>k(k=logβn)</u>**μμ μ μ μλ€.
			- **<u>k=logβn</u>**
		- κ° μν νΈμΆ λ¨κ³μ λΉκ΅ μ°μ°
			- κ° μν νΈμΆμμλ μ μ²΄ λ¦¬μ€νΈμ λλΆλΆμ λ μ½λλ₯Ό λΉκ΅ν΄μΌ νλ―λ‘ νκ·  nλ² μ λμ λΉκ΅κ° μ΄λ£¨μ΄μ§λ€.
			- **<u>νκ·  nλ²</u>**
		- μν νΈμΆμ κΉμ΄ * κ° μν νΈμΆ λ¨κ³μ λΉκ΅ μ°μ° = **<u>nlogβn</u>**
	- **<u>μ΄λ νμ</u>**
		- **λΉκ΅ νμλ³΄λ€ μ μΌλ―λ‘ <u>λ¬΄μν  μ μλ€</u>**.
	- μ΅μ μ κ²½μ° T(n) = O(nlogβn)

- **<u>μ΅μμ κ²½μ°</u>**
	: λ¦¬μ€νΈκ° κ³μ λΆκ· ννκ² λλμ΄μ§λ κ²½μ° (νΉν, μ΄λ―Έ μ λ ¬λ λ¦¬μ€νΈμ λνμ¬ ν΅ μ λ ¬μ μ€ννλ κ²½μ°)   

	<img width="283" alt="Screen Shot 2022-01-17 at 1 37 26 PM" src="https://user-images.githubusercontent.com/63195670/149708838-25f7ac6d-1f57-46aa-b4e6-98d7c5a411e3.png">   

	- **<u>λΉκ΅ νμ</u>**
		- μν νΈμΆμ κΉμ΄
			- λ μ½λμ κ°μ nμ΄ 2μ κ±°λ­μ κ³±μ΄λΌκ³  κ°μ (n=2^k)νμ λ, μν νΈμΆμ κΉμ΄λ nμμ μ μ μλ€.
			- **<u>n</u>**
		- κ° μν νΈμΆ λ¨κ³μ λΉκ΅ μ°μ°
			- κ° μν νΈμΆμμλ μ μ²΄ λ¦¬μ€νΈμ λλΆλΆμ λ μ½λλ₯Ό λΉκ΅ν΄μΌ νλ―λ‘ νκ·  nλ² μ λμ λΉκ΅κ° μ΄λ£¨μ΄μ§λ€.
			- **<u>νκ·  nλ²</u>**
		- μν νΈμΆμ κΉμ΄ * κ° μν νΈμΆ λ¨κ³μ λΉκ΅ μ°μ° = **<u>n^2</u>**
	- **<u>μ΄λ νμ</u>**
		- λΉκ΅ νμλ³΄λ€ μ μΌλ―λ‘ λ¬΄μν  μ μλ€.
		- μ΅μμ κ²½μ° **<u>T(n) = O(n^2)</u>**

- **<u>νκ· </u>**
	- νκ·  T(n) = <u>O(nlogβn)</u>
	- μκ° λ³΅μ‘λκ° O(nlogβn)λ₯Ό κ°μ§λ λ€λ₯Έ μ λ ¬ μκ³ λ¦¬μ¦κ³Ό λΉκ΅νμ λλ κ°μ₯ λΉ λ₯΄λ€.
	- ν΅ μ λ ¬μ΄ **λΆνμν λ°μ΄ν°μ μ΄λμ μ€μ΄κ³  λ¨Ό κ±°λ¦¬μ λ°μ΄ν°λ₯Ό κ΅νν  λΏλ§ μλλΌ, ν λ² κ²°μ λ νΌλ²λ€μ΄ μΆν μ°μ°μμ μ μΈλλ νΉμ±** λλ¬Έμ΄λ€.




### [6] Heap Sort

Heaps can be used in sorting an array. In max-heaps, maximum element will always be at the root. Heap Sort uses this property of heap to sort the array.   

Consider an array Arr which is to be sorted using Heap Sort.   

μ΅λ ν νΈλ¦¬λ μ΅μ ν νΈλ¦¬λ₯Ό κ΅¬μ±ν΄ μ λ ¬μ νλ λ°©λ²
λ΄λ¦Όμ°¨μ μ λ ¬μ μν΄μλ μ΅λ νμ κ΅¬μ±νκ³  μ€λ¦μ°¨μ μ λ ¬μ μν΄μλ μ΅μ νμ κ΅¬μ±νλ©΄ λλ€.

**<u>Idea</u>**:   

- **<u>Initially build a max heap</u> of elements in Arr.**
- The root element, that is Arr[1], will contain maximum element of Arr. After that, swap this element with the last element of Arr and heapify the max heap excluding the last element which is already in its correct position and then decrease the length of heap by one.
- Repeat the step 2, until all the elements are in their correct position.   

**<u>κ³Όμ  μ€λͺ</u>** : 

- μ λ ¬ν΄μΌ ν  nκ°μ μμλ€λ‘ μ΅λ ν(μμ  μ΄μ§ νΈλ¦¬ νν)μ λ§λ λ€.
	- λ΄λ¦Όμ°¨μμ κΈ°μ€μΌλ‘ μ λ ¬
- κ·Έ λ€μμΌλ‘ ν λ²μ νλμ© μμλ₯Ό νμμ κΊΌλ΄μ λ°°μ΄μ λ€λΆν° μ μ₯νλ©΄ λλ€.
- μ­μ λλ μμλ€(μ΅λκ°λΆν° μ­μ )μ κ°μ΄ κ°μλλ μμλ‘ μ λ ¬λκ² λλ€.


#### π? Implementation 

```cpp
void heap_sort(int Arr[ ])

{
	int heap_size = N;
	build_maxheap(Arr);
	for(int i = N; i >= 2 ; i-- )
	{
		swap|(Arr[ 1 ], Arr[ i ]);
		heap_size = heap_size - 1;
		max_heapify(Arr, 1, heap_size);
	}
}
```


#### π? ν μ λ ¬ (Heap sort) μκ³ λ¦¬μ¦μ νΉμ§  

π¬ **<u>μ₯μ </u>**

- μκ° λ³΅μ‘λκ° μ’μνΈ
- ν μ λ ¬μ΄ κ°μ₯ μ μ©ν κ²½μ°λ μ μ²΄ μλ£λ₯Ό μ λ ¬νλ κ²μ΄ μλλΌ κ°μ₯ ν° κ° λͺκ°λ§ νμν  λ μ΄λ€.



#### π? Performance 

max_heapify has complexity O(logN), bulid_maxheap has complexity O(N) and we run max_heapify N-1 times in heap_sort function, therefore complexity of heap_sort function is O(NlogN).

μκ°λ³΅μ‘λλ₯Ό κ³μ°νλ€λ©΄, 

- ν νΈλ¦¬μ μ μ²΄ λμ΄κ° κ±°μ logβn(μμ  μ΄μ§ νΈλ¦¬μ΄λ―λ‘)μ΄λ―λ‘ νλμ μμλ₯Ό νμ μ½μνκ±°λ μ­μ ν  λ νμ μ¬μ λΉνλ μκ°μ΄ logβnλ§νΌ μμλλ€.
- μμμ κ°μκ° nκ° μ΄λ―λ‘ μ μ²΄μ μΌλ‘ O(nlogβn)μ μκ°μ΄ κ±Έλ¦°λ€.
- T(n) = O(nlogβn)



### [7] Shell Sort

μ€λ¦μ°¨μμ κΈ°μ€μΌλ‘ μ λ ¬νλ€.

- βDonald L. Shellβμ΄λΌλ μ¬λμ΄ μ μν λ°©λ²μΌλ‘, μ½μμ λ ¬μ λ³΄μν μκ³ λ¦¬μ¦μ΄λ€.
- μ½μ μ λ ¬μ΄ μ΄λ μ λ μ λ ¬λ λ°°μ΄μ λν΄μλ λλ¨ν λΉ λ₯Έ κ²μ μ°©μ
	- μ½μ μ λ ¬μ μ΅λ λ¬Έμ μ : μμλ€μ΄ μ½μλ  λ, μ΄μν μμΉλ‘λ§ μ΄λ
	- μ¦, λ§μ½ μ½μλμ΄μΌ ν  μμΉκ° νμ¬ μμΉμμ μλΉν λ©λ¦¬ λ¨μ΄μ§ κ³³μ΄λΌλ©΄ λ§μ μ΄λμ ν΄μΌλ§ μ μλ¦¬λ‘ κ° μ μλ€.
	- μ½μ μ λ ¬κ³Ό λ€λ₯΄κ² μΈ μ λ ¬μ μ μ²΄μ λ¦¬μ€νΈλ₯Ό ν λ²μ μ λ ¬νμ§ μλλ€.

**<u>κ³Όμ  μ€λͺ</u>** : 

- λ¨Όμ  μ λ ¬ν΄μΌ ν  λ¦¬μ€νΈλ₯Ό μΌμ ν κΈ°μ€μ λ°λΌ λΆλ₯
- μ°μμ μ΄μ§ μμ μ¬λ¬ κ°μ λΆλΆ λ¦¬μ€νΈλ₯Ό μμ±
- κ° λΆλΆ λ¦¬μ€νΈλ₯Ό μ½μ μ λ ¬μ μ΄μ©νμ¬ μ λ ¬
- λͺ¨λ  λΆλΆ λ¦¬μ€νΈκ° μ λ ¬λλ©΄ λ€μ μ μ²΄ λ¦¬μ€νΈλ₯Ό λ μ μ κ°μμ λΆλΆ λ¦¬μ€νΈλ‘ λ§λ  νμ μκ³ λ¦¬μ¦μ λ°λ³΅
- μμ κ³Όμ μ λΆλΆ λ¦¬μ€νΈμ κ°μκ° 1μ΄ λ  λκΉμ§ λ°λ³΅


#### π? Implementation 

- μ λ ¬ν΄μΌ ν  λ¦¬μ€νΈμ κ° kλ²μ§Έ μμλ₯Ό μΆμΆν΄μ λΆλΆ λ¦¬μ€νΈλ₯Ό λ§λ λ€. μ΄λ, kλ₯Ό βκ°κ²©(gap)β μ΄λΌκ³  νλ€.
	- κ°κ²©μ μ΄κΉκ°: (μ λ ¬ν  κ°μ μ)/2
	- **μμ±λ λΆλΆ λ¦¬μ€νΈμ κ°μλ gapκ³Ό κ°λ€.**
- **κ° νμ λ§λ€ κ°κ²© kλ₯Ό <u>μ λ°μΌλ‘ μ€μΈλ€</u>.** μ¦, κ° νμ μ΄ λ°λ³΅λ  λλ§λ€ νλμ λΆλΆ λ¦¬μ€νΈμ μν κ°λ€μ κ°μλ μ¦κ°νλ€.
	- **κ°κ²©μ <u>νμ</u>λ‘ νλ κ²**μ΄ μ’λ€.
	- κ°κ²©μ μ λ°μΌλ‘ μ€μΌ λ μ§μκ° λμ€λ©΄ +1μ ν΄μ νμλ‘ λ§λ λ€.
- κ°κ²© kκ° 1μ΄ λ  λκΉμ§ λ°λ³΅νλ€.   

<img width="349" alt="Screen Shot 2022-01-17 at 3 18 42 PM" src="https://user-images.githubusercontent.com/63195670/149717751-46d88ed4-e303-465c-9a75-e5f395d2d522.png">    

```cpp
# include <stdio.h>
# define MAX_SIZE 10

// gapλ§νΌ λ¨μ΄μ§ μμλ€μ μ½μ μ λ ¬
// μ λ ¬μ λ²μλ firstμμ lastκΉμ§
void inc_insertion_sort(int list[], int first, int last, int gap){
  int i, j, key;

  for(i=first+gap; i<=last; i=i+gap){
    key = list[i]; // νμ¬ μ½μλ  μ«μμΈ iλ²μ§Έ μ μλ₯Ό key λ³μλ‘ λ³΅μ¬

    // νμ¬ μ λ ¬λ λ°°μ΄μ i-gapκΉμ§μ΄λ―λ‘ i-gapλ²μ§ΈλΆν° μ­μμΌλ‘ μ‘°μ¬νλ€.
    // j κ°μ first μ΄μμ΄μ΄μΌ νκ³ 
    // key κ°λ³΄λ€ μ λ ¬λ λ°°μ΄μ μλ κ°μ΄ ν¬λ©΄ jλ²μ§Έλ₯Ό j+gapλ²μ§Έλ‘ μ΄λ
    for(j=i-gap; j>=first && list[j]>key; j=j-gap){
      list[j+gap] = list[j]; // λ μ½λλ₯Ό gapλ§νΌ μ€λ₯Έμͺ½μΌλ‘ μ΄λ
    }

    list[j+gap] = key;
  }
}

// μΈ μ λ ¬
void shell_sort(int list[], int n){
  int i, gap;

  for(gap=n/2; gap>0; gap=gap/2){
    if((gap%2) == 0)(
      gap++; // gapμ νμλ‘ λ§λ λ€.
    )

    // λΆλΆ λ¦¬μ€νΈμ κ°μλ gapκ³Ό κ°λ€.
    for(i=0; i<gap; i++){
      // λΆλΆ λ¦¬μ€νΈμ λν μ½μ μ λ ¬ μν
      inc_insertion_sort(list, i, n-1, gap);
    }
  }
}

void main(){
  int i;
  int n = MAX_SIZE;
  int list[n] = {10, 8, 6, 20, 4, 3, 22, 1, 0, 15, 16};

  // μΈ μ λ ¬ μν
  shell_sort(list, n);

  // μ λ ¬ κ²°κ³Ό μΆλ ₯
  for(i=0; i<n; i++){
    printf("%d\n", list[i]);
  }
}
https://gmlwjd9405.github.io/2018/05/08/algorithm-shell-sort.html
```

#### π? μΈ μ λ ¬ (shell sort) μκ³ λ¦¬μ¦μ νΉμ§   

π¬ **<u>μ₯μ </u>**

- μ°μμ μ΄μ§ μμ λΆλΆ λ¦¬μ€νΈμμ μλ£μ κ΅νμ΄ μΌμ΄λλ©΄ λ ν° κ±°λ¦¬λ₯Ό μ΄λνλ€. λ°λΌμ κ΅νλλ μμλ€μ΄ μ½μ μ λ ¬λ³΄λ€λ μ΅μ’ μμΉμ μμ κ°λ₯μ±μ΄ λμμ§λ€.

- λΆλΆ λ¦¬μ€νΈλ μ΄λ μ λ μ λ ¬μ΄ λ μνμ΄κΈ° λλ¬Έμ λΆλΆ λ¦¬μ€νΈμ κ°μκ° 1μ΄ λκ² λλ©΄ μΈ μ λ ¬μ κΈ°λ³Έμ μΌλ‘ μ½μ μ λ ¬μ μννλ κ²μ΄μ§λ§ μ½μ μ λ ¬λ³΄λ€ λμ± λΉ λ₯΄κ² μνλλ€.

- μκ³ λ¦¬μ¦μ΄ κ°λ¨νμ¬ νλ‘κ·Έλ¨μΌλ‘ μ½κ² κ΅¬νν  μ μλ€.



#### π? Performance 

The list of size N is divided into a max of logN parts, and the merging of all sublists into a single list takes O(N) time, the worst case run time of this algorithm is <strong><u>O(N*logN)</u></strong>

μκ°λ³΅μ‘λλ₯Ό κ³μ°νλ€λ©΄,

- νκ· : T(n) = **<u>O(n^1.5)</u>**
- μ΅μμ κ²½μ°: T(n) = **<u>O(n^2)</u>**



<div class="notice--primary" markdown="1">
π <strong><u>μ¬κΈ°μ μ κΉ!</u> : <u>μ λ ¬ μκ³ λ¦¬μ¦ μκ°λ³΅μ‘λ λΉκ΅</u></strong>   

<img width="555" alt="Screen Shot 2022-01-17 at 1 19 30 PM" src="https://user-images.githubusercontent.com/63195670/149707448-e51a68ea-e42b-4d91-ada2-d78b6984ef1d.png">    

- λ¨μ(κ΅¬ν κ°λ¨)νμ§λ§ λΉν¨μ¨μ μΈ λ°©λ² : μ½μ μ λ ¬, μ ν μ λ ¬, λ²λΈ μ λ ¬        
- λ³΅μ‘νμ§λ§ ν¨μ¨μ μΈ λ°©λ² : ν΅ μ λ ¬, ν μ λ ¬, ν©λ³ μ λ ¬, κΈ°μ μ λ ¬
</div>


Sorting Algorithmμ μ¬κΈ°μ λ γ°οΈ
	
	
### π μΆμ²	
* [Sorting Algorithms μ°Έκ³  μ¬μ΄νΈ 1](https://www.hackerearth.com/practice/algorithms/sorting/bubble-sort/practice-problems/)
* [Sorting Algorithms μ°Έκ³  μ¬μ΄νΈ 2](https://gmlwjd9405.github.io)
* 2νλ 1νκΈ° λ λ°°μ΄ μλ£κ΅¬μ‘° μλ£..! 
