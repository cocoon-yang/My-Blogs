# AutoLisp Notes


## Block 

Syntax of block [[tutorialspoint][tutorialspoint]] is 

```
(block block-name(
...
...
))
```

## Lists 

Single dimensional list construction
```
(setq myList '(1 2 3 4 5) ) 
(setq myList  (list 1 2 3 4 5) )
```

Accessing entry of a list 

```
(cdr myList) ; return 1 
(cadr myList) ; return 2
(caddr myList) ; return 3
(nth 3 myList) ; return 3
```

Lists 
```
(append '(1 2 3) '(4 5 6)) ; return '(1 2 3 4 5 6)
```

## Looping Functions

```
(loop (s-expressions))
```
```
(setq a 10)
(loop 
   (setq a (+ a 1))
   (write a)
   (terpri)
   (when (> a 17) (return a))
)
```



```
repeat (repeat number exp ...)
```

```
while (repeat number exp ...)
```


## References

[draftsperson]: http://draftsperson.net/index.php?title=AutoLISP_Lesson_1_-_Introduction_to_Lisp_Programming "draftsperson"

[tutorialspoint]: https://www.tutorialspoint.com/lisp/index.htm "tutorialspoint"

 
