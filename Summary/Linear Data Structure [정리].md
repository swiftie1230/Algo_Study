# Linear Data Structure โ๐ป

<div class="notice--primary" markdown="1">
<u><strong>Reducing space</strong></u> and <u><strong>decreasing the time complexity</strong></u> of different tasks is the <u><strong>main aim of data structures</strong></u>.   

Basically, there are two types of data structure.   

1. Primitive data structure (๋จ์๊ตฌ์กฐ) : ํ๋ก๊ทธ๋๋ฐ์์ ์ฌ์ฉ๋๋ ๊ธฐ๋ณธ ๋ฐ์ดํฐ ํ์       
2. Non-primitive data structure (๋น๋จ์๊ตฌ์กฐ) : ๋จ์ํ ๋ฐ์ดํฐ๋ฅผ ์ ์ฅํ๋ ๊ตฌ์กฐ๊ฐ ์๋๋ผ, ์ฌ๋ฌ ๋ฐ์ดํฐ๋ฅผ ๋ชฉ์ ์ ๋ง๊ฒ ํจ๊ณผ์ ์ผ๋ก ์ ์ฅํ๋ ์๋ฃ ๊ตฌ์กฐ   

The primitive type of data structure is a kind of data structure that stores the data of only one type. It includes the predefined data structures such as char, float, int, and double.   

The non-primitive data structures are used to store the collection of elements. This data structure can be further categorized into   

1. <strong><u>Linear data structure (์ ํ๊ตฌ์กฐ)</u></strong> ์ ์ฅ๋๋ ์๋ฃ์ ์  ํ ๊ด๊ณ๊ฐ 1:1    
2. <strong><u>Non-Linear data structure (๋น์ ํ๊ตฌ์กฐ) : ๋ฐ์ดํฐ ํญ๋ชฉ ์ฌ์์ ๊ด๊ณ๊ฐ 1:n ๋๋ n:m</u></strong>    

<img width="645" alt="Screen Shot 2022-01-05 at 5 02 15 PM" src="https://user-images.githubusercontent.com/63195670/148181944-02411bc3-b487-492b-b84d-5182e9c75a2e.png">   

</div>


Linear data structure is a type of data structure where the arrangement of the data follows a linear trend. **The data elements are <u>arranged linearly</u> such that the element is directly linked to its previous and the next elements. As the elements are stored linearly, the structure supports <u>single-level storage of data</u>. And hence, <u>traversal of the data is achieved through a single run</u> only**.

## ๐ Characteristics

- It is a type of data structure where data is stored and managed in a linear sequence. 

- Data elements in the sequence are linked to one after the other.

- <u>Implementation</u> of the linear structure of data in a computerโs memory is <u>easy</u> as the **<u>data is organized sequentially</u>**.

- Array, queue. Stack, linked list, etc. are examples of this type of structure.

- The <u>data elements</u> stored in the data structure have **<u>only one relationship</u>**.

- <u>Traversal of the data elements</u> can be carried out in a **<u>single run</u>** as the data elements are stored in a <u>single level</u>.

- There is <u>poor utilization of the computer memory</u> if a structure storing data linearly is implemented.

- With the **<u>increase in the size of the data structure</u>, the <u>time complexity of the structure increases</u>**.

These structures can therefore be summarized as a type of data structure where the elements are stored sequentially and follow the order where:

- Only one first element is present which has one next element.

- Only one last element is present which has one previous element.

- All the other elements in the data structure have a previous and a next element

## ๐ List of data structure in a linear type of data structure

### [1] Array & List

**๋ฐ์ดํฐ ๊ฐฏ์๊ฐ ํ์คํ๊ฒ ์ ํด์ ธ ์๊ณ , ์์ฃผ ์ฌ์ฉ๋๋ค๋ฉด, ์ธ๋ฑ์ค๊ฐ ์ค์ํ๋ค๋ฉด ๋ฐฐ์ด**์ ์ฌ์ฉ, **์ธ๋ฑ์ค๊ฐ ์ค์ํ์ง ์์ ๊ฒฝ์ฐ์๋ ๋ฆฌ์คํธ**๋ฅผ ์ฌ์ฉํ๋ ๊ฒ ์ข์! 

#### โ๏ธ Arrary (๋ฐฐ์ด)

The array is that type of structure that stores homogeneous elements at memory locations **<u>which are contiguous</u>**. The **<u>same types</u> of objects are stored <u>sequentially</u> in an array**.    
The main idea of an array is that **multiple data of the same type can be stored together**.    
Before storing the data in an array, the **<u>size of the array has to be defined</u>**. Any element in the array can be accessed or modified and the elements stored are **<u>indexed</u>** to identify their locations. Simple traversal of the array can lead to the access of the elements.

- ๋ฐ์ดํฐ๊ฐ ๋ง์์ง๋ฉด ๊ทธ๋ฃน ๊ด๋ฆฌ์ ํ์์ฑ์ด ์๊ธฐ๋๋ฐ, ์ด๋ด ๋ ํ๋ก๊ทธ๋๋ฐ์์ ์ฌ์ฉ

- ์ฌ๋ฌ ๋ฐ์ดํฐ๋ฅผ ํ๋์ ์ด๋ฆ์ผ๋ก ๊ทธ๋ฃนํํด์ ๊ด๋ฆฌ ํ๊ธฐ ์ํ ์๋ฃ๊ตฌ์กฐ

- ๋ฐฐ์ด์ ์ด์ฉํ๋ฉด ํ๋์ ๋ณ์์ ์ฌ๋ฌ ์ ๋ณด๋ฅผ ๋ด์ ์ ์๊ณ , ๋ฐ๋ณต๋ฌธ๊ณผ ๊ฒฐํฉ ํ๋ฉด ๋ง์ ์ ๋ณด๋ ํจ์จ์ ์ผ๋ก ์ฒ๋ฆฌํ  ์ ์๋ค.

- ๋ฐฐ์ด ์ธ๋ฑ์ค๋ ๊ฐ์ ๋ํ ์ ์ผ๋ฌด์ดํ ์๋ณ์ (์ฐธ๊ณ ๋ก ๋ฆฌ์คํธ์์ ์ธ๋ฑ์ค๋ ๋ช ๋ฒ์งธ ๋ฐ์ดํฐ์ธ๊ฐ ์ ๋์ ์๋ฏธ๋ฅผ ๊ฐ์ง)

- ์ค์  ๋ฉ๋ชจ๋ฆฌ ์์ ์ ์ฅ๋๋ฏ๋ก ์์๊ฐ ์๊ณ , ์ธ๋ฑ์ฑ ๊ฐ๋ฅ.

- ๋ฐ์ดํฐ๋ฅผ ๋นจ๋ฆฌ ์ฝ์ด์ผ ํ  ๋ ์ฐ๊ธฐ ์ข์ผ๋ฉฐ, ๊ฐ์ฅ ๋ง์ด ์ฌ์ฉ๋จ.

##### ๐คฆ๐ปโโ๏ธ ๋ฐฐ์ด์ ํน์ง

- **ํฌ๊ธฐ๊ฐ ์ ํด์ ธ ์๋ค** / ๊ธฐ๋ฅ์ด ์๋ค 
(์ด๋ ๋ฐฐ์ด์ ์ฅ์ ์ด์ ๋จ์ ์ผ๋ก ๋ฐฐ์ด์ ๋ค๋ฅธ ์๋ฃ๊ตฌ์กฐ์ ์ข์ ๋ถํ์ผ๋ก ์ฌ์ฉ๋  ์ ์๋ค.)

