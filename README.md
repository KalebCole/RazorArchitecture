- When you run your website you will notice everything seems to work but none of your changes persist from page to page.
    - Why do you think that is?
Every time we rerender the page, the constructor is called again, which has all of the data, so it is refreshed.
    - What change do you think we could make to solve the problem?
Guess 1: If we move the data into a more persistent location like a database or even a json file and fetch data from it, it will solve the problem.
Guess 2 (after seeing the answer): Additionally, we can change the scope of the dependency injection to only call the constructor at the start.
    - Why do you think it works after making the change?
It works because the program does not call the constructor every rerender of the page. It only calls the constructor at the start, so the "new" keyword is not being invoked.
