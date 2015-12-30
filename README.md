#Tips and best practices
**This document is part of an on-going effort to teach students at Turner Fenton good programming practices.**

1. Don’t copy and paste code from others. In fact, never copy and paste code. If you’re doing that, then put it into a method/function and call method where you would have pasted the code. This way, if in the future you need to change that code, you only need to do it in one place. 

2. Stickers make life better.

3. Double check your code before running it. Look for missing semicolons, parentheses, and brackets! Make sure your loops aren’t infinite. 

4. Put spaces between operators and use a consistent indentation style:
  
  **Do** this. This will make your teacher happy :smiley:

  ```
  for (i = 0; i < n; i++) {
    int t = s[i];
    s[i] = s[n - 1];
    s[n - 1] = t;
    r += countFactorial(s, n - 1, total);
    s[n - 1] = s[i];
    s[i] = t;
  }
  ```

  Or this. Note the first bracket is on a new line after the for loop. But **don’t mix it** with the above indentation style! A lot of people use the above style but it’s a matter of preference. With the indentation style below, some people will find it easier to see where your code blocks start and end. You can still see it with the style above, but not as easily.
  
  ```
  for (i = 0; i < n; i++)
  {
     int t = s[i];
     s[i] = s[n - 1];
     s[n - 1] = t;
     r += countFactorial(s, n - 1, total);
     s[n - 1] = s[i];
     s[i] = t;
  }
  ```

  **Don’t** do this. This will make your teacher sad :disappointed:
  
  ```
  for(i=0;i<n;i++){
  int t=s[i];
  s[i]=s[n-1];
  s[n-1]=t;
  r+=countFactorial(s,n-1,total);
  s[n-1]=s[i];
  s[i]=t;
  }
  ```

5. Use descriptive variable names. For example, instead of `n` in the above example, you could use `numberOfElements` if it’s an array. `i`, `j`, `k`, etc are often used for loop indices. Those names are understood to be indices and so don’t have to be descriptive. 

6. Avoid magic numbers. Magic numbers are helpful (actually... no they’re not) things like 
 
  ```
  if (Math.random() * 23 > 5.23) {
    // do something
  }
  ```
  What do 23 and 5.23 mean? Use variable names for numerical constants. For example, a more descriptive name for 23 can be `UPPER_BOUND` and for 5.23 it can be `THRESHOLD`.

7. Code grouping is good. Similar or logically separate tasks can be grouped with empty lines between different tasks. For example, different sections in the following are 1) initialize variables 2) Create a BufferedReader 3) Use a for loop to initialize the set of values.
  
  ```
  int i, n;
  String s;
  int[] set = new int[11];
  
  BufferedReader bis = new BufferedReader(new InputStreamReader(System.in));
  
  for (i = 0; i < 11; i++) {
     set[i] = i + 1;
  }
```

8. Avoid too much nesting: for loop within a for loop within a for loop within a for loop with an if and statement and a while loop inside that if statement. Confusing, right? Don't be that person.

9. When Googling for code online, use it carefully. Don’t copy and paste it without fully understanding what the code does. It probably won’t work because your use case is different.

10. Debug as you go. Don’t write the full program and then debug. In non-trivial programs, there are too many variables to handle at the end. You should check that your code works after every feature implementation and during feature implementation whenever it makes sense.

11. Comment your code. Especially complicated things. Avoid commenting obvious stuff like
  ```
  // adds 5 to x
  x += 5;
  ```

12. Ready to Program is for learning. You won’t use it outside the classroom. Take a look at [IntelliJ IDEA](https://www.jetbrains.com/idea/) (our favorite), [Eclipse](https://eclipse.org/), or [NetBeans](https://netbeans.org/). Those are Integrated Development Environments (aka IDEs) which provide cool tools to make your life easier.
  - They provide intelligent code completion: instead of typing everything out, a drop down menu will appear beside the carat with suggestions. You just need to type 2 or 3 letters and then press enter on the suggestion you want. This saves a lot of time.
  - They have lots of shortcuts: In IntelliJ, Instead of creating a for loop manually, type ‘for’ + tab and a for loop template will be generated. Instead of renaming every variable, method, or class manually, click on any name and press shift + F6 and rename all matching names at once. And so on. 
  - They support easy version control: you can connect your project to something like Github from inside the IDE. It’s like an online backup. But you can also share the code with other people like that. It’s great for working on teams and is how open source projects are maintained. 
  
  They can do lots of [other stuff](https://www.jetbrains.com/idea/features/) like help you find bugs which is why you’re using Ready to Program. There are also other options like vim, vi, and emacs for the true coder but they have a steeper learning curve than IDEs do.