- **์ธ๋ฑ์ค๋ฅผ ๊ฐ์ง๋ฉฐ, element์ ์ธ๋ฑ์ค๋ ๋ณ๊ฒฝ๋์ง ์๋๋ค**. 

- ์ ๊ด ๋ฐ์ดํฐ๋ฅผ ๋ฉ๋ชจ๋ฆฌ์ **์์ฐจ์ ์ผ๋ก ๋์ด**ํ  ์ ์๋ค.

- ์ธ๋ฑ์ค๋ฅผ ํ์ฉํ์ฌ **๋น ๋ฅด๊ฒ ์กฐํ**๊ฐ ๊ฐ๋ฅํ๋ค.

- **cache hit** (์ญ..์ปด๊ตฌ ์๊ฐ์ ๋์๋ ์น๊ตฌ ์๋ฝ ๏ฝฅ_๏ฝฅ)  ์ ๊ฐ๋ฅ์ฑ์ด ์ปค์ ธ์ **์ฑ๋ฅ**์ ํฐ ๋์์ด ๋๋ค.

- ์ธ๋ฑ์ค๋ฅผ ์ด์ฉํ์ฌ ๋ฐ์ดํฐ๋ฅผ ๊ฐ์ ธ์ค๋ ค๋ฉด ๋ฐ์ดํฐ์ ๋ํ ์ธ๋ฑ์ค ๊ฐ์ด ๊ณ ์ ๋์ด์ผ ํ๊ธฐ์, **์ญ์ ๋ element์ ๊ณต๊ฐ์ด ๊ทธ๋๋ก ๋จ๋๋ค. -> <u>๋ฉ๋ชจ๋ฆฌ์ ๋ญ๋น ์ด๋ ๊ฐ๋ฅ</u>**

##### ๐คฆ๐ปโโ๏ธ ๋ฐฐ์ด์ ํ๊ณ

- **๋ฐฐ์ด์ ๊ธธ์ด๋ฅผ ๋ฐ๊ฟ ์ ์๋ค**. ๊ฐ๋ณ ๋ฐฐ์ด๊ณผ ๊ฐ์ด ๊ธธ์ด๊ฐ ๋ณ๊ฒฝ ๊ฐ๋ฅํ ๋ฐฐ์ด์ ๊ฒฝ์ฐ, 
	- ๊ธฐ์กด์ ๋ฐฐ์ด์ ๊ทธ๋๋ก ๋๊ณ ,
	- ์๋ก์ด ๊ธธ์ด๋ก ์ง์ ๋ ๋ฐฐ์ด์ ๋ฐ๋ก ํ ๋น ํ (๋ฉ๋ชจ๋ฆฌ๊ฐ ์๋์ง ํ์ ํ์)
	- ๋ฐ์ดํฐ์ ๋ณต์ฌ๋ฅผ ์งํํ๊ณ , 
	- ๊ธฐ์กด์ ๋ฐฐ์ด์ ์ญ์ ํ๋ค.
	- ์ด 3๋ฒ์ ์์ + ๋ฉ๋ชจ๋ฆฌ ํ์ ์ด ํ์ํ๊ธฐ ๋๋ฌธ์ ๋ฆฌ์์ค ๋ญ๋น๊ฐ ํฌ๋ค.

- ์์ ๊ฐ์ ํ๊ณ๋ฅผ ํด๊ฒฐํ๊ธฐ ์ํด์ linked list ์๋ฃํ์ ํ์ฉํ  ์ ์๋ค. (ํ์, ํ ๋น, ๋ณต์ฌ, ์ญ์  ๋ฑ์ ๋ฆฌ์์ค ๋ญ๋น๊ฐ ์๋ค.)

- **๋ฐฐ์ด์ ์ธ๋ฑ์ค์ ๋ฐ๋ผ์ ๊ฐ์ ์ ์งํ๊ธฐ ๋๋ฌธ์, <u>element๊ฐ ์ญ์ ๋์ด๋ ๋น์๋ฆฌ(null)๊ฐ ๋จ๊ฒ ๋๋ค</u>. <u>(๋ถํ์ํ ๋ฉ๋ชจ๋ฆฌ ์ฐจ์ง)</u>**

- ์กฐ๊ฑด๋ฌธ์ ํตํด์ ๋น element๋ฅผ ์ ์ธํ  ์ ์์ผ๋, ์กฐ๊ฑด๋ฌธ์ ๋ง์ด ์ฌ์ฉํ๋ ๊ฒ์ ์ข์ง ์๋ค.

#### โ๏ธ List (๋ฆฌ์คํธ)

- ๋ฆฌ์คํธ๋ ๋ฐฐ์ด์ด ๊ฐ์ง๊ณ  ์๋ ์ธ๋ฑ์ค๋ผ๋ ์ฅ์ ์ ๋ฒ๋ฆฌ๊ณ  ๋์  ๋นํ์๋ ๋ฐ์ดํฐ์ ์ ์ฌ ๋ผ๋ ์ฅ์ ์ ์ทจํ Data Structure   

- **์ญ์ ํ ๋ฐ์ดํฐ๋ฅผ ๋ค์ ์์นํ element๋ก ๋ฉ๊พธ๋ฉด, <u>๋ฐ์ดํฐ๊ฐ ์์์ ๋ฐ๋ผ์ ๋นํ์์ด ์ฐ์์ ์ผ๋ก ์์น</u>ํ๋ฉฐ ์ด๋ฅผ <u>list(๋ฆฌ์คํธ)</u>** ๋ผ๊ณ  ํ๋ค.

- ๋ฆฌ์คํธ ์๋ฃ๊ตฌ์กฐ์ ํต์ฌ์ elements ๊ฐ์ ์์. ๋ฐ๋ผ์ ๋ฆฌ์คํธ๋ฅผ ๋ค๋ฅธ ๋ง๋ก๋ ์ํ์ค(sequence) ๋ผ๊ณ ๋ ๋ถ๋ฅธ๋ค. ์ฆ ์์๊ฐ ์๋ ๋ฐ์ดํฐ์ ๋ชจ์์ด ๋ฆฌ์คํธ์ด๋ค.   

- ๋ฆฌ์คํธ์์ ์ธ๋ฑ์ค๋ **<u>๋ช ๋ฒ์งธ ๋ฐ์ดํฐ์ธ๊ฐ</u>** ์ ๋์ ์๋ฏธ๋ฅผ ๊ฐ์ง๋ค. (๋ฐฐ์ด-Array์์์ ์ธ๋ฑ์ค๋ ๊ฐ์ ๋ํ ์ ์ผ๋ฌด์ดํ ์๋ณ์)   

- ๋น element๋ ํ์ฉํ์ง ์๋๋ค.   

- ์์ฐจ์ฑ์ ๋ณด์ฅํ์ง ๋ชปํ๊ธฐ ๋๋ฌธ์ spacial locality ๋ณด์ฅ์ด ๋์ง ์์์ cash hit๊ฐ ์ด๋ ต๋ค.   

- ๋ฆฌ์คํธ์ ๋ํ ํจ์ฉ์ ์ด๋ค ์ธ์ด๋ฅผ ์ฌ์ฉํ๋๋์ ๋ฐ๋ผ์ ๋ฌ๋ผ์ง๋ค. ํนํ ๋ง์ ์ธ์ด๊ฐ ๋ฆฌ์คํธ๋ฅผ ๊ธฐ๋ณธ์ ์ผ๋ก ์ง์ํ๊ธฐ ๋๋ฌธ์ ๋ฆฌ์คํธ๋ฅผ ์ง์  ๊ตฌํํ๋ ๊ฒฝ์ฐ๋ ์ค๊ณ  ์๋ค.


