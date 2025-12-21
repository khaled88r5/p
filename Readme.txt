1)Write a MATLAB program to print the number from 1 to n
in such away that when the number is odd, add one and
when the number is even , subtract one. Use N = 10,20,30,40.
Obtain the program time complexity and print your result.
If n=10 the result are 2,1,4,6,5,8,7,10,9.
for k = 1:4
n=input("enter n :")
for i=1:n
if mod(i,2)==0
disp(i-1)
else
disp(i+1)
end
end
d(k)=n
end
x=sort(d)
for k = 1 :4
t(k)=x(k)
end
plot(x,t)
--------------------------------------------------------------------------------------
2)Write a MATLAB program to print the sequence
5,9,13,.....,4n+1 and obtain the time complexity . if
10,20,30,40. Print your result.
for k = 1:4
n=input("enter n :")
for i=1:n
disp(4*i+1)
end
d(k)=n
end
x=sort(d)
t=x
plot(x,t)
----------------------------------------------------------------------------------------------
3)Write a program ∑ ∑ i ∗ jwhere n =30,50,10,40



for k = 1:4
n=input("enter n :")
s=0
for i=1:n
for j=1:n
s=s+i*j
end
end
d(k)=n
end
x=sort(d)
t=x.^2
plot(x,t)

-----------------------------------------------------
4)5,10,20,40,80...................
for k = 1:4
n=input("enter n :")
j=5
for i=1:n
disp(j)
j=j*2
end
d(k)=n
end
x=sort(d)
t=x
plot(x,t)
--------------------------------------------------------------------------------------
5)Sum all even number from 1 to n
for k = 1:4
n=input("enter n :")
s=0
for i=2:2:n
s=s+i
end
d(k)=n
end
x=sort(d)
t=x
plot(x,t)
-----------------------------------------------------------------------------------
6)Write a program to compute the sum of
1)Square number =12 + 22+ 32 ........n2
2)Cubic number=13 + 23+ 33 ........n3
Computer their time complexity

1)for k = 1:4
n=input("enter n :")
s=0
for i=1:n
s= s+i^2
end
d(k)=n
end
x=sort(d)
t=x
plot(x,t)
\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\\
2)for k = 1:4
n=input("enter n :")
s=0
for i=1:n
s= s+i^3
end
d(k)=n
end
x=sort(d)
t=x
plot(x,t)
---------------------------------------------------------------------
7)Write a MATLAB program to print the number from 1 to n
in such away that when the number is divisible by 5. Use N =
50,100,15,120 . Obtain the program time complexity.
for k = 1:4
n=input("enter n :")
for i=1:n
if mod(i,5)==0
disp(i)
end
end
d(k)=n
end
x=sort(d)
t=x
plot(x,t)
----------------------------------------------------------------------------
8)Write a MATLAB program to print the number from 4 to
4n. Use N = 10,20,30,40 . Obtain the program time
complexity.
for k = 1:4
n=input("enter n :")
for i=4:4*n
disp(i)
end
d(k)=n
end
x=sort(d)
t=x
plot(x,t)
-------------------------------------------------------------------------
9)Write a program to compute the sum of
1
2 – 3
2 + 52
- 7
2 +.......+(-1)n+1 (2n-1)2

n=input("enter n :")
s=0
for i=1:n
s=s+(-1)^(n+1)*(2*n-1)^2
end
disp(s)
--------------------------------------------------------------------------
10) Write a program to compute the sum of
1 + 1/2 +1/3..........+1/n
n=input("enter n :")
s=0
for i=1:n
s=s+1/n
end
disp(s)
------------------------------------------------------------------------------
11) Write program to compute the recursion function of n
where n is a nonnegative integer.
T(n) = 3T(n-1) where n>0
T(n)=1 where n=0 run the program for different values of
n =10,20,30,50. Hence compute its time complexity.

File of function
function f= t(n)
if n==0
f=1
elseif n>0
f=3*t(n-1)
end
//////////////////////////////////////////////////////////////////////
File run:

for i =1:4
n = input("enter n=")
t(n)
d(i)=n
end
x=sort(d)
for i = 1:4
t(i) = 3^x(i)
end
plot(x,t)
---------------------------------------------------------------------------
12) Write program to compute the recursion function of n
where n is a nonnegative integer.
T(n) = T(n-1)+T(n-2) where n>=3
T(n)=0 where n=1 and T(n)=1 where n=2 run the program
for different values of n =10,20,30,50. Hence compute its
time complexity.

File of function
function f= fib(n)
if n==1
f=0;
elseif n==2
f=1
elseif n>=3
f=fib(n-1)+fib(n-2);
end
/////////////////////////////////////////////////
File run:

