# π DFS

2μ£Όμ°¨μλ DFSμ λν΄ λ°°μ λλ°, μ§μ  λνμ μΈ λ¬Έμ  νλλ₯Ό νμ΄μ£Όμλ©° μ€λͺν΄μ£Όμ¨λ€!    

μ°μ  μ£Όλ‘ μ¬μ©λλ κ²½μ°λ₯Ό λλμ΄ λ§μν΄ μ£Όμ¨λλ°..λ¬Έμ  νκ±°λ νλ¨ν  λ μ μ©ν  κ² κ°μ μ¬κΈ°μ μ μ΄λκΈ°β°     

<div class="notice--primary" markdown="1">
π <strong><u>Important!</u> : <u>DFS & BFS</u></strong>

- <strong><u>DFS μ£Όλ‘</u> μ¬μ©ν  λ</strong> (μ ννλ reason) : <strong>visit entire graph</strong> (κ·Έλνμμ κ° μ μλ λͺ¨λ  λΈλλ₯Ό κ°κ³ (λ€λ¬ λ³΄κ³ ) μΆμ λ)     

- <strong><u>BFS μ£Όλ‘</u> μ¬μ©ν  λ</strong> (μ ννλ reason) : <strong>Shortest path</strong> (νΉμ  λΈλμμ λ€λ₯Έ λΈλ μ¬μ΄μ μ΅λ¨κ±°λ¦¬λ₯Ό μ°Ύμ λ, λͺ¨λ  λΈλλ€μ λ€λ₯Ό νμ μμ, λͺ©νκ° μ ν΄μ Έ μλ€!)  

</div> 

## κ·Έλν νμμ΄λ ?

- νλμ μ μ μΌλ‘λΆν° μμνμ¬ μ°¨λ‘λλ‘ λͺ¨λ  μ μ λ€μ ν λ²μ© λ°©λ¬Ένλ κ²

	- Ex) νΉμ  λμμμ λ€λ₯Έ λμλ‘ κ° μ μλμ§ μλμ§, μ μ νλ‘μμ νΉμ  λ¨μμ λ¨μκ° μλ‘ μ°κ²°λμ΄ μλμ§

## κΉμ΄ μ°μ  νμ(DFS, Depth-First Search)

### κΉμ΄ μ°μ  νμμ΄λ ?

**λ£¨νΈ λΈλ(νΉμ λ€λ₯Έ μμμ λΈλ)μμ μμν΄μ λ€μ λΆκΈ°(branch)λ‘ λμ΄κ°κΈ° μ μ <u>ν΄λΉ λΆκΈ°λ₯Ό μλ²½νκ² νμ</u>νλ λ°©λ²**

- λ―Έλ‘λ₯Ό νμν  λ ν λ°©ν₯μΌλ‘ κ° μ μμ λκΉμ§ κ³μ κ°λ€κ° λ μ΄μ κ° μ μκ² λλ©΄ λ€μ κ°μ₯ κ°κΉμ΄ κ°λ¦ΌκΈΈλ‘ λμμμ μ΄κ³³μΌλ‘λΆν° λ€λ₯Έ λ°©ν₯μΌλ‘ λ€μ νμμ μ§ννλ λ°©λ²κ³Ό μ μ¬νλ€.

- μ¦, **λκ²(wide) νμνκΈ° μ μ <u>κΉκ²(deep) νμ</u>νλ κ²**μ΄λ€.

- μ¬μ©νλ κ²½μ°: **<u>λͺ¨λ  λΈλλ₯Ό λ°©λ¬Έ(visit entire graph)</u>**νκ³ μ νλ κ²½μ°μ μ΄ λ°©λ²μ μ ννλ€.

- κΉμ΄ μ°μ  νμ(DFS)μ΄ λλΉ μ°μ  νμ(BFS)λ³΄λ€ μ’ λ κ°λ¨νλ€.

- **λ¨μ κ²μ μλ μμ²΄λ λλΉ μ°μ  νμ(BFS)μ λΉν΄μ λλ¦¬λ€**.    


### κΉμ΄ μ°μ  νμ(DFS)μ νΉμ§

- μκΈ° μμ μ νΈμΆνλ **μν μκ³ λ¦¬μ¦μ νν**λ₯Ό κ°μ§κ³  μλ€.

- μ μ μν(Pre-Order Traversals)λ₯Ό ν¬ν¨ν λ€λ₯Έ ννμ νΈλ¦¬ μνλ λͺ¨λ DFSμ ν μ’λ₯μ΄λ€.