##### ๐คฆ๐ปโโ๏ธ list ์๋ฃ๊ตฌ์กฐ์ ๋ํ ๊ธฐ๋ฅ (operation)

์๋ฃ๊ตฌ์กฐ์์ ๊ฐ์ฅ ์ค์ํ ์ ์, **ํด๋น ์๋ฃ๊ตฌ์กฐ๊ฐ ์ด๋ ํ <u>๊ธฐ๋ฅ</u>์ ๊ฐ์ง๊ณ  ์๋๋๋ ๊ฒ**์ด๋ค.   
List์ ๋ํ๊ธฐ๋ฅ์ ๋ค์๊ณผ ๊ฐ๋ค :)

- ์ฒ์, ๋, ์ค๊ฐ์ ์๋ฆฌ๋จผํธ๋ฅผ ์ถ๊ฐ/์ญ์  ํ๋ ๊ธฐ๋ฅ
- ๋ฆฌ์คํธ์ ๋ฐ์ดํฐ๊ฐ ์๋์ง๋ฅผ ์ฒดํฌํ๋ ๊ธฐ๋ฅ
- ๋ฆฌ์คํธ์ ๋ชจ๋  ๋ฐ์ดํฐ์ ์ ๊ทผํ  ์ ์๋ ๊ธฐ๋ฅ

##### ๐คฆ๐ปโโ๏ธ ์ธ์ด๋ณ list ์ง์ ๋น๊ต

**_"C"_**

- ๋ฆฌ์คํธ๋ฅผ ์ง์ํ์ง ์๋๋ค. ๋์  ๋ฐฐ์ด์ ์ง์ํ๋ค.   
- ๋ฆฌ์คํธ๋ฅผ ์ฌ์ฉํ๋ ค๋ฉด ์ง์  ๋ง๋ค๊ฑฐ๋ ๋ผ์ด๋ธ๋ฌ๋ฆฌ๋ฅผ ์ฌ์ฉํด์ผํ๋ค. (๋ฐ๋ผ์ ๋ฆฌ์คํธ์ ๋ํ ๊น์ ์ดํด์ ์๋ชฉ์ด ํ์ํจ)


**_"Python"_**

- ๊ธฐ๋ณธ์ ์ผ๋ก ๋ฆฌ์คํธ๋ฅผ ์ ๊ณตํ๋ฉฐ, ๋ฐฐ์ด์ ์ ๊ณตํ์ง ์๋๋ค.
- ํ์ด์ฌ์์๋ ๋ฆฌ์คํธ๊ฐ ๋ฐฐ์ด์ด๋ค.
- ํ์ด์ฌ์ ๋ฆฌ์คํธ๋ ํฌ๊ธฐ๊ฐ ๊ฐ๋ณ์ ์ด๊ณ , ์ด๋ค ์์ ํ์์ด๋ ์ ์ฅํ  ์ ์๋ค๋ ์ฅ์ ์ ๊ฐ์ง๋ค. ๋์  C์ array ๋ณด๋ค ๋ฉ๋ชจ๋ฆฌ๋ฅผ ๋ ๋ง์ด ํ์๋ก ํ๋ค๋ ๋จ์ ์ด ์๋ค.

```python
numbers = [10, 20, 30, 40, 50]
numbers.pop(3) # 40 / 3๋ฒ์งธ ์ธ๋ฑ์ค ๊ฐ ๋ฆฌํด ํ ์ญ์ 
for number in numbers:
	print(number) # 10, 20, 30, 50
```


**_"Java"_**

- ์๋ฐ๋ ๋ฐฐ์ด๊ณผ ๋ฆฌ์คํธ๋ฅผ ๋ชจ๋ ์ง์ํ๊ณ , ๋ ๊ฐ์ง๊ฐ ์์ ํ ๋ถ๋ฆฌ๋์ด ์๋ค.
- **๋ฐฐ์ด์ ๋ฐฐ์ด์ ์ฅ์ ์ด, ๋ฆฌ์คํธ๋ ๋ฆฌ์คํธ์ ์ฅ์ ์ด ์๊ธฐ ๋๋ฌธ์ ๊ฐ๋ฐ์๊ฐ ์ํ๋๋๋ก ์ง์  ์ ํ๊ฐ๋ฅ**ํ๋ค.
- java๋ javascript, python์ ๋นํด์ ์๋ฃ๊ตฌ์กฐ์ ๋ํด ๋ ์์์ผ ํ  ํ์์ฑ์ด ์์ง๋ง, ๊ทธ๋งํผ ๊ฐ๋ฐ์์๊ฒ ๋ ํฐ ์์ ๋๊ฐ ์ฃผ์ด์ง๋ค.
- ์๋ฐ๋ 2๊ฐ์ง ํํ์ ๋ฆฌ์คํธ๋ฅผ ์ง์ํ๋ค.
	- LinkedList / ArrayList
	- ๋๊ฐ์ ๊ธฐ๋ฅ(๋ฉ์๋)๋ฅผ ๊ฐ์ง ๋ฆฌ์คํธ๊ฐ 2๊ฐ์ง ์กด์ฌํ๋ค.
	- ๊ฐ๊ฐ์ ์ฅ๋จ์ ์ด ๋ถ๋ชํ๋ค.

```java
// ๋ฐฐ์ด - ์ถ๊ฐ, ์ญ์ ๊ฐ ์ด๋ ต๋ค. ์ง์  ๊ตฌํํด์ผํ๋ค.
int[] numbers = {10,20,30,40,50};

// ๋ฆฌ์คํธ (ArrayList)
ArrayList numbers = new ArrayList();

numbers.add(10); // ์ถ๊ฐ
numbers.remove(0); // ์ญ์ 

// ๋ฆฌ์คํธ (LinkedList)
LinkedList numbers = new LinkedList();

numbers.add(10); // ์ถ๊ฐ
numbers.remove(0); // ์ญ์ 
```

<div class="notice--primary" markdown="1">
๐ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u>Java - ArrayList / LinkedList</u></strong>   

- Java์์๋ ๋ฐฐ์ด (array) ์ด์ธ์ ArrayList์ LinkedList 2์ข๋ฅ์ ๋ฆฌ์คํธ๋ฅผ ์ ๊ณตํ๋ค.     

- <strong>์ธ๋ฑ์ค๋ฅผ ์ด์ฉํด์ ๋ฐ์ดํฐ๋ฅผ ๊ฐ์ ธ์ค๋ ๊ฒ์ด ๋น๋ฒํ๋ค๋ฉด ๋ด๋ถ์ ์ผ๋ก ๋ฐฐ์ด์ ์ด์ฉํ๋ ArrayList๊ฐ ํจ์ฌ ๋น ๋ฅด๋ค. ํ์ง๋ง ๋ฐ์ดํฐ์ ์ถ๊ฐ/์ญ์ ๊ฐ ๋น๋ฒํ๋ค๋ฉด LinkedList๊ฐ ํจ์ฌ ํจ๊ณผ์ ์ด๋ค.</strong>    

- ์ด์๊ฐ์ด ์ฒ๋ฆฌํ๊ณ ์ ํ๋ ๋ฐ์ดํฐ์ ๋ฐ๋ผ์ ์ด๋ค ๋ฐ์ดํฐ ์คํธ๋ญ์ณ๋ฅผ ์ ํํ ์ง๋ฅผ ์ ํ๋จํ๋ ๊ฒ์ ๋๊ท๋ชจ ์์คํ์ ๊ตฌ์ถํ๋๋ฐ๋ ํ์์ ์ธ ๋ฅ๋ ฅ์ด๋ค.    

