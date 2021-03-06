# Bracket Sequence

## Turing Machine for Parenthesis Matching

### Code:

```
# turing_code.txt

ALPHABET = {(, ), X, _, 1, 0};
EMPTY = {_};
START_STATE = {q1};
STOP_STATE = {q0};

q1,( -> q1,(,R;
q1,) -> q2,X,L;
q1,X -> q1,X,R;
q1,_ -> q3,_,L;

q2,( -> q1,X,R;
q2,X -> q2,X,L;
q2,_ -> q4,_,R;

q3,( -> q0,0,S;
q3,X -> q3,_,L;
q3,_ -> q0,1,S;

q4,( -> q4,_,L;
q4,) -> q4,_,L;
q4,X -> q4,_,L;
q4,_ -> q0,0,S;
```

### Visualisation:

<p align="center">
  <img src="img/Bracket_Sequence.gif">
</p>


## More Examples:

1. [Double Ones](../Double%20Ones/README.md)
2. [Right Shift](../Right%20Shift/README.md)