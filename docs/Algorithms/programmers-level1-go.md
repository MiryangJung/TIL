---
layout: default
title: Programmers, Golang
parent: Algorithms
---

# [프로그래머스](https://programmers.co.kr/learn/challenges?tab=all_challenges) __Go__ 언어 풀이
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## [모의고사](https://programmers.co.kr/learn/courses/30/lessons/42840)

> Min : *0.00ms, 3.93MB* <br>
> Max : *0.04ms, 3.93MB*

```go
func solution(answers []int) []int {
    
    arr1 := [5]int{1,2,3,4,5}
    arr2 := [8]int{2,1,2,3,2,4,2,5}
    arr3 := [10]int{3,3,1,1,2,2,4,4,5,5}
    
    var cnt1, cnt2, cnt3 int = 0,0,0
    
    for i:=0; i<len(answers); i++{
        if answers[i]==arr1[i%5]{
            cnt1++
        }
        if answers[i]==arr2[i%8]{
            cnt2++
        }
        if answers[i]==arr3[i%10]{
            cnt3++
        }
    }
    
    m := max(cnt1,cnt2);
    m = max(m, cnt3);
    
    answer := []int{}
    if m == cnt1{
       answer = append(answer, 1) 
    }
    if m == cnt2{
       answer = append(answer, 2) 
    }
    if m == cnt3{
       answer = append(answer, 3) 
    }

    return answer
}

func max(a, b int) int {
    if a > b {
        return a
    }
    return b
}
```

*2020.12.16*


## [K번째수](https://programmers.co.kr/learn/courses/30/lessons/42748)

> Min : *0.01ms, 10MB* <br>
> Max : *0.01ms, 10.3MB*

```go

```

*2020.12.16*