- ์ด๋ฌํ ํ๋จ์ ํ๊ธฐ ์ํด์๋ ์ง์  Data structure๋ฅผ ๊ตฌํํด์ ์ฌ์ฉํ์ง ์๋๋ผ๋ ๋ด๋ถ์ ์ธ ๋ฉ์ปค๋์ฆ์ ์ดํดํ  ํ์๊ฐ ์๋ค.    

<img width="634" alt="Screen Shot 2022-01-05 at 5 02 04 PM" src="https://user-images.githubusercontent.com/63195670/148181935-e6b7f444-bc24-49a0-812c-8b1b9d49f54c.png">    

๐น Array List

Array List๋ ๋ฐฐ์ด์ ์ด์ฉํด์ ๋ฆฌ์คํธ๋ฅผ ๊ตฌํํ ๊ฒ์ ์๋ฏธํ๋ค.    
- ์ฅ์  : ๋ด๋ถ์ ์ผ๋ก ๋ฐฐ์ด์ ์ฌ์ฉํ๊ธฐ ๋๋ฌธ์ ์ธ๋ฑ์ค๋ฅผ ์ด์ฉํด์ ์ ๊ทผํ๋ ๊ฒ์ด ๋น ๋ฅด๋ค.   
- ๋จ์  : ๋ฐ์ดํฐ์ ์ถ๊ฐ์ ์ญ์ ๊ฐ ๋๋ฆฌ๋ค.     

- ๋ฐ์ดํฐ์ ์ถ๊ฐ : Array List๋ ๋ด๋ถ์ ์ผ๋ก ๋ฐ์ดํฐ๋ฅผ ๋ฐฐ์ด์ ์ ์ฅํ๋ค. ๋ฐฐ์ด์ ํน์ฑ์ ๋ฐ์ดํฐ๋ฅผ ๋ฆฌ์คํธ์ ์ฒ์์ด๋ ์ค๊ฐ์ ์ ์ฅํ๋ฉด, ์ดํ์ ๋ฐ์ดํฐ๋ค์ด ํ์นธ์ฉ ๋ค๋ก ๋ฌผ๋ฌ๋์ผํ๋ค.    

- ๋ฐ์ดํฐ์ ์ญ์  : ์ญ์ ๋ ์ถ๊ฐ์ ์ ์ฌํ๊ฒ ๋น์๋ฆฌ๊ฐ ์๊ธฐ๋ฉด ๋น์๋ฆฌ๋ฅผ ์ฑ์ฐ๊ธฐ ์ํด์ ์์ฐจ์ ์ผ๋ก ํ์นธ์ฉ ๋ก๊ฒจ์ผ ํ๋ค.    

- ๋ฐ์ดํฐ ์กฐํ(๊ฐ์ ธ์ค๊ธฐ) : ์ธ๋ฑ์ค๋ฅผ ์ด์ฉํ์ฌ ๋ฐ์ดํฐ๋ฅผ ๊ฐ์ ธ์ค๊ณ  ์ถ์ ๋ Array๋ก ๊ตฌํํ ๋ฆฌ์คํธ๋ ์๋๊ฐ ๋งค์ฐ ๋น ๋ฅด๋ค. (๋ฉ๋ชจ๋ฆฌ ์์ ์ฃผ์๋ฅผ ์ ํํ๊ฒ ์ฐธ๊ณ ํด์ ๊ฐ์ ธ์ค๊ธฐ ๋๋ฌธ์ด๋ค.).   

๐น Linked List

Linked List๋ ๋ธ๋์ ์ฐ๊ฒฐ์ ์ด์ฉํด์ ๋ฆฌ์คํธ๋ฅผ ๊ตฌํํ ๊ฒ์ ์๋ฏธํ๋ค.    
- ์ฅ์  : ๋ฐ์ดํฐ์ ์ถ๊ฐ์ ์ญ์  ์๋๊ฐ ๋น ๋ฅด๋ค.   
- ๋จ์  : ์ธ๋ฑ์ค๋ฅผ ์ด์ฉํด์ ์ ๊ทผํ๋ ๊ฒ์ด Array List์ ๋นํด ์๋์ ์ผ๋ก ๋๋ฆฌ๋ค.     

- ๋ฐ์ดํฐ์ ์ถ๊ฐ : ์ถ๊ฐ๋  ์๋ฆฌ๋จผํธ์ ์ด์ , ์ดํ ๋ธ๋์ ์ฐธ์กฐ๊ฐ(next)๋ง ๋ณ๊ฒฝํ๋ฉด ๋๊ธฐ ๋๋ฌธ์ ๋น ๋ฅด๋ค   

- ๋ฐ์ดํฐ์ ์ญ์  : ์ญ์ ๊ฐ ๋  ์๋ฆฌ๋จผํธ์ ์ด์ , ์ดํ ๋ธ๋์ ์ฐธ์กฐ๊ฐ(next)๋ง ๋ณ๊ฒฝํ๋ฉด ๋๊ธฐ ๋๋ฌธ์ ๋น ๋ฅด๋ค.    

- ๋ฐ์ดํฐ ์กฐํ(๊ฐ์ ธ์ค๊ธฐ) : ์ธ๋ฑ์ค๋ฅผ ์ด์ฉํด์ ๋ฐ์ดํฐ๋ฅผ ์กฐํํ  ๋ linked list๋ head๊ฐ ๊ฐ๋ฆฌํค๋ ๋ธ๋๋ถํฐ ์์ํด์ ์์ฐจ์ ์ผ๋ก ๋ธ๋๋ฅผ ์ฐพ์๊ฐ๋ ๊ณผ์ ์ ๊ฑฐ์ณ์ผ ํ๋ค. ๋ง์ฝ ์ฐพ๊ณ ์ ํ๋ ์๋ฆฌ๋จผํธ๊ฐ ๊ฐ์ฅ ๋์ ์๋ค๋ฉด ๋ชจ๋  ๋ธ๋๋ฅผ ํ์ํด์ผ ํ๊ธฐ์ Array List์ ๋นํด ๋๋ฆฌ๋ค.

</div>


### [2] Linked list

Linked List๋ Array List์๋ ๋ค๋ฅด๊ฒ ์๋ฆฌ๋จผํธ์ ์๋ฆฌ๋จผํธ ๊ฐ์ ์ฐ๊ฒฐ(link)์ ์ด์ฉํด์ ๋ฆฌ์คํธ๋ฅผ ๊ตฌํํ ๊ฒ์ ์๋ฏธํ๋ค. Linked list์์ ๊ฐ์ฅ ์ค์ํ ๊ฒ์ ์ฐ๊ฒฐ์ด ๋ฌด์์ธ๊ฐ๋ฅผ ํ์ํ๋ ๊ฒ๊ณผ ๋ ์ฐ๊ฒฐ์ด ์๋ ๊ฒ์ ๋ฌด์์ธ๊ฐ๋ฅผ ์๊ฐํด๋ณด๋ ๊ฒ์ด๋ผ๊ณ  ํ  ์ ์์.

<img width="275" alt="Screen Shot 2022-01-05 at 5 30 44 PM" src="https://user-images.githubusercontent.com/63195670/148185621-18d03000-1114-4e52-9699-c4e70e3b3c11.png">