for i =1:4
n = input("enter n=")
fib(n)
d(i)=n
end
x=sort(d)
for i = 1:4
t(i) = 2^x(i)
end
plot(x,t)

-------------------------------------------------------------------------------------------------------------------------------------------
1. Write a program to compute the multiplication of the following real matrices A = (A(i,j)){l\times n} and B = (B(i,j)){n\times m}. Obtain the program time complexity and print your results and save it. Test your program for the following values

clc;
clear;


A = input('Enter the first matrix (A): ');


B = input('Enter the second matrix (B): ');

[l, n] = size(A);
[p, m] = size(B);

if n ~= p
    disp('Error: The number of columns in matrix A must equal the number of rows in matrix B.');
else
   
    C = zeros(l, m);

   
    for i = 1:l
        for j = 1:m
            for k = 1:n
                C(i, j) = C(i, j) + A(i, k) * B(k, j);
            end
        end
    end

 
    disp('The product of matrices A and B is:');
    disp(C);
end

----------------------------------------------------------------------------------------------------------------------------------------

2. Write a program to print the numbers from 1 to N in such a way that when the number is odd, add one to the number, and when the number is even, subtract one. Obtain the program time complexity. Print your results and save it in case N=10, 20, 40.

clc;
clear;


for k = 1:3
   
    n = input(['Enter the number for n' num2str(k) ': ']);

   
    disp(['The modified series for n = ' num2str(n) ' is:']);

    for i = 1:n
        if mod(i, 2) == 0 
            modified_value = i - 1;
        else 
            modified_value = i + 1;
        end
        fprintf('%d ', modified_value);
    end
    fprintf('\n'); 
end

--------------------------------------------------------------------------------------------------------------------------

Let T(n) be the running time of mergesort(L, n)

