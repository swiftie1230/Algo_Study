# โ๏ธ <u>Topological Sort</u> + <u>BFS</u>  



## ๐ Topological Sort

Topological Sort, BFS๊ฐ ์ ์ผ ๋ง์ด ์ฐ์ด๋ ๊ณณ๊ณผ, ๋ํ์ ์ผ๋ก ๋ง์ด ๋์ค๋ ๋ฌธ์  ์ ํ์ ์ผ๋จ **<u>๋คํธ์ํฌ</u>**!              

Tolpological Sort๋ฅผ ํ  ๋ ์ค์ํ ๊ฒ์ด ๋ช ๊ฐ์ง๊ฐ ์๋๋ฐ, ์ด์ ๋ํด์ ๋จผ์  ์์๋ณด์.    

1. It has to be a **<u>directed graph</u>**! : bi-directed graph์ ๋ํด์๋ topological sort๋ฅผ ์ ์ฉํ  ์๊ฐ ์์!     

2. **<u>adjacency matrix</u>** : topological sort๋ **<u>matrix</u> ํ์**์ผ๋ก ๋์ด ์์ด์ผ ํ๋ค.

๋ณดํต Topological Sort ๊ด๋ จ ๋ฌธ์ ๋ค์์๋ ์๋์ ๊ฐ์ ํํ์ `array`๋ก ๊ทธ๋ํ๊ฐ ์ฃผ์ด์ง๋ค.    

```python
[[from, to], [from, to], ....]
```

๊ทธ๋ฐ๋ฐ ์ด ์ํ๋ก๋, ์ด๊ฒ๋ง ๊ฐ์ง๊ณ ๋ ์ฐ๋ฆฌ๊ฐ ๊ทธ๋ํ ๋ฌธ์ ๋ฅผ ํ๊ธฐ๊ฐ ์ด๋ ค์ T^T     
๊ทธ๋ ๊ธฐ์ **์ฐ๋ฆฌ๊ฐ ์ํ๋ ๋ฐฉ์๋๋ก, ์ต๋ํ ์ฐ๋ฆฌ๊ฐ DFS๋ BFS๋ฅผ ๋๋ฆด ์ ์๊ฒ ๋ง๋ค์ด์ฃผ๋, ๊ณผ์ ์ ๊ฑฐ์ณ์ผ ํ๋๋ฐ, ์ด๊ฒ ๋ฐ๋ก Topological Sort**!     
๊ทธ๋ฆฌ๊ณ  ํด๋น ๊ณผ์ ์ ๊ฑฐ์น ํ, adjacency matrix๋ก ํํ์ด ๋์ผ ํ๋ ๊ฑฐ๊ฒ ์ง?         

์๋ฅผ ๋ค์ด ๋ค์ํ ๋คํธ์ํฌ ์๋ฒ๋ค์ ์ฐ๊ฒฐ๊ณผ ๊ฐ์ ๊ด๊ณ์ฑ์ ๋ํ๋ธ ๊ทธ๋ํ๊ฐ ์ฃผ์ด์ง๊ณ  `source`์ `destination`์ด ์์ ๋, **<u>Topological Sort</u>**๋ ๊ฐ ์ ์๋ ๋ฐฉ๋ฒ, ์ด๋ค ์์ผ๋ก ์์๋ฅผ ์ ํด์ผ ํ๋๋ ๋ฑ์ ๋ฌธ์ ์ ํ์ํ **"REARRANGE"**๋ฅผ ํ๋ ๊ฒ์ด๋ผ๊ณ  ํ  ์ ์๋ค.    



* * *



๊ทธ๋ผ ์ด์  ๋ณธ๊ฒฉ์ ์ผ๋ก Topological Sort์ BFS๋ฅผ ์ฌ์ฉํ๋ ์ค์  ๋ฌธ์ ๋ฅผ ์ ํด๋ณด์!   
์ค์ ๋ก ๊ฐ์ํด ์ฃผ์๋ฉฐ ์์๋ก ๋ค์ผ์จ๋ ๋ฌธ์ ์๋ค ๐    

## ๐ฌ Problem

### ๐ ๋ฌธ์  ์ค๋ช

<img width="457" alt="Screen Shot 2022-03-29 at 9 50 07 PM" src="https://user-images.githubusercontent.com/63195670/160614916-5edbd9b0-542c-425f-807a-b2e4f9b6a273.png">    