- μ΄ μκ³ λ¦¬μ¦μ κ΅¬νν  λ κ°μ₯ ν° μ°¨μ΄μ μ, κ·Έλν νμμ κ²½μ° **<u>μ΄λ€ λΈλλ₯Ό λ°©λ¬Ένμλμ§ μ¬λΆ</u>λ₯Ό λ°λμ κ²μ¬ ν΄μΌ νλ€λ κ²**μ΄λ€.
	- μ΄λ₯Ό κ²μ¬νμ§ μμ κ²½μ° λ¬΄νλ£¨νμ λΉ μ§ μνμ΄ μλ€.

<div class="notice--primary" markdown="1">
ππ»ββοΈ <strong><u>μ¬κΈ°μ μ κΉ!</u> : <u>κ·Έλν κΉμ΄(Depth)</u></strong>

λ§μ½, κ΅¬ννλ €κ³  νλ μκ³ λ¦¬μ¦μ΄ νΈλ¦¬κ° μλ κ·Έλνλ₯Ό νμνκ² λλ€λ©΄ μ½κ°μ λ³νκ° νμνλ€. μ°μ μ μΌλ‘λ κ·Έλνμ κΉμ΄(depth)λ₯Ό κ²°μ ν  νμκ° μλ€.      
λ£¨νΈ λΈλ(κ°μ μ΅μμμ μμΉν λΈλ)μ κΉμ΄λ 0μΌλ‘ νλ©°, μμμ λΈλμ κΉμ΄λ μ΄μ 'λΆλͺ¨ μ€ κ°μ₯ κΉμ΄κ° μμ κ²'μ κΉμ΄μ '1'μ λν κ°μΌλ‘ μ μνλ€.        

</div> 


### κΉμ΄ μ°μ  νμ(DFS)μμμ κΉμ΄ μ νκ³Ό λ°±νΈλνΉ

**νμ κ³Όμ μ΄ μμ λΈλμμ νμμ΄ κΉμ΄ μ§νλλ κ²μ λ§κΈ° μν΄ κΉμ΄ μ ν(depth bound)λ₯Ό μ¬μ©νλ€.**      

κΉμ΄ μ νμ λλ¬ν  λκΉμ§ λͺ©νλΈλκ° λ°κ²¬λμ§ μμΌλ©΄ μ΅κ·Όμ μ²¨κ°λ λΈλμ λΆλͺ¨λΈλλ‘ λμμμ, λΆλͺ¨λΈλμμ μ΄μ κ³Όλ λ€λ₯Έ λμμλ₯Ό μ μ©νμ¬ μλ‘μ΄ μμλΈλλ₯Ό μμ±νλ€. μ¬κΈ°μ **λΆλͺ¨λΈλλ‘ λλμ μ€λ κ³Όμ **μ **<u>λ°±νΈλνΉ(backtracking)</u>**μ΄λΌκ³  νλ€.
	
### κΉμ΄ μ°μ  νμ(DFS)μ κ³Όμ 

