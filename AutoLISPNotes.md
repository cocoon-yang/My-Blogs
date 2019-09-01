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
(car myList) ; return 1 
(cadr myList) ; return 2
(caddr myList) ; return 3
(nth 3 myList) ; return 3 
(cdr myList) ; Returns '(2 3 4 5 6)
```

```
(member 'c' (a b c d e)) ; returns (c d e).
```

```
(foreach n ans_list (strcase n))
```

Lists Functions 
```
(append '(1 2 3) '(4 5 6)) ; return '(1 2 3 4 5 6)
```

```
(length '(a b c d)) ; returns 4.
```

```
(apply '+ (23 12 -10)) ;Returns 25
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


## Examples

Change Layer[[AutoLisp Start]]
```
(defun c:chlayer (/ a1 a2 n index b1 b2 d1 d2 b3)
(graphscr)
(prompt "\nselect entities to be changed: ")
(setq a1 (ssget))
(prompt "\npoint to entity on target layer: ")
(setq a2 (entsel))
(setq n (sslength a1))
(setq index 0)
(setq b2 (entget (car a2)))
(setq d2 (assoc 8 b2))
(repeat n
(setq b1 (entget (ssname a1 index)))
(setq d1 (assoc 8 b1))
(setq b3 (subst d2 d1 b1))
(entmod b3)
(setq index (+ index 1))
)
(princ)
)
```

Global Text Height Change [[AutoLisp Start]]
```
(defun chtext (/ a ts n index b1 b c d b2)
(setq a (ssget))
(setq ts (getreal "\nEnter new text size"))
(setq n (sslength a))
(setq index 0)
(repeat n
(setq b1 (entget (ssname a index)))
(setq index (1+ index))
(setq b (assoc 0 b1))
(if (= "TEXT" (cdr b))
(progn
(setq c (assoc 40 b1))
(setq d (cons (car c) ts))
(setq b2 (subst d c b1))
(entmod b2))))
(princ)
)
```

[More AutoLISP examples[Examples]]
## References

[draftsperson]: http://draftsperson.net/index.php?title=AutoLISP_Lesson_1_-_Introduction_to_Lisp_Programming "draftsperson"

[tutorialspoint]: https://www.tutorialspoint.com/lisp/index.htm "tutorialspoint" 

[AutoLisp Start]: https://www.cadtutor.net/tutorials/autolisp/quick-start.php

[Examples]: http://www.lee-mac.com/programs.html
