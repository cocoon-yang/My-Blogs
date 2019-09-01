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

```
(member 'c' (a b c d e)) ; returns (c d e).
```


Lists Functions 
```
(append '(1 2 3) '(4 5 6)) ; return '(1 2 3 4 5 6)
```


## String

String methods

```
(strcat "H" "ello"); returns "Hello"
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


The syntax of repeat statement
```
repeat (repeat number exp ...)
```
The syntax of while statement
```
while (repeat number exp ...)
```

The syntax of do statement
```
(do ((variable1    value1   updated-value1)
      (variable2   value2   updated-value2)
      (variable3   value3   updated-value3)
   ...)
   (test return-value)
   (s-expressions)
)
```


## References

[draftsperson]: http://draftsperson.net/index.php?title=AutoLISP_Lesson_1_-_Introduction_to_Lisp_Programming "draftsperson"

[tutorialspoint]: https://www.tutorialspoint.com/lisp/index.htm "tutorialspoint"