![](https://media.vlpt.us/images/sohi_5/post/221b5009-1002-468c-a68a-415ef78c3cdf/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%206.37.06.png)     

μ μ¬μ§μ λΈλ 1μ μμμΌλ‘ μ°¨λ‘λλ‘ λΈλ 9κΉμ§ μννλ€. μ§νλλ λ°©ν₯μ λ³΄λ©΄ ν κ°μ§μ λκΉμ§ νμνκ³ , κ·Έ λ€μ κ°μ§λ₯Ό μμ°¨μ μΌλ‘ νμνλ€. μ μ²΄μ  μμμ μλλ‘ κΉκ² νμμ΄ μ§νλλ κ²μ λ³Ό μ μλ€.      

μ‘°κΈ λ ν΄λΉ νΈλ¦¬ννμ κ·Έλνμ κ³Όμ μ μμΈν μ€λͺν΄λ³΄κ² λ€!    

![](https://media.vlpt.us/images/sohi_5/post/fcbdab2d-9cc6-4bb9-8ec7-7bb28be3bf1c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.05.28.png)      

νΈλ¦¬μ λ£¨νΈ λΈλμΈ λΈλ 1μ κΈ°μ€μΌλ‘ νμμ μμνλ€. μ€ν λΈλ 1μ λ£μ ν, λΈλ 1κ³Ό μ°κ²°λ λΈλ μ€ λ°©λ¬Ένμ§ μμ λΈλκ° μλμ§ νμΈνλ€. μ΄? 2κ° μλ€.        

![](https://media.vlpt.us/images/sohi_5/post/19026fa3-779d-43db-95e6-2438c48496fd/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.09.37.png)        

λΈλ 2λ₯Ό μ€νμ λ£μ΄ μ€ ν, λμΌνκ² λΈλ 2μ μ°κ²°λ λΈλ μ€ λ°©λ¬Ένμ§ μμ λΈλκ° μλμ§ νμΈνλ€. μ­μ λΈλ 3μ λ°κ²¬ν  μ μμ.          

![](https://media.vlpt.us/images/sohi_5/post/ecaacfa5-eb94-4177-9f40-70f0f810c22c/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.13.17.png)     

μ΄μ  λΈλ 3μ μ€νμ λ£μ΄μ£Όκ³ , μ°κ²°λ λΈλ μ€ λ°©λ¬Ένμ§ μμ λΈλκ° μλμ§ νμΈ!    

![](https://media.vlpt.us/images/sohi_5/post/06c1ccf6-383f-4dda-a3ba-b1bd4d4c05af/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.15.53.png)      

But  λΈλ 3κ³Ό μ°κ²°λ λΈλλ λΈλ 2λΏμ΄λ©°, μ΄λ―Έ λ°©λ¬ΈνμΌλ―λ‘ μ΄λ² λΆκΈ°μ νμμ΄ μλ£λ κ²μ΄κΈ° λλ¬Έμ λΈλ 3μ μ€νμμ λΉΌλΈλ€.         
λ€μ, μ€νμ κ°μ₯ μμ μμΉν λΈλ 2μ μ°κ²°λ μμ§ λ°©λ¬Ένμ§ μμ λΈλκ° μλμ§ νμΈνλ€. κ·Έλ¬λ μ‘΄μ¬νμ§ μκΈ° λλ¬Έμ μ­μ λΈλ 2λ μ€νμμ λΉΌλ.      

![](https://media.vlpt.us/images/sohi_5/post/c53e8fd8-0c9a-4e2e-89c3-3b9cc7771b46/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.19.03.png)     

![](https://media.vlpt.us/images/sohi_5/post/209c03f6-77bd-4a35-ac8b-63d35ad7467f/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.23.03.png)    

μμ κ³Όμ μ κ³μ λ°λ³΅νμ. λΈλ 1κ³Ό μ°κ²°λ λΈλ μ€ λ°©λ¬Ένμ§ μμ λΈλ 4λ₯Ό μ€νμ μΆκ°νκ³ , λΈλ 4μ μ°κ²°λ λΈλ 5 , λΈλ 5μ μ°κ²°λ λΈλ 6 μ­μ λ€μ μ€νμ μΆκ°νλ€.     

λΈλ 6μ μ°κ²°λ λΈλλ₯Ό νμΈνλ€. λ°©λ¬Ένμ§ μμ λΈλκ° μμΌλ―λ‘ μ€νμμ μ κ±°νλ€. λΈλ 5λ λ§μ°¬κ°μ§λ‘ μ€νμμ μ κ±°νλ€.   

μ΄μ  λΈλ 4μ μ°κ²°λ λλ€λ₯Έ λΈλλ₯Ό νμΈνμ. 7μ΄ μκ΅°.      

![](https://media.vlpt.us/images/sohi_5/post/2d80c51f-03a6-46c1-ac88-8431e9ea00b8/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.25.14.png)         

λΈλ 7μ μ€νμ μΆκ°νλ€. But μ°κ²°λ λΈλ μ€ λ°©λ¬Ένμ§ μμ κ²μ΄ μμΌλ―λ‘ λ€μ μ€νμμ μ κ±°νκ³ , λΈλ 4 μ­μ λμΌν μ΄μ λ‘ μ€νμμ μ κ±°!       

![](https://media.vlpt.us/images/sohi_5/post/2d31b1d2-f0d0-4455-968c-53767b6f78d7/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.26.57.png)     

λΈλ 1κ³Ό μ°κ²°λ λ§μ§λ§ λΈλ 8μ μ€νμ μΆκ°νκ³ , λ€μ λΈλλ₯Ό νμνλ€. 9.     

![](https://media.vlpt.us/images/sohi_5/post/5226b43e-219f-4f29-a4fe-a30cb8f43d26/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.29.24.png)        

λΈλ 9λ₯Ό μ€νμ μΆκ°νλ€. λ°©λ¬Έν  λΈλκ° μμΌλ©°, λΈλ 8 λν λ§μ°¬κ°μ§μ΄λ―λ‘ μ€νμμ μ κ±°νλ€.       

![](https://media.vlpt.us/images/sohi_5/post/00d332f2-dc0d-4666-9c35-06d7364c03cd/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202020-04-21%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.30.47.png)       

μ΄μ  λ°©λ¬Ένμ§ μμ λΈλκ° λ μ΄μ μ‘΄μ¬νμ§ μμ§? κ·ΈλΌ λΈλ 1μ μ€νμμ μ κ±°ν΄ νμμ λ§μΉλ©΄ λλ€.      

### κΉμ΄ μ°μ  νμ(DFS)μ κ΅¬ν

- κ΅¬ν λ°©λ²  : μν νΈμΆκ³Ό λͺμμ μΈ μ€ν μ΄μ©     
	
	- μμ¬μ½λ (pseduocode)

		```python
		def dfs(Node root):
			# λ£¨νΈ λΈλ λ°©λ¬Έ
			if not root:
				return
			root.visited = True; # λ°©λ¬Έν λΈλλ₯Ό νμ
			# λ£¨νΈ λΈλμ μΈμ ν μ μ μ λͺ¨λ λ°©λ¬Έ
			for Node n in root.adjacent: 
				if n.visited == False: # λ°©λ¬Ένμ§ μμ μ μ μ μ°Ύλλ€.
					dfs(n) # λ£¨νΈ λΈλμ μΈμ ν μ μ μ μμμΌλ‘ DFS μμ
		```




### κΉμ΄ μ°μ  νμ(DFS)μ μκ° λ³΅μ‘λ

- DFSλ κ·Έλν(μ μ μ μ : N, κ°μ μ μ : E)μ λͺ¨λ  κ°μ μ μ‘°ννλ€.

	- μΈμ  λ¦¬μ€νΈλ‘ ννλ κ·Έλν : O(N+E)

	- μΈμ  νλ ¬λ‘ ννλ κ·Έλν : O(N^2)

- μ¦, **κ·Έλν λ΄μ μ μ μ«μμ κ°μ λ§μ κ°μ§λ <u>ν¬μ κ·Έλν(Sparse Graph)</u>**μ κ²½μ° **μΈμ  νλ ¬λ³΄λ€ <u>μΈμ  λ¦¬μ€νΈ</u>λ₯Ό μ¬μ©νλ κ²μ΄ μ λ¦¬**νλ€.     
	
<div class="notice--primary" markdown="1">
π <strong><u>μ¬κΈ°μ μ κΉ!</u> : <u>μΈμ  λ¦¬μ€νΈμ μΈμ  νλ ¬λ‘ ννλ κ·Έλνκ° λ­κ° λ¬λΌμ?</u></strong>    

μ¬μ€ μ λ§ λ³λ‘ μ΄λ ΅μ§ μμ κ°λμ΄λ€! μλ λ§ν¬ (μμ μ μ λ¦¬ν΄ λκ² μλλΌκ³ ..π) μ°Έκ³ ! π     

<strong><a href = "https://swiftie1230.github.io/algorithm_study/μκ³ λ¦¬μ¦νμ©-BFS&DFS-μ λ¦¬/">μκ³ λ¦¬μ¦νμ©-BFS&DFS-μ λ¦¬</a></strong>

</div> 

### κΉμ΄ μ°μ  νμ(DFS)μ μ₯μ κ³Ό λ¨μ 

1. μ₯μ 

	- λ¨μ§ ν κ²½λ‘μμ λΈλλ€λ§μ κΈ°μ΅νλ©΄ λλ―λ‘ **μ μ₯κ³΅κ°μ μμκ° λΉκ΅μ  μ λ€**.
	- λͺ©νλΈλκ° κΉμ λ¨κ³μ μμ κ²½μ° ν΄λ₯Ό λΉ¨λ¦¬ κ΅¬ν  μ μλ€.

2.  λ¨μ 

	- **ν΄κ° μλ κ²½λ‘μ κΉμ΄ λΉ μ§ κ°λ₯μ±**μ΄ μλ€. λ°λΌμ κΉμ΄μ νμ ν΅νμ¬ λͺ©νλΈλλ₯Ό λ°κ²¬νμ§ λͺ»νλ©΄ λ€μμ κ²½λ‘λ₯Ό λ°λΌ νμνλ λ°©λ²μ΄ μ μ©ν  μ μλ€.
	- **μ»μ΄μ§ ν΄κ° μ΅λ¨ κ²½λ‘κ° λλ€λ λ³΄μ₯μ΄ μλ€**. μ΄λ λͺ©νμ μ΄λ₯΄λ κ²½λ‘κ° λ€μμΈ λ¬Έμ μ λν΄ κΉμ΄μ°μ  νμμ ν΄μ λ€λ€λ₯΄λ©΄ νμμ λλ΄λ²λ¦¬λ―λ‘, μ΄ λ μ»μ΄μ§ ν΄λ μ΅μ μ ν΄κ° μλ μ μλ€λ μλ―Έμ΄λ€.

DFS μ λ¦¬λ μ¬κΈ°μ λ!    

μ΄μ  λ³Έκ²©μ μΌλ‘ μ κΈ°μΈμμμ νμλ λ¬Έμ λ₯Ό ν λ² λ³΄μ!    

## π Problem

### π¬ [Leetcode - Number of Islands](https://leetcode.com/problems/number-of-islands/) 

#### π λ¬Έμ  μ€λͺ  

Given an `m x n` 2D binary grid `grid` which represents a map of `'1'`s (land) and `'0'`s (water), return *the number of islands*.

An **island** is surrounded by water and is formed by connecting adjacent lands horizontally or vertically. You may assume all four edges of the grid are all surrounded by water.

#### βοΈ μ νμ¬ν­
- `m == grid.length`
- `n == grid[i].length`
- `1 <= m, n <= 300`
- `grid[i][j] is '0'` or `'1'`.

#### π­ μμΆλ ₯ μ

<div class="notice--primary" markdown="1">
π <u>μμΆλ ₯ μ #1</u>     

[μλ ₯]   

   ```python
grid = [
  ["1","1","1","1","0"],
  ["1","1","0","1","0"],
  ["1","1","0","0","0"],
  ["0","0","0","0","0"]
]
   ```             
      
    
[μΆλ ₯]    

   ```python    
1     
   ```
</div>   


<div class="notice--primary" markdown="1">
π <u>μμΆλ ₯ μ #2</u>     

[μλ ₯]   

   ```python
grid = [
  ["1","1","0","0","0"],
  ["1","1","0","0","0"],
  ["0","0","1","0","0"],
  ["0","0","0","1","1"]
]
   ```             
      
    
[μΆλ ₯]    

   ```python    
3 
   ```
   
</div>    

### βοΈ Final Code With Explaination

μμΈν μ€λͺμ μ£Όμμ μ°Έκ³ νμ.

```python  
class Solution(object):
    def numIslands(self, grid):
        # λ°νν  κ°
        result = 0
        
        # λͺ¨λ  matrixλ₯Ό λλ©΄μ μλ‘μ΄ island μ¬λΆ νμΈ 
        for i in range(len(grid)):
            for j in range(len(grid[0])):
                # ν΄λΉ κ°μ΄ 1λ‘, μλ‘μ΄ island κ°λ₯νλ€λ©΄ dfs_recursion μμ
                if grid[i][j] == "1":
                    self.dfs_recursion(grid, i, j)
                    # λͺ¨λ  recursion μ’λ£λλ©΄ νλμ island μ°Ύμ κ²μ΄λ―λ‘ resultμ 1 μΆκ°ν΄ μ€λ€.
                    result += 1
        
        return result
                                    
    # dfs recursion μ§νν  μΆκ° ν¨μ    
    def dfs_recursion(self, matrix, current_i, current_j):
        # edge case : recursionμ returnν  κ΅¬μ€μ΄ λλ μ‘°κ±΄λ€
        # matrix λ²μ λ°μ΄κ±°λ, ν΄λΉ κ°μ΄ 0μΌ λ
        if (current_i < 0 or current_i >= len(matrix) or current_j < 0 or current_j >= len(matrix[0]) or matrix[current_i][current_j] == "0"):
            return
        
        # markνκΈ° μν΄ ν΄λΉ κ°μ 0μΌλ‘ κ΅μ²΄
        matrix[current_i][current_j] = "0"
        
        direction = [[-1, 0], [0, 1], [1, 0], [0, -1]]
        
        # μλ κ³³ κΈ°μ€μΌλ‘ μμλ, μ€λ₯Έμͺ½, μΌμͺ½ λͺ¨λ recursion μ§ν
        for i in range(len(direction)):
            self.dfs_recursion(matrix, current_i - direction[i][0], current_j - direction[i][1])
```          


<div class="notice--primary" markdown="1">
π <strong><u>μ¬κΈ°μ μ κΉ!</u> : <u>λ€μ λ³΄λ©° ν·κ°λ Έκ±°λ μλ‘μ λ λ΄μ©</u></strong>        

 1. μΈμ  νλ ¬κ³Ό μΈμ  λ¦¬μ€νΈλ₯Ό μ¬μ©νλ λ°©λ²          
 2. Of course, DFS  

</div>
