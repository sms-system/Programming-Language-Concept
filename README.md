Example of syntax:

    @Tasks
    import Set
    import Suffix
    import Generator
    
    all is N
    all in [-100..-20] or [20..100]
    ans ! /0$/
    
      @1
      a in (1..8]
      b in [1..a]
      ans maybe = 0 //ещё можно ans ignore // ans forget
      ans(Ответ) = a - b
    
      @2
      E1{a,b} < 0 or ans < 0
      ans = a - b
      if b < 0 -> b set '({{b}})'
    
    for i in {1..30}
      generate all except i
      print
        Вариант {{i}}:
        1) Задача: На столе лежал{{suffix a@1:,о,о}} {{a@1}} пирож{{suffix a@1:ок,кa,ков}} из них {{b@1}} съели.
        Сколько осталось?
        
      print@2
        2) {{a}}-{{b}} =
    
    //      A{a,b} < 0 if A{b,a} > 0   -  a<0, если b>0, аналогично b<0, если a>0
    //      E1{a,b}<0 or ans < 0      -  Среди a,b есть только одно значение меньше нуля, или сам ответ <0
    //      * all, := set
    
    //   ∪    u                ∧   &                     !     fact
    //   ∩    n                ¬   !                     ∈ ⊆   in
    //   ∀    V                ∅   {}                    ⊇     has
    //   ∃    E                ≈   ~=                    →     ->
    //   ∞    inf              ≠   !=                    ↔     <->
    //   ∪ ∨  or               √   sqrt                  :     :