**T(n) = { 2.T(n/2) + 3n, n > 1
{ 1, n = 1

Obtain T(n) and write a program to compute T(30), T(50). Hence compute the time complexity of your calculations and what about time complexity if we need to solve the above recurrence relation?

T30 = Tn(30);
T50 = Tn(50);

fprintf('T(30) = %d\n', T30);
fprintf('T(50) = %d\n', T50);

function T = Tn (n)
    if n == 1
        T = 1;
    else
        T = 2 * Tn(floor(n / 2)) + 3 * n;
    end
end

----------------------------------------------------------------------------------------------------------------------------

Write a program to

(i) generate Fibonacci numbers 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, ...

n = 10; 

series = fibonacci_series(n);
disp('Fibonacci series:');
disp(series);


function fib = fibonacci(n)
    if n == 0
        fib = 0;
    elseif n == 1
        fib = 1;
    else
        fib = fibonacci(n-1) + fibonacci(n-2);
    end
end


function series = fibonacci_series(n)
    series = zeros(1, n+1); % Initialize an array to store the series
    for i = 0:n
        series(i+1) = fibonacci(i); % Get Fibonacci number for each index
    end
end

----------------------------------------------------------------------------------------------------------------------------
Compute the sum 1² - 3² + 5² - 7² + ... + (-1)^(N+1)(2N - 1)²

Hence compute their time complexity.


function result = series_sum(n) % example value n=9

    result = 0;
    series_str = ''; % Initialize an empty string to build the series representation

    for i = 1:n
       
        odd_num = 2*i - 1;

        
        term = ((-1)^(i+1)) * (odd_num^2);

     
        if i > 1
            series_str = [series_str, ' + ', num2str(term)];
        else
            series_str = [series_str, num2str(term)];
        end

       
        result = result + term;
    end

    
    fprintf('The series is: %s\n', series_str);
    fprintf('The result is: %.0f\n', result);
end

----------------------------------------------------------------------------------------------------------------------

2. Write a program to print the multiplication table to the number n and obtain the program time complexity. Print your results and save it in case n=7. i.e.

n = input('Enter the value of n: ');

for i = 1:n
    for j = 1:n
       
      
        fprintf('%d*%d=%d', i, j, i*j);
        if j < n
            fprintf(', ');
        else
            fprintf('\n\n'); 
        end
    end
end

----------------------------------------------------------------------------------------------------------------------------------

Write a general program to compute the sum

∑<sub>i=1</sub><sup>N</sup> ∑<sub>j=1</sub><sup>i</sup> (A(i,j) / (i! * j!)) * x<sup>i</sup> * y<sup>j</sup>

where N, x, y and A = (A(i,j))<sub>N×N</sub> are given.

Then run your program in cases N=3, 4 and 5 where

[A=(A(i,j))=(\begin{matrix}-1&0&4&10&12\ 3&-5&-5&5&0\ 5&-3&-2&6&0\ 7&-3&-3&-2&6\ 9&4&8&4&1\end{matrix})]

with x = 0.1 and y = 0.4. Hence, compute their time complexity.



A = input('Enter the matrix A as an N x N array: ');


x = input('Enter the value of x: ');
y = input('Enter the value of y: ');


for N = [3, 4, 5]
    if N > size(A, 1)
        fprintf('Skipping N = %d as it exceeds the matrix size.\n', N);
        continue;
    end

    sum_result = 0; % Initialize the sum

   
   
    for i = 1:N
        for j = 1:N
            term = (A(i, j) / (i * j)) * (x^i) * (y^j);
            sum_result = sum_result + term;
        end
    end

    
    fprintf('The sum for N = %d is: %.4f\n', N, sum_result);
end

----------------------------------------------------------------------------------------------------------------------------------------
1. Write a Mat lab program to print the numbers from 1 to N in such a way that when the number is odd, add one and when the number is even, subtract one. Use N=10, 20, 30, 40. Obtain the program time complexity and print your results and save it.

For Example If N=10 the results are: 2, 1, 4, 3, 6, 5, 8, 7, 10, 9.


clc;
clear;

for k=1:4
    n=input('n= ');
    for i=1:n %T.C=O(n)
        if mod(i, 2)==1 %odd number
            disp(i+1);
        else %even number
            disp(i-1);
        end
    end
    d(k)=n;
end

y=sort(d);
for k=1:4
    t(k)=y(k);
end

plot(y,t)

---------------------------------------------------------------------------------------------------------------------------------------

2. Write a Mat lab program to print the sequence 5, 9, 13, ..., 4N+1 and obtain the program time complexity if 10, 20, 30, 40. Print your results and save it.



clc;
clear;

for k=1:4
    n=input('n= ');
    for i=1:n %T.C=O(log(n))
        i=4*i+1;
        disp(i)
    end
end

---------------------------------------------------------------------------------------------------------------------------------------
1. Write a Mat lab program to print the numbers which is divisible by 5 from 1 to N. Use N=50, 100, 150, 200. Obtain the program time complexity and print your results and save it.


clc;
clear;


for k=1:4
    n=input('n= ');
    for i=1:n
        if mod(i,5)==0
            disp(i);
        end
    end
end
d(k)=n;



y=sort(d);
for k=1:4
    t(k)=y(k);
end

plot(y,t)

--------------------------------------------------------------------------------------------
2. Write a Mat lab program to print the integers from 4 to ..., 4N and obtain the program time complexity if N=10, 20, 30, 40. Print your results and save it.



clc;
clear;

%the code
for k=1:4
    n=input('n= ');
    for i=4:4*n
        disp(i);
    end
end
d(k)=n;

%for time complexity
%T.C=O(n)

y=sort(d);
for k=1:4
    t(k)=y(k);
end

plot(y,t)


--------------------------------------------------------------------------------------------------------
(1) Write a program to compute the recursion function of n and n is a nonnegative integer.

[T(n)=\begin{cases}3T(n-1)\ 1\end{cases}]
[n>0]
[n=0]

Run the program for different values of n = 10, 20, 30, 50. Hence compute its time complexity


for k=1:4
    n=input('n= ');
    %evaluate the function for each n
    T(n)
end

%define the function
function result = T(n)
    if n>0
        %recall the function
        result=3*T(n-1)
    elseif n==0
        result=1
    else
        return
    end
end

---------------------------------------------------------------------------------------------------------------

Write a program to compute the sum of

(i) 1² - 3² + 5² - 7² ... + (-1)^(N+1)(2N - 1)²

(ii) 1 + 1/2 + 1/3 + ... + 1/N

Hence compute their time complexity.



clc;
clear;

for k=1:10
    n=input('n= ');
    s=0;
    for i=1:n %O(n)
        i=1/i;
        s=s+i;
    end
    disp(s);
end

d(k)=n;

y=sort(d);
for k=1:10
    t(k)=y(k);
end

plot(y,t);


--------------------------------------------------------------------------

merge sort 


% --- Script section ---
A = [38, 27, 43, 3, 9, 82, 10];
sortedA = mergeSort(A);
disp(sortedA);
% --- Functions below ---
function sortedArray = mergeSort(array)
    if length(array) <= 1
        sortedArray = array;
        return;
    end
    mid = floor(length(array)/2);
    left = mergeSort(array(1:mid));
    right = mergeSort(array(mid+1:end));
    sortedArray = merge(left, right);
end

function merged = merge(left, right)
    i = 1; j = 1;
    merged = [];
    while i <= length(left) && j <= length(right)
        if left(i) <= right(j)
            merged = [merged left(i)];
            i = i + 1;
        else
            merged = [merged right(j)];
            j = j + 1;
        end
    end
    merged = [merged left(i:end) right(j:end)];
end



-----------------------------------------------------------------------------------------


quick sort 


A = [38, 27, 43, 3, 9, 82, 10];
sortedA = quick_Sort(A);
disp(sortedA);

function sortedArray = quick_Sort(array)
    if length(array) <= 1
        sortedArray = array;
        return;
    end
    
    pivot = array(1); % choose pivot
    left = array(array < pivot);
    right = array(array > pivot);
    equal = array(array == pivot);
    
    leftSorted = quick_Sort(left);
    rightSorted = quick_Sort(right);
    
    sortedArray = [leftSorted equal rightSorted];
end



--------------------------------------------------------------------------------
selection sort 


function selection_sort_main()
    % Main function
    arr = [64, 25, 12, 22, 11];
    fprintf("Original array: ");
    print_array(arr);
    arr = selection_sort(arr);
    fprintf("Sorted array: ");
    print_array(arr);
end

function arr = selection_sort(arr)
    n = length(arr);
    for i = 1:n-1
        % Assume current position has the minimum
        min_idx = i;
        % Iterate through unsorted part to find actual minimum
        for j = i+1:n
            if arr(j) < arr(min_idx)
                min_idx = j;
            end
        end
        % Swap elements
        temp = arr(i);
        arr(i) = arr(min_idx);
        arr(min_idx) = temp;
    end
end

function print_array(arr)
    for i = 1:length(arr)
        fprintf("%d ", arr(i));
    end
    fprintf("\n");
end



-------------------------------------------------------------------------------------


insertion sort 

function insertion_sort_main()
    % Main function
    arr = [12, 11, 13, 5, 6];
    arr = insertionSort(arr);
    printArray(arr);
end

function arr = insertionSort(arr)
    % Insertion sort implementation
    for i = 2:length(arr)
        key = arr(i);
        j = i - 1;
        % Move elements greater than key one position ahead
        while j >= 1 && arr(j) > key
            arr(j + 1) = arr(j);
            j = j - 1;
        end
        % Insert key at correct position
        arr(j + 1) = key;
    end
end

function printArray(arr)
    % Utility function to print array
    for i = 1:length(arr)
        fprintf("%d ", arr(i));
    end
    fprintf("\n");
end


-----------------------------------------------------------------------------------


linear search 


function linear_search_main()
    arr = [2, 3, 4, 10, 40];
    x = 40;
    result = search(arr, x);
    if result == -1
        fprintf("Element is not present in array\n");
    else
        fprintf("Element is present at index %d\n", result);
    end
end

function index = search(arr, x)
    n = length(arr);
    % Iterate through array to find x
    for i = 1:n
        if arr(i) == x
            index = i;     % Found -> return position
            return;
        end
    end
    index = -1; % Not found
end




-------------------------------------------------------------------------

bubble sort 


arr = [64, 34, 25, 12, 22, 11, 90];
arr = bubble_Sort(arr);
disp("Sorted array:");
disp(arr);

function arr = bubble_Sort(arr)
    n = length(arr);
    % Traverse through all array elements
    for i = 1:n
        swapped = false;
        % Last i-1 elements are already in place
        for j = 1:(n - i)
            % Swap if the element found is greater
            if arr(j) > arr(j + 1)
                temp = arr(j);
                arr(j) = arr(j + 1);
                arr(j + 1) = temp;
                swapped = true;
            end
        end
        % If no swap happened, array is already sorted
        if swapped == false
            break;
        end
    end
end


------------------------------------------------------------------------------------


heap sort

arr = [9, 4, 3, 8, 10, 2, 5];
arr = heapSort(arr);
disp("Sorted array:");
disp(arr);

function arr = heapSort(arr)
    n = length(arr);
    % Build max heap (rearrange array)
    for i = floor(n/2) : -1 : 1
        arr = heapify(arr, n, i);
    end
    % One by one extract elements from the heap
    for i = n : -1 : 2
        % Move current root to the end
        temp = arr(1);
        arr(1) = arr(i);
        arr(i) = temp;
        % Call max-heapify on the reduced heap
        arr = heapify(arr, i - 1, 1);
    end
end

function arr = heapify(arr, n, i)
    largest = i;
    l = 2 * i;      % left child index (MATLAB uses 1-based indexing)
    r = 2 * i + 1;  % right child index

    % If left child exists and is larger than root
    if l <= n && arr(l) > arr(largest)
        largest = l;
    end
    % If right child exists and is larger than largest so far
    if r <= n && arr(r) > arr(largest)
        largest = r;
    end
    % If largest is not root
    if largest ~= i
        temp = arr(i);
        arr(i) = arr(largest);
        arr(largest) = temp;

        % Recursively heapify the affected subtree
        arr = heapify(arr, n, largest);
    end
end