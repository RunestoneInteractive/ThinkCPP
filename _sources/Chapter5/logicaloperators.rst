Logical operators
-----------------

There are three **logical operators** in C++: AND, OR and NOT, which are
denoted by the symbols ''&&'', ''\|\|'' and ''!''. The semantics (meaning) of these
operators is similar to their meaning in English. For example ''x > 0 && x
< 10'' is true only if x is greater than zero AND less than 10.

''evenFlag \|\| n%3 == 0'' is true if *either* of the conditions is true,
that is, if evenFlag is true OR the number is divisible by 3.

Finally, the NOT operator has the effect of negating or inverting a bool
expression, so !evenFlag is true if evenFlag is false; that is, if the
number is odd.

Logical operators often provide a way to simplify nested conditional
statements.


.. mchoice:: logical_op_1
   :multiple_answers:
   :answer_a: if (x > 0 && x < 10) {...
   :answer_b: if (x > 0 || x < 10) {...
   :answer_c: if (x > 0 ! x < 10) {...
   :answer_d: if ( !(x < 0) && !(x > 10) ) {...
   :answer_e: if ( !(x <= 0) && !(x >= 10) ) {...
   :correct: a,e
   :feedback_a: This is exactly what the nested conditionals are saying.
   :feedback_b: || represents "or", but we need both sides of the conditional to be true.
   :feedback_c: The ! operator cannot be used to compare two sides of a conditional.
   :feedback_d: If x = 0 or if x = 10, this expression will return true when it shouldn't.
   :feedback_e: If it IS NOT what we don't want, then it IS what we want!

   How could you re-write the following code using a single conditional?

   ::

      if (x > 0) {
        if (x < 10) {
          cout << "x is a positive single digit" << endl;
        }
      }

.. dragndrop:: logical_op_2
   :feedback: Try again!
   :match_1: (n * 2 > 10 && n >= 7)|||true, "and"
   :match_2: (n * 2 > 10 && n < 7)|||false, "and"
   :match_3: (n%2 == 1 || n == 8)|||true, "or"
   :match_4: (n%2 == 0 || n == 8)|||false, "or"
   :match_5: !(n == 7)|||false, "not"
   :match_6: !(n >= 10)|||true, "not"

   Match the conditional statement to the correct boolean and the meaning of the operator in use, given n = 7.
