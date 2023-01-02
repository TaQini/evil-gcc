# gcc-attack-preprocess

# alias gcc

```bash
mv evil /tmp/evil
alias gcc='gcc -I /tmp/evil'
```

# demo
 - evil      : dir for evil headers
 - hello.c   : src code
 - hello-E.c : after evil preprocess