๋ฐฐ์ด๊ณผ๋ ๋ค๋ฅด๊ฒ Linked list๋ ๋ฉ๋ชจ๋ฆฌ์ ๊ทธ ์์น๊ฐ ํฉ์ด์ ธ ์๊ธฐ ๋๋ฌธ์ ์๋ก ์ฐ๊ฒฐ๋์ด ์์ด์ผ ํ๋ค. ๋ฐ๋ก ๊ทธ๋ฐ ์ ์์ ์ฐ๊ฒฐ์ด๋ผ๋ ์ด๋ฆ์ ๊ฐ๊ฒ ๋ ๊ฒ! 

Array list์์๋ element๋ผ๋ ์ด๋ฆ์ ์ฌ์ฉํ์ง๋ง Linked list์ ๊ฐ์ด ์ฐ๊ฒฐ๋ ์๋ฆฌ๋จผํธ๋ค์ ๋ธ๋(node, ๋ง๋, ๊ต์ ์ ์๋ฏธ) ํน์ ๋ฒํ์ค(vertex, ์ ์ , ๊ผญ์ง์ ์ ์๋ฏธ)๋ผ๊ณ  ๋ถ๋ฅธ๋ค. ์ฐ๊ฒฐ์ฑ์ด ๊ฐ์กฐ๋ ํํ์ด๋ผ๊ณ  ์๊ฐํ๋ฉด ๋จ!

The linked list is that type of data structure where separate objects are stored sequentially. Every object stored in the data structure will have the data and a reference to the next object. The last node of the linked list has a reference to null. The first element of the linked list is known as the head of the list. There are many differences between a linked list to the other types of data structures. These are in terms of memory allocation, the internal structure of the data structure, and the operations carried on the linked list. 

Getting to an element in a linked list is a slower process compared to the arrays as the indexing in an array helps in locating the element. However, in the case of a linked list, the process has to start from the head and traverse through the whole structure until the desired element is reached. In contrast to this, the advantage of using linked lists is that the addition or deletion of elements at the beginning can be done very quickly. 

There are three types of linked lists:

#### โ๏ธ Single Linked List

This type of structure has **<u>the address or the reference of the next node</u>** stored in the current node. Therefore, a node which at the last has the address and reference as a NULL.  

๊ทธ๋ผ linked list์ ๊ตฌ์กฐ๋ฅผ ์์๋ณด์. ๋ฆฌ์คํธ๋ ๋ธ๋(์๋ฆฌ๋จผํธ)๋ค์ ๋ชจ์์ด๊ธฐ์ ๋ด๋ถ์ ์ผ๋ก ๋ธ๋๋ฅผ ๊ฐ์ง๊ณ  ์์ด์ผ ํ๋ค. array list์ ๊ฒฝ์ฐ ์๋ฆฌ๋จผํธ๊ฐ ๋ฐฐ์ด์ ์๋ฆฌ๋จผํธ์๋ ๋ฐ๋ฉด, linked list๋ ๋ฐฐ์ด ๋์ ์ ๋ค๋ฅธ ๊ตฌ์กฐ๋ฅผ ์ฌ์ฉํ๋ค.

๋ธ๋๋ <u>๋ธ๋์ ๊ฐ</u>๊ณผ <u>๋ค์ ๋ธ๋</u>๋ผ๋ ์ต์ํ ๋ ๊ฐ์ง ์ ๋ณด๋ฅผ ์๊ณ  ์์ด์ผ ํ๋ค. ๊ฐ๊ฐ์ ๋ธ๋๊ฐ ๋ค์ ๋ธ๋๋ฅผ ์๊ณ  ์๊ธฐ ๋๋ฌธ์ ํ๋์ ์ฐ๊ฒฐ๋ ๊ฐ์ ๋ชจ์์ ๋ง๋ค ์ ์๋ ๊ฒ์ด๋ค. ์๋ ๊ทธ๋ฆผ์ linked list์ ๊ตฌ์กฐ๋ฅผ ๋ณด์ฌ์ค๋ค.

<img width="651" alt="Screen Shot 2022-01-05 at 5 33 45 PM" src="https://user-images.githubusercontent.com/63195670/148185957-500d1c23-d225-45b1-8044-659328d28f05.png">   

์ด๊ฒ์ ๊ตฌํํ๋ ๋ฐฉ๋ฒ์ ์ฌ๋ฌ๊ฐ์ง๋ค. ๋ง์ฝ ์ฌ์ฉ ์ธ์ด๊ฐ C๋ผ๋ฉด ๊ตฌ์กฐ์ฒด, ์๋ฐ์ ๊ฐ์ ๊ฐ์ฒด์งํฅ ์ธ์ด๋ผ๋ฉด ๊ฐ์ฒด์ ๋ฐ์ดํฐ ํ๋์ ๋งํฌ ํ๋๋ฅผ ๋ง๋ ๋ค. ๋ณดํต **<u>๋ฐ์ดํฐ ํ๋</u>**๋ value๋ผ๋ ์ด๋ฆ์ ๋ณ์, **<u>๋งํฌ ํ๋</u>**๋ next ๋ณ์๋ฅผ ์ฌ์ฉํ๋๋ฐ, value์๋ **<u>๋ธ๋์ ๊ฐ</u>์ด ์ ์ฅ**๋๊ณ , next์๋ **<u>๋ค์ ๋ธ๋์ ํฌ์ธํฐ๋ ์ฐธ์กฐ๊ฐ</u>**์ ์ ์ฅํด์ ๋ธ๋์ ๋ธ๋๋ฅผ ์ฐ๊ฒฐ์ํค๋ ๋ฐฉ๋ฒ์ ์ฌ์ฉํจ!

##### ๐ Example
A->B->C->D->E->NULL

#### โ๏ธ A Double Linked List

As the name suggests, each node has two references associated with it. One reference directs to the previous node while the second reference points to the next node. Traversal is possible in both directions as reference is available for the previous nodes. Also, explicit access is not required for deletion. 

doubly linked list์ ํต์ฌ์ ๋ธ๋์ ๋ธ๋๊ฐ ์๋ก ์ฐ๊ฒฐ๋์ด ์๋ค๋ ์ ์ด๋ค. ์๋ ๊ทธ๋ฆผ์ ๋ณด๋ฉด ๋จ์ ์ฐ๊ฒฐ ๋ฆฌ์คํธ(linked list)์๋ ๋ค๋ฅด๊ฒ **<u>๋ธ๋๊ฐ ์ด์  ๋ธ๋(previous)์ ๋ค์ ๋ธ๋(next)๋ก ๊ตฌ์ฑ๋์ด ์๋ค</u>**๋ ๊ฒ์ ํ์ธํ  ์ ์๋ค.    

<img width="617" alt="Screen Shot 2022-01-07 at 9 55 06 AM" src="https://user-images.githubusercontent.com/63195670/148473920-b5a0cbbe-2df5-4888-815b-2654ed95a6f5.png">   

์ด๊ฒ์ ๊ฐ์ฅ ํฐ ์ฅ์ ์ ์๋ฐฉํฅ์ผ๋ก ์ฐ๊ฒฐ๋์ด ์๊ธฐ ๋๋ฌธ์ ๋ธ๋๋ฅผ ํ์ํ๋ ๋ฐฉํฅ์ด ์์ชฝ์ผ๋ก ๊ฐ๋ฅํ๋ค๋ ๊ฒ์ด๋ค.

