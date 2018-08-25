---
layout: article
title: "Kanade 算法"
categories: algorithm
image:
  feature: spot.jpg
  teaser: spot.jpg
---
##Kanade 算法
用于求解给定数组中，最大子数组和的算法。  
如一个数组[-1, 2, 3, -4, 6], 求最大的子数组值
  
1. max__cur = 0, max\__so_far = 0  (element = -1)  
2. max_cur = 2, max\_so\_far = 2 (element = 2)
3. max_cur = 5, max\_so\_far = 5 (element = 3)
4. max_cur = 1 (5+(-4)) max\_so\_far = 5 (element = -4)
5. max_cur = 7 max\_so\_far = 7 (element = 6)
6. return max\_so_far

伪代码如下：

```
Initialize params:
	max_so_far = 0; // 目前为止最大的值，用于输出
	max_cur = 0; 	 // 用于记录每个连续子数组的值，
					// 当遇到子数组和递减时，赋0
	
// Start loop
for element in array:
	max_cur = max(0, max_cur + A[i]);
	max_so_far = max(max_cur, max_so_far);
		
return max_so_far

```

C++算法：

```
//
//  main.cpp
//  C++
//
//  Created by lee on 25/08/2018.
//  Copyright © 2018 lee. All rights reserved.
//

#include <iostream>
#include <vector>
using namespace std;

int Max_subarray(vector<int> Array){
    int max_so_far = 0;
    int max_cur = 0;
    for (auto i = 0; i < Array.size(); ++i){
        max_cur = max(0, max_cur + Array[i]);
        max_so_far = max(max_so_far, max_cur);
    }
    return max_so_far;
}

int main(int argc, const char * argv[]) {
    vector<int> Array{-1, 2, 3, -4, 6};
    int res = 0;
    res = Max_subarray(Array);
    cout << "result is: " << res << endl;
    return 0;
}

```