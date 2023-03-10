# Assignment 1
Create <ins>Term-Doc Matrix</ins> and <ins>Inverted Index</ins> for the following text documents. Then process the given queries.

In each step, describe what you do in one sentence.
## Documents:

**d1:** The greatest glory in living lies not in never falling, but in rising every time we fall.

**d2:** The way to get started is to quit talking and begin doing.

**d3:** Your time is limited, so don't waste it living someone else's life. Don't be trapped by dogma – which is living with the results of other people's thinking.

**d4:** If life were predictable it would cease to be life, and be without flavor.

**d5:** If you look at what you have in life, you'll always have more. If you look at what you don't have in life, you'll never have enough.

**d6:** If you set your goals ridiculously high and it's a failure, you will fail above everyone else's success.

**d7:** Life is what happens when you're busy making other plans.

**d8:** Whatever life passes, you remember it happily. Today's face is better viewed in the tomorrow's mirror.

## Queries:

**q1:** Life AND Long

**q2:** Life OR Happy

**q3:** Life AND( Failure OR Success) AND (you OR Your)

**q4:** Life AND NOT(time OR talking)

# Solution

## Doc-Term Matrix
A document-term matrix (DTM) is a mathematical representation of text data, where rows represent individual terms(words, phrases, or concepts) and columns represent documents . Each cell in the matrix contains the frequency or occurrence of a specific term in a particular document. The matrix can be binary, where each cell contains a 1 if the term is present in the document and a 0 if it is not, or it can be weighted, where the cell value is the frequency of the term in the document. The document-term matrix is a crucial component in many Natural Language Processing (NLP) and text mining tasks, such as topic modeling, sentiment analysis, and information retrieval.
| Term/Document | d1 | d2 | d3 | d4 | d5 | d6 | d7 | d8 |
| ------------- | -- | -- | -- | -- | -- | -- | -- | -- |
| a             | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| above         | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| always        | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| and           | 0  | 1  | 0  | 1  | 0  | 1  | 0  | 0  |
| at            | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| be            | 0  | 0  | 1  | 1  | 0  | 0  | 0  | 0  |
| begin         | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| better        | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| busy          | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  |
| but           | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| by            | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| cease         | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  |
| dogma         | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| doing         | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| don't         | 0  | 0  | 1  | 0  | 1  | 0  | 0  | 0  |
| else's        | 0  | 0  | 1  | 0  | 0  | 1  | 0  | 0  |
| enough        | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| every         | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| everyone      | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| face          | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| fail          | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| failure       | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| fall          | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| falling       | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| flavor        | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  |
| get           | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| glory         | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| goals         | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| greatest      | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| happens       | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  |
| happily       | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| have          | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| high          | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| if            | 0  | 0  | 0  | 1  | 1  | 1  | 0  | 0  |
| in            | 1  | 0  | 0  | 0  | 1  | 0  | 0  | 1  |
| is            | 0  | 1  | 1  | 0  | 0  | 0  | 1  | 1  |
| it            | 0  | 0  | 1  | 1  | 0  | 0  | 0  | 1  |
| it's          | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| lies          | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| life          | 0  | 0  | 1  | 1  | 1  | 0  | 1  | 1  |
| limited       | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| living        | 1  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| look          | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| making        | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  |
| mirror        | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| more          | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| never         | 1  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| not           | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| of            | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| other         | 0  | 0  | 1  | 0  | 0  | 0  | 1  | 0  |
| passes        | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| people's      | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| plans         | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  |
| predictable   | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  |
| quit          | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| remember      | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| results       | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| ridiculously  | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| rising        | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| set           | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| so            | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| someone       | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| started       | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| success       | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| talking       | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| the           | 1  | 1  | 1  | 0  | 0  | 0  | 0  | 1  |
| thinking      | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| time          | 1  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| to            | 0  | 1  | 0  | 1  | 0  | 0  | 0  | 0  |
| today's       | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| tomorrow's    | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| trapped       | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| viewed        | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| waste         | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| way           | 0  | 1  | 0  | 0  | 0  | 0  | 0  | 0  |
| we            | 1  | 0  | 0  | 0  | 0  | 0  | 0  | 0  |
| were          | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  |
| what          | 0  | 0  | 0  | 0  | 1  | 0  | 1  | 0  |
| whatever      | 0  | 0  | 0  | 0  | 0  | 0  | 0  | 1  |
| when          | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  |
| which         | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| will          | 0  | 0  | 0  | 0  | 0  | 1  | 0  | 0  |
| with          | 0  | 0  | 1  | 0  | 0  | 0  | 0  | 0  |
| without       | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  |
| would         | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0  |
| you           | 0  | 0  | 0  | 0  | 1  | 1  | 0  | 1  |
| you'll        | 0  | 0  | 0  | 0  | 1  | 0  | 0  | 0  |
| you're        | 0  | 0  | 0  | 0  | 0  | 0  | 1  | 0  |
| your          | 0  | 0  | 1  | 0  | 0  | 1  | 0  | 0  |