##### ๐ ์ฅ์ 
์๋ฐฉํฅ ํ์์ ๊ฐ์ฅ ํฐ ์ฅ์ ์ <u>ํน์  ์ธ๋ฑ์ค ์์น์ ์๋ฆฌ๋จผํธ๋ฅผ ๊ฐ์ ธ์ฌ ๋</u>์ <u>๋ฐ๋ณต์๋ฅผ ์ด์ฉํด์ ํ์ํ  ๋</u> ๋๋ฌ๋๋ค.

**<u>์ธ๋ฑ์ค์ ๋ฐ์ดํฐ ๊ฐ์ ธ์ค๊ธฐ</u>**   
๋ธ๋๊ฐ 6๊ฐ์ผ ๋ 3๋ฒ์งธ ์๋ฆฌ๋จผํธ ์ด์ ์ ์ฒ์๋ถํฐ ์์ํด์ next๋ฅผ ์ด์ฉํด์ ํ์ํ๊ณ , 4๋ฒ์งธ ์ดํ์ ์๋ฆฌ๋จผํธ๋ ๋ง์ง๋ง ๋ธ๋๋ถํฐ previous๋ฅผ ์ด์ฉํด์ ์กฐํํ๋ค. ๋จ์ ์ฐ๊ฒฐ ๋ฆฌ์คํธ๊ฐ ์ต์์ ๊ฒฝ์ฐ ๋ธ๋ ์ ์ฒด๋ฅผ ํ์ํด์ผ ํ๋ ๊ฒ์ ๋นํด์ ์๋ฐฉํฅ ์ฐ๊ฒฐ ๋ฆฌ์คํธ๋ ํ์ํด์ผํ๋ ์๋ฆฌ๋จผํธ๊ฐ ๋ฐ์ผ๋ก ์ค์ด ๋ค๊ฒ ๋จ!     
์๋ ๊ทธ๋ฆผ์ ๋ณด๋ฉด ๋ ๋ชํํ ์ดํด๊ฐ ๊ฐ๋ฅํ  ๊ฒ์ด๋ค.    

<img width="516" alt="Screen Shot 2022-01-07 at 10 02 20 AM" src="https://user-images.githubusercontent.com/63195670/148474348-d96a1459-7a7a-4fbe-984e-21c6309e60de.png">    

**<u>๋ธ๋ ํ์ํ๊ธฐ</u>**   
๋จ๋ฐฉํฅ ์ฐ๊ฒฐ ๋ฆฌ์คํธ๋ ๋ค์ ๋ธ๋์ ํ์๋ง ๊ฐ๋ฅํ๋ ๊ฒ์ ๋นํด์ ์ด์ค ์ฐ๊ฒฐ ๋ฆฌ์คํธ์ ๊ฒฝ์ฐ ์๋ค๋ก ํ์์ด ๊ฐ๋ฅํ๋ค. ์ํฉ์ ๋ฐ๋ผ ํ์์ ๋ฐฉํฅ์ด ๋ฐ๋์ด์ผ ํ๋ ๊ฒฝ์ฐ๋ผ๋ฉด ์ด์ค ์ฐ๊ฒฐ ๋ฆฌ์คํธ๋ฅผ ์ฌ์ฉํ๋ ๊ฒ์ด ์ข์!      

<img width="509" alt="Screen Shot 2022-01-07 at 10 04 08 AM" src="https://user-images.githubusercontent.com/63195670/148474463-54e86461-f235-4982-94c9-5e1ae204aa7f.png">


##### ๐ ๋จ์ 

์ฐ์  ์ด์  ๋ธ๋๋ฅผ ์ง์ ํ๊ธฐ ์ํ ๋ณ์๋ฅผ ํ๋ ๋ ์ฌ์ฉํด์ผ ํ๊ธฐ์ ๋ฉ๋ชจ๋ฆฌ๋ฅผ ๋ ๋ง์ด ์ฌ์ฉํ๋ค๋ ์๋ฏธ์ด๋ค. ๋ ๊ตฌํ์ด ์กฐ๊ธ ๋ ๋ณต์กํด์ง๋ค๋ ๋จ์ ๋ ์๋ค. ํ์ง๋ง ์ฅ์ ์ด ํฌ๊ธฐ ๋๋ฌธ์ ํ์ค์์ ์ฌ์ฉํ๋ ์ฐ๊ฒฐ ๋ฆฌ์คํธ๋ ๋๋ถ๋ถ ์ด์ค ์ฐ๊ฒฐ ๋ฆฌ์คํธ์ด๋ค.  

##### ๐ Example
NULL<-A<->B<->C<->D<->E->NULL


#### โ๏ธ Linked List which is circular

The nodes in a circular linked list are connected in a way that a circle is formed. As the linked list is circular there is no end and hence no NULL. This type of linked list can follow the structure of both singly or doubly. There is no specific starting node and any node from the data can be the starting node. The reference of the last node points towards the first node.  

๋จ์ผ ์ฐ๊ฒฐ๋ฆฌ์คํธ์๋ ๋ค๋ฅด๊ฒ ๋ง์ง๋ง ๋ธ๋๊ฐ ์ฒซ ๋ธ๋์ ์ฐ๊ฒฐ๋์ด ์๋ ๋ฆฌ์คํธ๋ก, ์ํ์ผ๋ก ์ฐ๊ฒฐ๋์ด ์๋ค๊ณ  ํ์ฌ ์ํ ์ฐ๊ฒฐ ๋ฆฌ์คํธ๋ผ ๋ถ๋ฅธ๋ค.

๋ฆฌ์คํธ๋ ๋ช๊ฐ์ ๋ธ๋๊ฐ ๋ค์ด ์๋์ง ์๊ธฐ ์ํ index๊ฐ๊ณผ ๋ธ๋๋ฅผ ํ์ํ  ๋ ๊ธฐ์ค ๋ธ๋๋ฅผ ํด์ฃผ๊ธฐ์ํ head์ tail๋ก ๋๋ ์ง๋ ๊ฑด ์ด๋ฏธ ๋ค ์ ๊ฒ์ด๋ค. (head๋ ๋จธ๋ฆฌ, ์ฆ ๋ฆฌ์คํธ์ ๋งจ ์์ ์๋ ๋ธ๋๋ฅผ ๊ฐ๋ฅดํค๋ ๊ฒ์ด๊ณ  tail์ ๊ผฌ๋ฆฌ ์ฆ, ๋งจ ๋ง์ง๋ง ๋ธ๋๋ฅผ ์ผ์ปซ๋ ๋ง)

์ํ linked list์์๋ head๋ฅผ ์ฌ์ฉํด๋ ๋์ง๋ง, **<u>tail์ ์ฌ์ฉํ๋ ๋ฐฉ๋ฒ์ด ์ข ๋ ๋์ ๋ฐฉ๋ฒ</u>**์ด๋ค.
์๋ํ๋ฉด tail์ ๊ธฐ์ค์ผ๋ก ์ก์ผ๋ฉด ์ฐ์  tail ๋ธ๋๋ฅผ ์ ์ ์๊ณ  tail ๋ธ๋์ ๋ค์ ๋ธ๋๋ head ๋ธ๋์ด๊ธฐ ๋๋ฌธ์ head์ tail์ ๋ ๋ค ์ ์ ์์!   

<img width="540" alt="Screen Shot 2022-01-07 at 10 18 22 AM" src="https://user-images.githubusercontent.com/63195670/148475538-14be1e4f-0d07-4474-8bb1-9590b79a91ef.png">



##### ๐ Example
A->B->C->D->E

#### โ๏ธ Properties of a linked list

- Access time: O(n) 
- Searching time: O(n)
- Adding element: O(1) 
- Deleting  an Element : O(1) 

