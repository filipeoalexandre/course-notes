# Some notes on google's technical writing 

Course and more details [here](https://developers.google.com/tech-writing)

## Actual notes

* Define new terms, link to definition of existing terms
  
* When using acronyms, use its extended version alongside the shortened for the first time

* Avoid using pronouns if the name its referring to is "far" away (a good rule of thumb is around 5 words of maximum distance)

* Avoid using indirect (or reported) speech - avoid as much as possible verb **to be**

    :thumbsup: `He laid down his bundle and thought of his misfortune. "And just what pleasure have I found, since I came into this world?" he asked.`

    :thumbsdown: `He laid down his bundle and thought of his misfortune. He asked himself what pleasure he had found since he came into the world.`

* Avoid weak verbs that transmit uncertainty

    Weak | Strong
    :---: | :---:
    The error **occurs** when clicking the Submit button. | Clicking the Submit button **triggers** the error.
    This error message **happens** when... | The system **generates** this error message when...
    We **are** very careful to ensure... | We **carefully** ensure...

* Reduce usage of `there is/there are`
 
    ```
    There are some facts you should know -> You should know some facts

    There is no creator stack for the main thread -> The main thread does not provide a creator stack
    ```

* Use short sentences that transmit a single idea

* Enumerations should be transformed into unsorted lists

* Avoid using filler words, go straight to the point

* Use `which` for non essential subordinate clauses and `that` for essential

    ```
    ..., which Guido invented.

    Fortran is perfect for calculations that don't involve algebra

    ```

* Sorted lists should use imperative verbs

  1. Instantiate the Froobus class.
  2. Invoke the Froobus.Salmonella() method.
  3. The process stalls.


* List items should be parallel (grammar, logical category, capitalization, punctuation)

    *Grammar in this context means that all list members should be of the same category. For example: all names, all adjectives or all sentences*

* The opening sentence of a paragraph should be captivating, intersting, and establish the paragraph's point. 

* Restrict one paragraph to one idea/theme

* Good paragraphs answer three questions:
  
  1. **What** are you trying to tell the reader?
  2. **Why** is it important for the reader to know this?
  3. **How** should the reader use this knowledge?

  Example: 

  ```
  <Start of what> The garp() function returns the delta between a dataset's mean and median.<End of what><Start of why>
   Many people believe unquestioningly that a mean always holds the truth. However, a mean is easily influenced by a 
   few very large or very small data points.<End of why><Start of how> Call garp() to help determine whether a few very 
   large or very small data points are influencing the mean too much. A relatively small garp() value suggests that 
   the mean is more meaningful than when the garp() value is relatively high.<End of how>
  ```

* The document you are writing should tell your audience what it doesn't know yet it needs to know.

* Audiences should be separated into **roles** (SW engineers, scientists, undergrad students, professionals in scientific fields, etc.) and **skills** (knowledge of big O notation, equations of motion, etc.)

* Avoid expressions that only make sense in certain areas. Be as culturally neutral as possible. (Example: A British might not understand a NASCAR analogy)

* Clearly state the scope of the document, its audience and any previous knowledge requirements

* Documents should have an outline at the beginning indicating its key points. Long documents should also contain a TL;DR