์ด ๊ทธ๋ํ๋ค์ ๋ชจ๋  `[from, to]` ๋ค์ด `2D array`๋ก ์ฃผ์ด์ก๋ค๊ณ  ๊ฐ์ ํด๋ณด์.    

์ด๋ ๊ฒ input์ด ์ฃผ์ด์ก์ ๋, ์ฒ์ ์๊ฐํด๋ด์ผ ํ  ๊ฑด ๋ฐ๋ก **<u>SOURCE</u>**๋ค. SOURCE์ ์ ํํ ๋ป์ **๋ค์ด์ค๋ ๊ฒ ์๋ค**๋ ๊ฑธ ์๋ฏธ!     
๋, ๋ฐ๋๋ก **๋๊ฐ๋ ๊ฒ ์๋ ๊ฒ**๋ค์ **<u>SINK</u>**๋ผ๊ณ  ํ๊ณ , ์ฌ๊ธฐ์๋ ์ด ๋์ ์ฐพ๋ ๊ฒ ์ค์ํ๋ค.      

๊ทธ๋ฐ ํ, SOURCE์์ SINK๊น์ง์ ๋ชจ๋  ๊ฒฝ๋ก๋ฅผ ์ฐพ์ ๋ DFS๋ฅผ ์ฌ์ฉํ๊ฑฐ๋, ๊ฐ์ฅ ๋น ๋ฅธ ๊ฒฝ๋ก๋ฅผ ์ฐพ์ ๋ BFS๋ฅผ ์ฌ์ฉํ๋ ๊ฒ!    

์ด ๋ฌธ์ ์์๋ ์ต๋จ ๊ฒฝ๋ก์ ๊ธธ์ด๋ฅผ ์ฐพ๊ธฐ ์ํด BFS๋ฅผ ์ฌ์ฉํด ์ฝ๋๋ฅผ ์์ฑํด ๋ณด์.     
ํด๊ฒฐํ๊ธฐ ์ํด ํด์ผ ํ  ์ผ์ ํฌ๊ฒ ์๋ ๋ ๋จ๊ณ๋ผ๋ ๊ฑด ์ด์  ์๊ฒ ์ง?    

1. **First Step : <u>Topological Sort</u>**
2. **Second Step : <u>BFS</u>**


<div class="notice--primary" markdown="1">
๐๐ปโโ๏ธ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u></strong>    

๊ทธ๋ฆฌ๊ณ  ์ฐธ๊ณ ๋ก ๋ง๋ถ์ด์๋ฉด, ์ด ์์ ์์๋ <code>airport๋ค</code>๋ก ๋ช์ํ์ง๋ง ์ด๋ฆ๋ง ๋ฐ๊พธ๋ฉด ๋ฐ๋ก ๋คํธ์ํฌ ๋ฌธ์ ๊ฐ ๋๋ ๊ฒ์ ํ์ธํ  ์ ์๋ค.   
์ด๋ฐ ๋ฌธ์ ๋ค ๋ค์ด๋ฒ, ์นด์นด์ค์์ ํ๋ ์ด์์ ๊ผญ ๋์จ๋ค๊ณ  ํ๋ ๊ผญ ์ ํํ๊ฒ, ์์ธํ ์ง๊ณ  ๋์ด๊ฐ์ ๐ฉ๐ปโ๐ป   
    
</div>


์ด์  ์ฝ๋๋ฅผ ์์ฑํด๋ณด์.        
์ผ๋จ input 2D array ๋จผ์ !        

```python
inputs = [['S', 'J'], ['S', 'I'], ['J', 'Mex'], ['J', 'Mor'], ['Mor', 'H'], ['Mor', 'Jap'], ['Mex', 'Jap'], ['Jap', 'E'], ['Jap', 'C'], ['Jap', 'F'], ['I', 'F']]
```

์ฐ๋ฆฌ๋ ์ด ๋ฌธ์ ๋ฅผ ํด๊ฒฐํ๊ธฐ ์ํด ๋ค ๊ฐ์ง ํจ์๋ฅผ ์์ฑํ  ๊ฒ์ด๋ค! `solution`, `topological_sort`, `BFS`, ๊ทธ๋ฆฌ๊ณ  `find_the_source`๊น์ง.          

**`solution`์ ์ฐ๋ฆฌ๊ฐ ๋ง ๊ทธ๋๋ก ์ด ๋ฌธ์ ๋ฅผ ์ํํ๊ธฐ ์ํด ์ฒ์ ๋ถ๋ฅด๋ ํจ์**. ์ผ๋ฐ ํ๋ก๊ทธ๋จ๋ค์ `main`ํจ์๋ผ๊ณ  ์๊ฐํ๋ฉด ์ดํดํ๊ธฐ ์ฌ์ธ ๊ฒ.        

