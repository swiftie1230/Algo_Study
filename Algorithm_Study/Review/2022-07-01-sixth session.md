# โ๏ธ <u>Advanced Topological Sort + BFS</u>  



## ๐ Advanced Topological Sort + BFS

์ ๋ฒ ์๊ฐ์ ๋ค์ํ ๋คํธ์ํฌ ์๋ฒ๋ค์ ์ฐ๊ฒฐ๊ณผ ๊ฐ์ ๊ด๊ณ์ฑ์ ๋ํ๋ธ ๊ทธ๋ํ๊ฐ ์ฃผ์ด์ง๊ณ  `source`์ `destination`์ด ์์ ๋, **<u>Topological Sort</u>**๋ ๊ฐ ์ ์๋ ๋ฐฉ๋ฒ, ์ด๋ค ์์ผ๋ก ์์๋ฅผ ์ ํด์ผ ํ๋๋ ๋ฑ์ ๋ฌธ์ ์ ํ์ํ **"REARRANGE"**๋ฅผ ํ๋ ๊ฒ์ด๋ผ๊ณ  ๋ฐฐ์ ๋ค.     

์ ๋ฒ ๊ฐ์ ์ ๋ฆฌ ๋งํฌ : [์๊ธฐ !](https://swiftie1230.github.io/algorithm_study/์๊ณ ๋ฆฌ์ฆํ์ฉ-TopologicalSort_BFS-์ ๋ฆฌ/)

๊ทธ๋ ๋ค๋ฉด ์ด๋ฒ์๋ ์กฐ๊ธ ๋ ์ฌํ๋, **์ฐ์ ์์๊ฐ ์ฃผ์ด์ ธ ์์ ๋, ๊ทธ๋ค ์ฌ์ด์ scheduling์ ํด๋ณด๋ ๊ฒ**์ด๋ค.      

์๋ฅผ ๋ค์ด, ๊ทธ๋ํ์ ๋ชจ๋  `[pre, post]` ๋ค์ด  `[[math1, math2], [math0, math2], [math2, math3]]` ๋ก ์ฃผ์ด์ก๋ค๊ณ  ๊ฐ์ ํด๋ณด์. (`pre`๋ฅผ ๊ฑฐ์น ํ์์ผ `post`๊ฐ ๊ฐ๋ฅํ๋ค. ์ฆ, ์ ์์์์๋ `math1`๊ณผ `math0`์ ๊ฑฐ์ณ์ผ `math2`๋ฅผ ๊ฑฐ์น  ์ ์๋ ๊ฒ!)         

๊ทธ๋ ๋ค๋ฉด ์ฐ๋ฆฌ๋ ์ ์ฐ์ ์์๋ฅผ ๋ง์กฑ์ํค๋ scheduling์ ์ฐพ์ return ํ๋ ์๊ณ ๋ฆฌ์ฆ์ ์ง๋ ๊ฒ์ด๋ค.     
์๋ฅผ ๋ค๋ฉด ํ๊ฐ์ง schedule์ `math0 โ math1 โ math2 โ math3`๊ฐ ์์ ์ ์๊ฒ ์ง.    

์ด๋ ์ฌ์ฉํ๋ ๋ฐฉ๋ฒ์ด ๋ฐ๋ก ์กฐ๊ธ ๋ ์ฌํ๋! **`Advanced Topological Sort + BFS`**๋ค!



* * *



๊ทธ๋ผ ์ด์  ๋ณธ๊ฒฉ์ ์ผ๋ก Advanced Topological Sort + BFS๋ฅผ ์ฌ์ฉํ๋ ์ค์  ๋ฌธ์ ๋ฅผ ์ ํด๋ณด์!   
์ค์ ๋ก ๊ฐ์ํด ์ฃผ์๋ฉฐ ์์๋ก ๋ค์ผ์จ๋ ๋ฌธ์ ์๋ค ๐    

## ๐ฌ Problem

### ๐ ๋ฌธ์  ์ค๋ช   

๋ชจ๋  `[pre, from]` ๋ค์ด `2D array`๋ก ์ฃผ์ด์ก๋ค๊ณ  ๊ฐ์ ํด๋ณด์.     

```python
[["math1", "math2"], ["math0", "math2"], ["math2", "math3"], ["math0", "math4"], ["math3", "math5"], ["math4", "math5"]]
```

์ด๋ ๊ฒ input์ด ์ฃผ์ด์ก์ ๋, ์ฌ๊ธฐ์ ์๋กญ๊ฒ ์๊ฐํด๋ด์ผ ํ  ๊ฑด **<u>์ฐ์ ์์</u>**๋ค. ์ด ๋ฌธ์ ์์ ๋ณด๋ฉด `math1`๊ณผ `math0`๊ฐ ์ ํ๋์ด์ผ์ง๋ง `math2`๋ฅผ ๊ฑฐ์น  ์ ์๋ ๋ฐ๋ฉด, `math4`๋ `math0`๋ง ๊ฑฐ์น๋ฉด ๊ฐ๋ฅํ๋ค. ๋ฐ๋ผ์ ์ด๋ ๊ฒ ๊ธฐ์กด topological sort ํ, **<u>์ ํ๋์ด์ผ ํ๋ ๋ธ๋๋ค์ ๋ ๋ฒจ๋ณ๋ก ๊ตฌ๋ถํ์ฌ ํ์ ๋ฃ์ด์ฃผ๊ณ  scheduleํด์ผ ํ๋ค</u>**๋ ๊ฒ์ ์ ์ ์๋ค. ์ด ๊ณผ์ ์์ **<u>BFS</u>**๋ฅผ ์ฌ์ฉํ๋๋ฐ, ์ด ๋ ํ์ ๋ค์์ผ๋ก ๋ฃ์ด์ฃผ๋ ์กฐ๊ฑด์ incoming, ์ฌ๊ธฐ์๋ **<u>`pre`์ ๊ฐ์ด `0`</u>์ด ๋๊ธฐ ์ ๊น์ง๋ ๋ฃ์ด์ฃผ์ง ์๋ค๊ฐ, 0์ด ๋๋ฉด ๋ฃ์ด์ฃผ์ด์ผ ํ๋ค**. (์ฆ, **<u>๊ทธ ์ ์ ์ ํ๋์ด์ผ ํ๋ ๋ธ๋๋ค์ ๋ชจ๋ ๊ฑฐ์น ๊ฒ์ ํ์ธํ ํ</u>์์ผ ํ์ ๋ฃ์ด์ค๋ค**๋ ๋ป.)                   

๊ทธ๋ ๋ค๋ฉด ํด๊ฒฐํ๊ธฐ ์ํด ํด์ผ ํ  ์ผ์ ํฌ๊ฒ ์๋ ๋ ๋จ๊ณ๋ผ๋ ๊ฑด ์๊ฒ ์ง? ๋ํ ์ฐ๋ฆฌ๊ฐ ์ ์ ๋ฐฐ์ด ์๊ณ ๋ฆฌ์ฆ์์ ์ข ๋ ์ฌํํ์ฌ ์์ ํด์ผ ํ  ๋ถ๋ถ์ BFS ๋จ๊ณ๋ผ๋ ๊ฒ ์ญ์ ์ธ์งํ  ์ ์์ ๊ฒ์ด๋ค.         

1. **First Step : <u>Topological Sort</u>**
2. **Second Step : <u>BFS</u>**


<div class="notice--primary" markdown="1">
๐๐ปโโ๏ธ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u></strong>    

์ด ์ฌํ๋ <strong><u>Advanced Topological Sort + BFS ๋ฌธ์ </u></strong>๊ฐ Top 2์ ๋ค ์ ๋๋ก ์ด๋ ต๊ณ , ๊ทธ๋งํผ ์์๋์์ผ ํ  ์ฃผ์ ๋ผ๋๊น ๊ผญ ๊ผผ๊ผผํ ๊ณต๋ถํด๋๊ธฐ ~ ๐ฉ๐ปโ๐ป   
    
</div>


์ด์  ์ฝ๋๋ฅผ ์์ฑํด๋ณด์.        
์ผ๋จ input 2D array ๋จผ์ !        

```python
inputs = [['S', 'J'], ['S', 'I'], ['J', 'Mex'], ['J', 'Mor'], ['Mor', 'H'], ['Mor', 'Jap'], ['Mex', 'Jap'], ['Jap', 'E'], ['Jap', 'C'], ['Jap', 'F'], ['I', 'F']]
```

์ฐ๋ฆฌ๋ ์ด ๋ฌธ์ ๋ฅผ ํด๊ฒฐํ๊ธฐ ์ํด ๋ค ๊ฐ์ง ํจ์๋ฅผ ์์ฑํ  ๊ฒ์ด๋ค! `solution`, `topological_sort`, `BFS`, ๊ทธ๋ฆฌ๊ณ  `find_the_source`๊น์ง.          

**`solutionAdvanced`์ ์ฐ๋ฆฌ๊ฐ ๋ง ๊ทธ๋๋ก ์ด ๋ฌธ์ ๋ฅผ ์ํํ๊ธฐ ์ํด ์ฒ์ ๋ถ๋ฅด๋ ํจ์**. ์ผ๋ฐ ํ๋ก๊ทธ๋จ๋ค์ `main`ํจ์๋ผ๊ณ  ์๊ฐํ๋ฉด ์ดํดํ๊ธฐ ์ฌ์ธ ๊ฒ.        

**`topologicalAdvanced`์ `topological sort`์ ์ฌ์ฉํ์ฌ `input`์ผ๋ก ์ฃผ์ด์ง `2D array`๋ฅผ traversing ํ  ์ ์๋๋ก `dictionary(graph)`๋ก ๋ณํํ์ฌ ๋ฆฌํดํ๋ ํจ์**์ด๋ค.     

๋ค์์ผ๋ก **`find_the_source`๋ ๋ณํํ `dictionary`๋ฅผ ์ด์ฉํด "Source"๋ฅผ ์ฐพ์ ๋ฆฌํดํ๋ ํจ์**์ด๊ณ , **`BFSAdvanced`๋ ์ ํ๋์ด์ผ ํ๋ ๋ธ๋๋ค์ ๋ ๋ฒจ๋ณ๋ก ๊ตฌ๋ถํ์ฌ ํ์ ๋ฃ์ด์ฃผ๊ณ  scheduleํ์ฌ ๋ฆฌํดํ๋ ํจ์**!      


<div class="notice--primary" markdown="1">
๐๐ปโโ๏ธ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u>์ ์ด๋ ๊ฒ ๊ตณ์ด ๋ง์ ํจ์๋ค์?</u></strong>    

๋งค๋ฒ ๊ฐ์กฐํ๊ณ , ๊ฐ์๋ก ๋ผ์ ๋ฆฌ๊ฒ ๋๋ผ๊ณ  ์๋ ๋ถ๋ถ์ด๋ค...๐ญ          
<strong>์ฐ๋ฆฌ๊ฐ function์ด๋ผ๊ณ  ์ ํด ๋์ ๊ฒ๋ค์ <u>์ ํํ๊ฒ ์ฃผ์ด์ง ๊ธฐ๋ฅ๋ง, ์ฆ, ๋ด๊ฐ ์ด๋ฆ์ ์ ํ ๊ฒ๋ง  ์ํ</u>ํด์ผ ํ๋ค!</strong> ๊ทธ๋์ผ ์ข์ ์ฝ๋, ๊ฐ๋์ฑ์ด ์ข๊ณ  ๊น๋ํ ์ฝ๋๊ฐ ๋  ์ ์๊ฒ ์ง. ๊ทธ ์ด์์ ํจ์๊ฐ ์ํํ๊ฒ ๋๋ฉด ์ฝ๋๋ ๋ณต์กํด์ง๊ณ , ์ง์ ๋ถํด์ง ์๋ฐ์ ์์..       

๊ท์ฐฎ์ง๋ง! ๋งค์ฐ ์ข์ ์ฐ์ต์ด๋, <strong><u>breakdown</u></strong>ํ๋ ๊ฒ์ ์ต์ํด์ง์ ๐ฉ๐ปโ๐ป
    
</div>

์ด์  ํ ๋ฒ ์ฝ๋๋ฅผ ์์ฑํด๋ณด์.    
์์ธํ ๋ด์ฉ์ ์ฃผ์์ ์ฐธ๊ณ !   

```python
# topological์์ ๋ฆฌํดํ  dictํํ๋ฅผ ๋ง๋ค์ด์ค ๋ ํ์ํ defaultdict import
from collections import defaultdict

# BFS์์ ํ์ํ queue ๋๋ฌธ์ deque import
from collections import deque

# ๊ทธ๋ํ ํํ๋ฅผ 2D array๋ก ์๋ ฅ๋ฐ๋๋ค.
inputs = [["math1", "math2"], ["math0", "math2"], ["math2", "math3"], ["math0", "math4"], ["math3", "math5"], ["math4", "math5"]]

def solutionAdvanced(list):
    if len(list) == 0:
        return []
	
    adjacency_list = topologicalAdvanced(list)
    
    return BFSAdvanced(adjacency_list)
	

# input์ผ๋ก ์ฃผ์ด์ง 2D array๋ฅผ ๋ด๊ฐ ํ์ฌ traversing ํ  ์ ์๋๋ก dictionary(graph)๋ฅผ ๋ง๋ค์ด์ฃผ์๋ค!   
def topologicalAdvanced(list):
    route = lambda:{'pre': 0, 'post': []}
    
    map = defaultdict(route)
    
    for i in range(len(list)):
        pre_node = list[i][0]
        post_node = list[i][1]

	    # pre_node๋ ๋๊ฐ๋ ๊ฒ์ด ํ๋ ์๋ค๋ ๋ป์ด๋ฏ๋ก post์ append	
        map[pre_node]['post'].append(post_node)
	
	    # post_node๋ ๋ค์ด์ค๋ ๊ฒ์ด ํ๋ ์๋ค๋ ๋ป์ด๋ฏ๋ก pre 1 ์ฆ๊ฐ	
        map[post_node]['pre'] += 1
		
    return map

    
def BFSAdvanced(graph):
    result = ""

    source = find_the_source(graph)

    if not source:
        return 'We cannot find the source'
    
    queue = deque([source])

    # while and queue
    while queue:
        currentLevel = queue.popleft()
        nextLevel = []
        
        for i in range(len(currentLevel)):
            key = currentLevel[i]
            children = graph[key]['post']

            if result == "":
                result += key
            else:
                result += ' -> ' + key

            for j in range(len(children)):
                child = children[j]
                graph[child]['pre'] -= 1
                
                if graph[child]['pre'] == 0:
                    nextLevel.append(child)
        
        if len(nextLevel) > 0:
            queue.append(nextLevel)

    return result

					

def find_the_source(graph):
    sources = []
    for key, val in graph.items():
        if val['pre'] == 0:
            sources.append(key)
    
    return sources
		

print(solutionAdvanced(inputs))
```


<div class="notice--primary" markdown="1">
๐ <strong><u>์ฌ๊ธฐ์ ์ ๊น!</u> : <u>๋ค์ ๋ณด๋ฉฐ ํท๊ฐ๋ ธ๊ฑฐ๋ ์๋ก์ ๋ ๋ด์ฉ</u></strong>        

1. Topological Sort         
2. Advanced BFS        

</div>