## Inverted Index
An inverted index is a data structure used to efficiently retrieve a set of documents that contain a given search term or keyword. It is essentially an index data structure that maps each unique term or word in a document collection to the set of documents that contain that term.

In an inverted index, each term is associated with a list of documents (or document IDs) that contain that term. The index is usually constructed by first tokenizing and normalizing the text in each document, and then creating an entry in the index for each unique term that appears in the document collection.

The inverted index is widely used in information retrieval systems such as search engines, where it helps to quickly identify relevant documents for a given query. Instead of searching through every document in the collection, the search engine can use the inverted index to retrieve a smaller subset of documents that contain the query terms, and then rank them based on their relevance.

a [6]

above [6]

always [5]

and [2, 4, 6]

at [5]

be [3, 4]

begin [2]

better [8]

busy [7]

but [1]

by [3]

cease [4]

dogma [3]

doing [2]

don’t [3, 5]

else’s [3, 6]

enough [5]

every [1]

everyone [6]

face [8]

fail [6]

failure [6]

fall [1]

falling [1]

flavor [4]

get [2]

glory [1]

goals [6]

greatest [1]

happens [7]

happily [8]

have [5]

high [6]

if [4, 5, 6]

in [1, 5, 8]

is [2, 3, 7, 8]

it [3, 4, 8]

it’s [6]

lies [1]

life [3, 4, 5, 7, 8]

limited [3]

living [1, 3]

look [5]

making [7]

mirror [8]

more [5]

never [1, 5]

not [1]

of [3]

other [3, 7]

passes [8]

people [3]

plans [7]

predictable [4]

quit [2]

remember [8]

results [3]

ridiculously [6]

rising [1]

set [6]

so [3]

someone [3]

started [2]

success [6]

talking [2]

the [1, 2, 3, 8]

thinking [3]

time [1, 3]

to [2, 4]

today’s [8]

tomorrow’s [8]

trapped [3]

viewed [8]

waste [3]

way [2]

we [1]

were [4]

what [5, 7]

whatever [8]

when [7]

which [3]

will [6]

with [3]

without [4]

would [4]

you [5, 6, 8]

you’ll [5]

you’re [7]

your [3, 6]

## Queries:

- **q1:** `Life AND Long`

    Life -> [3, 4, 5, 7, 8]
    
    Long -> None

    **result: None**

- **q2:** `Life OR Happy`

    Life -> [3, 4, 5, 7, 8]
    
    Happy -> None

    **result: d3, d4, d5, d7, d8**

- **q3:** `Life AND( Failure OR Success) AND (you OR Your)`
    
    Life -> [3, 4, 5, 7, 8]
    
    Failure -> [6]
    
    Success -> [6]

    you -> [5, 6, 8]

    Your -> [3, 6]

    **result: None**

- **q4:** ‍‍‍`Life AND NOT(time OR talking)`

    Life -> [3, 4, 5, 7, 8]

    time -> [1, 3]

    talking -> [3]

    **result: d4, d5, d7, d8**