**`topological_sort`์ `topological sort`์ ์ฌ์ฉํ์ฌ `input`์ผ๋ก ์ฃผ์ด์ง `2D array`๋ฅผ traversing ํ  ์ ์๋๋ก `dictionary(graph)`๋ก ๋ณํํ์ฌ ๋ฆฌํดํ๋ ํจ์**์ด๋ค.     

๋ค์์ผ๋ก **`find_the_source`๋ ๋ณํํ `dictionary`๋ฅผ ์ด์ฉํด "Source"๋ฅผ ์ฐพ์ ๋ฆฌํดํ๋ ํจ์**์ด๊ณ , **`BFS`๋ ์ํ์ ๋๋ ค ์ด ๋ฌธ์ ์์์ ๋ต, ์ฆ, ์ต๋จ ๊ฑฐ๋ฆฌ๋ฅผ ๋ฆฌํดํ๋ ํจ์**!      


<div class="notice--primary" markdown="1">
๐๐ปโโ๏ธ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u>์ ์ด๋ ๊ฒ ๊ตณ์ด ๋ง์ ํจ์๋ค์?</u></strong>    

<strong>์ฐ๋ฆฌ๊ฐ function์ด๋ผ๊ณ  ์ ํด ๋์ ๊ฒ๋ค์ <u>์ ํํ๊ฒ ์ฃผ์ด์ง ๊ธฐ๋ฅ๋ง, ์ฆ, ๋ด๊ฐ ์ด๋ฆ์ ์ ํ ๊ฒ๋ง  ์ํ</u>ํด์ผ ํ๋ค!</strong> ๊ทธ๋์ผ ์ข์ ์ฝ๋, ๊ฐ๋์ฑ์ด ์ข๊ณ  ๊น๋ํ ์ฝ๋๊ฐ ๋  ์ ์๊ฒ ์ง. ๊ทธ ์ด์์ ํจ์๊ฐ ์ํํ๊ฒ ๋๋ฉด ์ฝ๋๋ ๋ณต์กํด์ง๊ณ , ์ง์ ๋ถํด์ง ์๋ฐ์ ์์..       

๊ท์ฐฎ์ง๋ง! ๋งค์ฐ ์ข์ ์ฐ์ต์ด๋, breakdownํ๋ ๊ฒ์ ์ต์ํด์ง์ ๐ฉ๐ปโ๐ป
    
</div>

์ด์  ํ ๋ฒ ์ฝ๋๋ฅผ ์์ฑํด๋ณด์.    
์์ธํ ๋ด์ฉ์ ์ฃผ์์ ์ฐธ๊ณ !   

```python
# topological์์ ๋ฆฌํดํ  dictํํ๋ฅผ ๋ง๋ค์ด์ค ๋ ํ์ํ defaultdict import
from collections import defaultdict

# BFS์์ ํ์ํ queue ๋๋ฌธ์ deque import
from collections import deque

# ๊ทธ๋ํ ํํ๋ฅผ 2D array๋ก ์๋ ฅ๋ฐ๋๋ค.
inputs = [['S', 'J'], ['S', 'I'], ['J', 'Mex'], ['J', 'Mor'], ['Mor', 'H'], ['Mor', 'Jap'], ['Mex', 'Jap'], ['Jap', 'E'], ['Jap', 'C'], ['Jap', 'F'], ['I', 'F']]

def solution(list, target):
    if len(list) == 0:
        return []
	
    adjacency_list = topological_sort(list)
    
    return BFS(adjacency_list)
	
# input์ผ๋ก ์ฃผ์ด์ง 2D array๋ฅผ ๋ด๊ฐ ํ์ฌ traversing ํ  ์ ์๋๋ก dictionary(graph)๋ฅผ ๋ง๋ค์ด์ฃผ์๋ค!   
def topological_sort(list):
    route = lambda:{'incoming': 0, 'dest': []}
    
    map = defaultdict(route)
    
    for i in range(len(list)):
        from_node = list[i][0]
        to_node = list[i][1]
	
	# ๋์ฐฉ์ง dest์ append	
        map[from_node]['dest'].append(to_node)
	
	# to_node๋ ๋ค์ด์ค๋ ๊ฒ์ด ํ๋ ์๋ค๋ ๋ป์ด๋ฏ๋ก 1 ์ฆ๊ฐ	
	map[to_node]['incoming'] += 1
		
    return map


    
def BFS(graph, target):
    source = find_the_source(graph)

    if not source:
        return 'We cannot find the source'
    
    # source์์์ initial_depth = 0 (๋ง์น source๊ฐ root์ธ ํธ๋ฆฌ์ฒ๋ผ ์๊ฐํ๋ ๊ฒ)
    queue = deque([[source, 0]])

    # while and queue
    while queue:
        [key, current_depth] = queue.popleft()
        current_node = graph[key]

        children = current_node['dest']

        if key == target:
            return current_depth
        
        for i in range(len(children)):
            queue.append([children[i], current_depth+1])

    return -1
					

def find_the_source(graph):
    for key, val in graph.items():
        if val['incoming'] == 0:
            return key
    
    # edge case
    return None
		

print(solution(inputs, 'F'))
```