### [3] Stack
The stack is another type of structure where the elements stored in the data structure follow the rule of LIFO (last in, first out) or FILO (First In Last Out). Two types of operations are associated with a stack i.e. push and pop. Push is used when an element has to be added to the collection and pop is used when the last element has to be removed from the collection. Extraction can be carried out for only the last added element.   

ํ ์ชฝ ๋์์๋ง ์๋ฃ๋ฅผ ๋ฃ๊ณ  ๋บ ์ ์๋, ๊ฐ์ฅ ์ต๊ทผ์ ์คํ์ ์ถ๊ฐํ ํญ๋ชฉ์ด ๊ฐ์ฅ ๋จผ์  ์ ๊ฑฐ๋๋ **<u>LIFO(Last In First Out)</u>** ํ์์ ์๋ฃ ๊ตฌ์กฐ์ด๋ค.    

<img width="298" alt="Screen Shot 2022-01-07 at 10 44 36 AM" src="https://user-images.githubusercontent.com/63195670/148477708-926b7366-cf4a-41b2-997e-9143b8824894.png">

#### โ๏ธ ์คํ(Stack)์ ์ฐ์ฐ

- **<u>pop()</u>** : ์คํ์์ ๊ฐ์ฅ ์์ ์๋ ํญ๋ชฉ์ ์ ๊ฑฐํ๋ค.
- **<u>push(item)</u>** : item ํ๋๋ฅผ ์คํ์ ๊ฐ์ฅ ์ ๋ถ๋ถ์ ์ถ๊ฐํ๋ค.
- **<u>peek()(top())</u>** : ์คํ์ ๊ฐ์ฅ ์์ ์๋ ํญ๋ชฉ์ ๋ฐํํ๋ค.
- **<u>isEmpty()</u>** : ์คํ์ด ๋น์ด ์์ ๋์ true๋ฅผ ๋ฐํํ๋ค.

#### โ๏ธ Properties of a stack are:

- Adding element: O(1)
- deleting element:  O(1)
- Accessing Time: O(n) [Worst Case]

Only one end allows inserting and deleting an element.
Examples of the stack include the removal or recursion. In scenarios where a word has to be reversed, or while using editors when the word that was last typed will be removed first (using an undo operation), stacks are used.  

์ฌ๊ท ์๊ณ ๋ฆฌ์ฆ์ ์ฌ์ฉํ๋ ๊ฒฝ์ฐ ์คํ์ด ์ ์ฉํ๋ค.  
๋ค์์ ์คํ์ ์ฌ์ฉ ์ฌ๋ก๋ค!

- ์ฌ๊ท ์๊ณ ๋ฆฌ์ฆ
	- ์ฌ๊ท์ ์ผ๋ก ํจ์๋ฅผ ํธ์ถํด์ผ ํ๋ ๊ฒฝ์ฐ์ ์์ ๋ฐ์ดํฐ๋ฅผ ์คํ์ ๋ฃ์ด์ค๋ค.
	- ์ฌ๊ทํจ์๋ฅผ ๋น ์ ธ ๋์ ํด๊ฐ ๊ฒ์(backtrack)์ ํ  ๋๋ ์คํ์ ๋ฃ์ด ๋์๋ ์์ ๋ฐ์ดํฐ๋ฅผ ๋นผ ์ค์ผ ํ๋ค.
	- ์คํ์ ์ด๋ฐ ์ผ๋ จ์ ํ์๋ฅผ ์ง๊ด์ ์ผ๋ก ๊ฐ๋ฅํ๊ฒ ํด ์ค๋ค.
	- ๋ํ ์คํ์ ์ฌ๊ท ์๊ณ ๋ฆฌ์ฆ์ ๋ฐ๋ณต์  ํํ(iterative)๋ฅผ ํตํด์ ๊ตฌํํ  ์ ์๊ฒ ํด์ค๋ค.
- ์น ๋ธ๋ผ์ฐ์  ๋ฐฉ๋ฌธ๊ธฐ๋ก (๋ค๋ก๊ฐ๊ธฐ)
- ์คํ ์ทจ์ (undo)
- ์ญ์ ๋ฌธ์์ด ๋ง๋ค๊ธฐ
- ์์์ ๊ดํธ ๊ฒ์ฌ (์ฐ์ฐ์ ์ฐ์ ์์ ํํ์ ์ํ ๊ดํธ ๊ฒ์ฌ)
	- Ex) ์ฌ๋ฐ๋ฅธ ๊ดํธ ๋ฌธ์์ด(VPS, Valid Parenthesis String) ํ๋จํ๊ธฐ
- ํ์ ํ๊ธฐ๋ฒ ๊ณ์ฐ


๋ฌธ์ ์ ์ข๋ฅ์ ๋ฐ๋ผ ๋ฐฐ์ด๋ณด๋ค ์คํ์ ๋ฐ์ดํฐ๋ฅผ ์ ์ฅํ๋ ๊ฒ์ด ๋ ์ ํฉํ ๋ฐฉ๋ฒ์ผ ์ ์์.

- ๋ฐฐ์ด๊ณผ ๋ฌ๋ฆฌ ์คํ์ ์์ ์๊ฐ์ i๋ฒ์งธ ํญ๋ชฉ์ ์ ๊ทผํ  ์ ์๋ค.
- ํ์ง๋ง **<u>์คํ์์ ๋ฐ์ดํฐ๋ฅผ ์ถ๊ฐํ๊ฑฐ๋ ์ญ์ ํ๋ ์ฐ์ฐ์ ์์ ์๊ฐ์ ๊ฐ๋ฅ</u>**ํ๋ค.
- ๋ฐฐ์ด์ฒ๋ผ ์์๋ค์ ํ๋์ฉ ์์ผ๋ก ๋ฐ์ด ์ค ํ์๊ฐ ์๋ค.

### [4] Queue
Queue is the type of data structure where the elements to be stored follow the rule of First In First Out (FIFO). The particular order is followed for performing the required operations over the elements. The difference of a queue from that of a stack lies in the removal of an element, where the most recently added object is removed first in a stack. Whereas, in the case of a queue, the element that was added first is removed first.

Both the end of the data structure is used for the insertion and the removal of data. The two main operations governing the structure of the queue are enqueue, and dequeue. Enqueue refers to the process where inserting an element is allowed to the collection of data and dequeue refers to the process where removal of elements is allowed, which is the first element in the queue in this case.   

์ปดํจํฐ์ ๊ธฐ๋ณธ์ ์ธ ์๋ฃ ๊ตฌ์กฐ์ ํ๊ฐ์ง๋ก, ๋จผ์  ์ง์ด ๋ฃ์ ๋ฐ์ดํฐ๊ฐ ๋จผ์  ๋์ค๋ FIFO(First In First Out)๊ตฌ์กฐ๋ก ์ ์ฅํ๋ ํ์์ด๋ค.    

<img width="364" alt="Screen Shot 2022-01-07 at 10 45 57 AM" src="https://user-images.githubusercontent.com/63195670/148477809-6a5f9920-c729-4c8d-b7d5-1ca814f68830.png">

#### โ๏ธ ํ(Queue)์ ์ฐ์ฐ

- **<u>add(item)</u>** : item์ ๋ฆฌ์คํธ์ ๋๋ถ๋ถ์ ์ถ๊ฐํ๋ค.
- **<u>remove()</u>** : ๋ฆฌ์คํธ์ ์ฒซ ๋ฒ์งธ ํญ๋ชฉ์ ์ ๊ฑฐํ๋ค.
- **<u>peek()(top())</u>** : ํ์์ ๊ฐ์ฅ ์์ ์๋ ํญ๋ชฉ์ ๋ฐํํ๋ค.
- **<u>isEmpty()</u>** : ํ๊ฐ ๋น์ด ์์ ๋์ true๋ฅผ ๋ฐํํ๋ค.

