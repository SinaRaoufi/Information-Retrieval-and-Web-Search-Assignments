# Assignment 2
Create a <ins>Positional Index</ins> for the following text documents and then show how to process a Phrase Query with it.
## Documents:

**d1:** The greatest glory in living lies not in never falling, but in rising every time we fall.

**d2:** The way to get started is to quit talking and begin doing.

**d3:** Your time is limited, so don't waste it living someone else's life. Don't be trapped by dogma – which is living with the results of other people's thinking.

**d4:** If life were predictable it would cease to be life, and be without flavor.

**d5:** If you look at what you have in life, you'll always have more. If you look at what you don't have in life, you'll never have enough.

**d6:** If you set your goals ridiculously high and it's a failure, you will fail above everyone else's success.

**d7:** Life is what happens when you're busy making other plans.

**d8:** Whatever life passes, you remember it happily. Today's face is better viewed in the tomorrow's mirror.

## Positional Indexing
positional indexing refers to the process of indexing and retrieving documents based on the position of query terms within those documents.

<a, 1;
d6: 9;>

<above, 1;
d6: 14;>

<always, 1;
d5: 10;>

<and, 3;
d2: 9;
d4: 10;
d6: 7;>

<at, 1;
d5: 3, 16;>

<be, 2;
d3: 13;
d4: 8, 11;>

<begin, 1;
d2: 10;>

<better, 1;
d8: 10;>

<busy, 1;
d7: 6;>

<but, 1;
d1: 10;>

<by, 1;
d3: 15;>

<cease, 1;
d4: 6;>

<dogma, 1;
d3: 16;>

<doing, 1;
d2: 11;>

<don't, 2;
d3: 5;
d5: 19;>

<else’s, 2;
d3: 10;
d6: 16;>

<enough, 1;
d5: 26;>

<every, 1;
d1: 13;>

<everyone, 1;
d6: 15;>

<face, 1;
d8: 8;>

<fail, 1;
d6: 13;>

<failure, 1;
d6: 10;>

<fall, 1;
d1: 16;>

<falling, 1;
d1: 9;>

<flavor, 1;
d4: 13;>

<get, 1;
d2: 3;>

<glory, 1;
d1: 2;>

<goals, 1;
d6: 4;>

<greatest, 1;
d1: 1;>

<happens, 1;
d7: 3;>

<happily, 1;
d8: 6;>

<have, 1;
d5: 6, 11, 20, 25;>

<high, 1;
d6: 6;>

<if, 3;
d4: 0;
d5: 0, 13;
d6: 0;>

<in, 3;
d1: 3, 7, 11;
d5: 7, 21;
d8: 12;>

<is, 4;
d2: 5;
d3: 2, 18;
d7: 1;
d8: 9;>

<it, 3;
d3: 7;
d4: 4;
d8: 5;>

<it's, 1;
d6: 8;>

<lies, 1;
d1: 5;>

<life, 5;
d3: 11;
d4: 1, 9;
d5: 8, 22;
d7: 0;
d8: 1;>

<limited, 1;
d3: 3;>

<living, 2;
d1: 4;
d3: 8, 19;>

<look, 1;
d5: 2, 15;>

<making, 1;
d7: 7;>

<mirror, 1;
d8: 15;>

<more, 1;
d5: 12;>

<never, 2;
d1: 8;
d5: 24;>

<not, 1;
d1: 6;>

<of, 1;
d3: 23;>

<other, 2;
d3: 24;
d7: 8;>

<passes, 1;
d8: 2;>

<people's, 1;
d3: 25;>

<plans, 1;
d7: 9;>

<predictable, 1;
d4: 3;>

<quit, 1;
d2: 7;>

<remember, 1;
d8: 4;>

<results, 1;
d3: 22;>

<ridiculously, 1;
d6: 5;>

<rising, 1;
d1: 12;>

<set, 1;
d6: 2;>

<so, 1;
d3: 4;>

<someone, 1;
d3: 9;>

<started, 1;
d2: 4;>

<success, 1;
d6: 17;>

<talking, 1;
d2: 8;>

<the, 4;
d1: 0;
d2: 0;
d3: 21;
d8: 13;>

<thinking, 1;
d3: 26;>

<time, 2;
d1: 14;
d3: 1;>

<to, 2;
d2: 2, 6;
d4: 7;>

<today's, 1;
d8: 7;>

<tomorrow's, 1;
d8: 14;>

<trapped, 1;
d3: 14;>

<viewed, 1;
d8: 11;>

<waste, 1;
d3: 6;>

<way, 1;
d2: 1;>

<we, 1;
d1: 15;>

<were, 1;
d4: 2;>

<what, 2;
d5: 4, 17;
d7: 2;>

<whatever, 1;
d8: 0;>

<when, 1;
d7: 4;>

<which, 1;
d3: 17;>

<will, 1;
d6: 12;>

<with, 1;
d3: 20;>

<without, 1;
d4: 12;>

<would, 1;
d4: 5;>

<you, 3;
d5: 1, 5, 14, 18;
d6: 1, 11;
d8: 3;>

<you'll, 1;
d5: 9, 23;>

<you're, 1;
d7: 5;>

<your, 2;
d3: 0;
d6: 3;>

## Phrase Queries

- **q1:** `get started`

    get -> [**d2: 3;**]     
    started -> [**d2: 4;**]

    **result: d2**

- **q2:** `the greatest`

    the -> [**d1: 0;**, d2: 0; d3: 21; d8: 13;]     
    greatest -> [**d1: 1;**]

    **result: d1**

- **q3:** `to be`

    to -> [d2: 2, 6; **d4: 7;**]        
    be -> [d3: 1; **d4: 8, 11;**]

    **result: d4**

- **q4:** `always busy`

    always -> [d5: 10;]     
    busy -> [d7: 6;]

    **result: none**

- **q5:** `high standards`

    high -> [d6: 6;]    
    standards -> []

    **result: none**
