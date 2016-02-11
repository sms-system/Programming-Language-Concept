Example of syntax:

    @Tasks
    import /Generator
    import /Grammar/Rus
    
    * in N
    * in [-100..-20] or [20..100]
    ans ! _0
    
      @1
      a in [2..100]
      b in [1..a]
      b != a
      ans maybe = 0
    
      @2
      E1(a,b) < 0 or ans < 0
    
      @1, @2
      ans = a-b
    
    for i in [1..30]
      generate * except i
      _ Вариант {i}:
      _ 1) Задача: На столе лежал{suffix a@1:,о,о} {a@1} пирож{suffix a@1:ок,кa,ков} из них {b@1} съели.
      _ Сколько осталось?
      use 2
      _ 2) {a}-{b} =
    
    
    @Example
    fib(i i) n = f n 0 1
    | f(i i i:i) n a b
      | n = 0 -> a
      | otherwise -> f (n-1) b (a+b)
    
    qsort([]:[]) arr
    | arr = [] -> []
    | otherwise -> ++ 
      qsort[a| a in arr, a < x]
      b| b in arr, b = x
      qsort[c| c in arr, c > x]
    
    //      A{a,b} < 0 if A{b,a} > 0   -  a<0, если b>0, аналогично b<0, если a>0
    //      E1{a,b}<0 or ans < 0       -  Среди a,b есть только одно значение меньше нуля, или сам ответ <0
    //      * all, := set
    
    //   ∪    u                ∧   &                     !     fact
    //   ∩    n                ¬   !                     ∈ ⊆   in
    //   ∀    V                ∅   {}                    ⊇     has
    //   ∃    E                ≈   ~=                    →     ->
    //   ∞    inf              ≠   !=                    ↔     <->
    //   ∪ ∨  or               √   sqrt                  :     :