#### โ๏ธ Properties of a queue are

- Inserting an element: O(1)
- Deleting an element: O(1)
- Accessing Time: O(n)

Example of the queue: Similar to those queues made while waiting for the bus or anywhere, the data structure too follows the same pattern. We can imagine a person waiting for the bus and standing at the first position as the person that came to the queue first. This person will be the first one who will get onto a bus, i.e. exit the queue. Queues are applied when multiple users are sharing the same resources and they have to be served on the basis of who has come first on the server. 

๋ฐ์ดํฐ๊ฐ ์๋ ฅ๋ ์๊ฐ ์์๋๋ก ์ฒ๋ฆฌํด์ผ ํ  ํ์๊ฐ ์๋ ์ํฉ์ ์ด์ฉํ๋ค.  
๋ค์์ ํ์ ์ฌ์ฉ ์ฌ๋ก๋ค์ ๊ฐ์ ธ์๋ค.

- ๋๋น ์ฐ์  ํ์(BFS, Breadth-First Search) ๊ตฌํ โ ๋์ค์ ๋ค์ ๋ค๋ค๋ณด๊ธฐ! 
	- ์ฒ๋ฆฌํด์ผ ํ  ๋ธ๋์ ๋ฆฌ์คํธ๋ฅผ ์ ์ฅํ๋ ์ฉ๋๋ก ํ(Queue)๋ฅผ ์ฌ์ฉํ๋ค.
	- ๋ธ๋๋ฅผ ํ๋ ์ฒ๋ฆฌํ  ๋๋ง๋ค ํด๋น ๋ธ๋์ ์ธ์ ํ ๋ธ๋๋ค์ ํ์ ๋ค์ ์ ์ฅํ๋ค.
	- ๋ธ๋๋ฅผ ์ ๊ทผํ ์์๋๋ก ์ฒ๋ฆฌํ  ์ ์๋ค.
- ์บ์(Cache) ๊ตฌํ
- ์ฐ์ ์์๊ฐ ๊ฐ์ ์์ ์์ฝ (์ธ์ ๋๊ธฐ์ด)
- ์ ์์ ์ถ์ด ํ์ํ ๋๊ธฐ์ด (ํฐ์ผ ์นด์ดํฐ)
- ์ฝ์ผํฐ ๊ณ ๊ฐ ๋๊ธฐ์๊ฐ
- ํ๋ฆฐํฐ์ ์ถ๋ ฅ ์ฒ๋ฆฌ
- ์๋ ์์คํ์ ๋ฉ์์ง ์ฒ๋ฆฌ๊ธฐ
- ํ๋ก์ธ์ค ๊ด๋ฆฌ

### [5] Hash Table

์๋ Hash Table ์ ๋ฆฌ ๋งํฌ๋ฅผ ์ฐธ๊ณ ํ์.

[Hash Table ์ ๋ฆฌ ๋งํฌ](https://swiftie1230.github.io/algorithm_study/์๊ณ ๋ฆฌ์ฆํ์ฉ-HASH-TABLE-์ ๋ฆฌ/)

<div class="notice--primary" markdown="1">
๐ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u>What is the difference between linear and non-linear data structures?</u></strong>   

The following illustrates the significant differences between the linear and non-linear data structures:   

๐น <strong><u>Linear Data Structure</u></strong>  
1. In linear data structures, each element is linearly connected to each other having reference to the next and previous elements.  
2. Implementation is quite easy as only a single level is involved.   
3. Wastage of memory is much more common in linear data structures.   
4. Stacks, Queues, Arrays, and Linked lists are all examples of linear data structures.   

๐น <strong><u>Non-Linear Data Structure</u></strong>   
1. In non-linear data structures, the elements are connected in a hierarchical manner.   
2. Implementation is much more complex as multiple levels are involved.   
3. Memory is consumed wisely and there is almost no wastage of memory.   
4. Graphs and trees are examples of non-linear data structures.   
</div>

<div class="notice--primary" markdown="1">
๐ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u>In what ways are linked lists more efficient than arrays?</u></strong>   

The following points elaborate the ways in which linked lists are much more efficient than arrays:   

๐น <strong><u>Dynamic Memory allocation</u></strong>   
The memory of a linked list is dynamically located which means that there is no need to initialize the size and it can be expanded as well as shrink anytime without implying any exterior operation.   
On the other hand, arrays are statically allocated and the size has to be initialized. Once created, the size cannot be altered.   

๐น <strong><u>Insertion and Deletion</u></strong>    
Since a linked list is dynamically created, operations like insertion and deletion are much more convenient.   

๐น <strong><u>No memory wastage</u></strong>    
There is no memory wastage in a linked list as all the elements are dynamically inserted. And after the deletion of an element, we can free its memory.    
</div>

<div class="notice--primary" markdown="1">
๐ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u>What are the most common operations performed in linear data structures?</u></strong>   

The common possible operations that can be performed in all linear data structures include traversing, insertion, deletion, modification, search operation, and sort operation.    
These operations are recognized by different names in different data structures. For example, the insertion and deletion operations are known as Push and Pop operations in Stack, whereas they are referred to as enqueue and dequeue operations in Queue.     
There can be some other operations as well such as merging and the empty operation to check if the data structure is empty or not.    
</div>

๋ค์์ผ๋ก๋ Non-linear data structures๋ฅผ ์ ๋ฆฌํ ๊ฒ์๋ฌผ์ ๊ฐ์ ธ์ ๋ด์ผ์งใฐ๏ธ๐
	
	
### ๐ ์ถ์ฒ	
* [Data Structure ์ฐธ๊ณ  ์ฌ์ดํธ](https://velog.io/@k904808/Data-Structure์๋ฃ๊ตฌ์กฐ)
* [๋ฐฐ์ด๊ณผ ๋ฆฌ์คํธ ์ฐธ๊ณ  ์ฌ์ดํธ 1](https://wayhome25.github.io/cs/2017/04/17/cs-18-1/)     
* [๋ฐฐ์ด๊ณผ ๋ฆฌ์คํธ ์ฐธ๊ณ  ์ฌ์ดํธ 2](https://opentutorials.org/module/1335/8636)
* [Linear Data Structure ์ฐธ๊ณ  ์ฌ์ดํธ](https://www.upgrad.com/blog/what-is-linear-data-structure/)
* [๋งํฌ๋ ๋ฆฌ์คํธ ์ฐธ๊ณ  ์ฌ์ดํธ](https://opentutorials.org/module/1335/8821)
* [๋๋ธ๋ฆฌ ๋งํฌ๋ ๋ฆฌ์คํธ ์ฐธ๊ณ  ์ฌ์ดํธ](https://opentutorials.org/module/1335/8940)
* [์ํ ๋งํฌ๋ ๋ฆฌ์คํธ ์ฐธ๊ณ  ์ฌ์ดํธ](https://supark7.tistory.com/entry/์ํ-์ฐ๊ฒฐ-๋ฆฌ์คํธ-Circular-Linked-List)
* [์คํ ์ฐธ๊ณ  ์ฌ์ดํธ](https://gmlwjd9405.github.io/2018/08/03/data-structure-stack.html)
* [ํ ์ฐธ๊ณ  ์ฌ์ดํธ](https://gmlwjd9405.github.io/2018/08/02/data-structure-queue.html)