<div class="notice--primary" markdown="1">
๐๐ปโโ๏ธ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u><code>route = lambda:{'incoming': 0, 'dest': []}</code></u> ์ด๊ฑด ๋ญ์ฃ ? </strong>     

๊ทธ๋ฅ <code>route = {'incoming': 0, 'dest': []}</code> ๋ก ์ ์ธํ์ฌ ์ฌ์ฉํ์ ๊ฒฝ์ฐ, <code>TypeError: first argument must be callable or None</code>๋ผ๋ ์ค๋ฅ๊ฐ ๋ฐ์ํ๋ค.     

๋นํฉํด์ ์ฐพ์๋ณด๋, ์ด๋ฐ ์ด์ ๋ผ๊ณ  ํจ.     

<strong><u>For a defaultdict the default value is usually not really a value, it a factory</u>: a method that generates a new value.</strong> You can solve this issue by using a lambda expression that generates whatever you wanted.      

๋๋ ์ฌ๊ธฐ์. <code> {'incoming': 0, 'dest': []} </code>๋ผ๋ ํน์  <code>dictionary</code>๋ฅผ default ์ธ์๋ก ํ๋ <code>defaultdict</code>๋ฅผ ๋ง๋ค๊ณ ์ ํ์ผ๋ฏ๋ก, <code>lambda:{'incoming': 0, 'dest': []}</code>๋ผ๊ณ  ์์ฑํ๋ฉด ๋๋ ๊ฒ์ด๋ค!       

ํน์ฌ๋ defaultdict๊ฐ ๋ญ์ง ๋ชจ๋ฅธ๋ค! ํน์ ์์ด๋ฒ๋ ธ๋ค! ์ ๊ฒฝ์ฐ๋ผ๋ฉด <a href="https://dongdongfather.tistory.com/69">"์ด ๋งํฌ"</a>๋ฅผ ์ฐธ๊ณ ํ์!       
    
</div>


๊ทธ๋ผ ๋ง์ฝ ์ต๋จ ๊ฒฝ๋ก์ ๊ธธ์ด๊ฐ ์๋, **<u>์ต๋จ ๊ฒฝ๋ก์ฒด์์ฒด๋ฅผ ๋ฆฌํด</u>ํ๊ณ  ์ถ๋ค**๋ฉด ์ด๋ป๊ฒ ํ๋ฉด ๋ ๊น?      
๊ฐ๋จํ๋ค. BFS ํจ์์์ `depth` ๋์  `path`๋ฅผ ๊ธฐ๋กํ๋ฉด ๋จ!     

     
```python           
def BFS(graph, target):
    source = find_the_source(graph)

    if not source:
        return 'We cannot find the source'
    
    path = source
    
    queue = deque([[source, path]])

    while queue:
        key, current_path = queue.popleft()
        
        current_node = graph[key]

        children = current_node['dest']

        if key == target:
            return current_path
        
        for i in range(len(children)):
            queue.append([children[i], current_path + ' -> ' + children[i]])       
        

    return -1
```




<div class="notice--primary" markdown="1">
๐ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u>๋ค์ ๋ณด๋ฉฐ ํท๊ฐ๋ ธ๊ฑฐ๋ ์๋ก์ ๋ ๋ด์ฉ</u></strong>        

1. Topological Sort         
2. BFS    
3. Queue : [] ์ฃผ์!    
4. defaultdict     
5. defaultdict ์์ defaultdict ๋ฃ๊ธฐ!    

</div>
