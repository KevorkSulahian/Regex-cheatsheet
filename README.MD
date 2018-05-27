##Some Regex's to remember


```JS

let re; 

// this looks for the strings between the slashes. It will match hello but not HelLo.
re = /hello/;

//the lower case i means be case sensetiven't (insensetive)/ this will mactch HeLLo
re = /hello/i;

console.log("HellO" == re.source); // returns true

// common search characters

re = /^h/i; // the " ^ " means starts with this. if position 0 is not the letter or the number, then it brings back false. Matches "hello" but not "why hello there"

re = /ld%/i // the " $ " means the string must end with the same charcter or number.

re = /^hello$/i; // must start and end with the string.

re = /^hello$/ig; // the lowercase " g " means global. It means search the entire string to find multiple matches.

re = /h.ello$/i; // the " . " is and constant. would match "hallo" or "hbllo"

re = /h.*ello/i; // the same as above but for many chars. would match "hewfrrfnwfegewjmoognwfeojllo.

re = /gre?a?y/i; //the ? means an optional char. it can be either of the char behind a ? or empty

re = /gre?a?y\?/i; // the \ esc meta chars to treat as literals.

re = /gr[ae]y/i; // must be an e or a

re = /[^GF]ray/i; // will match anything EXCEPT GF

re = /[A-Z]ray/; // will match any upper case letter

re = /[a-z]ray/; // will match any lower case letter

re = /[A-Za-z]ray/; // will match any lette

re = /[A-Za-z0-9]ray/; // will match any letter or num

// Braces {} - Quantifiers

re = /He[a-z]{3}/i; // must occur exatctly {m} times. looks at prev char/regex

re = /He[a-z]{2,3}/i; // must occur between range. looks at prev char/regex

re = /He[a-z]{2,}/i; // must occur at least m times.

// Parentheses () - Grouping

re = /([0-9]x){3}/; // matches num then letter x 3x

re = /^([0-9]x){3}$/; // matches ONLY exactly num x 3x b/c of ending dollar sign

// shorthand chars

re = /\w/; //word char

re = /\w+/; //plus = one or more words

re = /\W/; //non-word char

re = /\d/; //match any digit

re = /\d+/; //match any digit 0 or more times

re = /\D+/; //match any non-digit

// re.test(string here) to test



```