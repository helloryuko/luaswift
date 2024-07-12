<div align='center'>
  luaswift
</div>

<br/>

<div align='center'>
  <a href='https://rjukankukan.github.io/luaswift'>try it out</a>
  <span>&nbsp;-&nbsp;</span>
  <a href='https://github.com/gamesensical/gamesensical.github.io'>forked from...</a>
  <span>&nbsp;-&nbsp;</span>
  <a href='https://t.me/run1t'>contact me</a>
</div>

### what is this?

it makes your lua script go vroom

### how does it make it vroom?

local variables are known for being **faster to access** than the global ones.

this simple tool replaces calls to global functions with calls to local functions.

this is achieved by...
1. parsing the script with `luaparse`
2. going through every function call
3. checking if the function is not defined elsewhere
4. adding the function to the local variables list
5. replacing the function name with the local one

also, it replaces the "dot syntax" with "underscore syntax". love it or not, accessing tables <sub><sup>(and especially accessing global tables)</sup></sub> is slooow.

### why should i prefer this over gamesensical's lua optimizer?

- cool ui
- supports [neverlose](neverlose.cc) <sub><sup>(ironical, right?)</sup></sub>
- doesn't break when using `goto`
- uses `LuaJIT` as a lua version for luaparse

### technologies used...
- [luaparse](https://github.com/oxyc/luaparse)
- [ace (editor)](https://github.com/ajaxorg/ace)
- [lua-beautifier](https://github.com/dptole/lua-beautifier)
