Arthur
======

Arthur hopefully will understand Human Language some day. For now he is rather dull...


>Goal to create a tool or system of tools that better understand human language. 

## Why Do We Need Arthur?

I personally believe that the greatest limitation we have in Artificial Intelligence and also the next barrier we need in order to greatly increase the speed at which we can develop it is, "We can't really talk to it yet." This is no fault of its' own but a limition of both our understanding of language and an inferior application of the knowledge we have in current Natural Language Processing technologies and approaches. My philosophical approach to defending this statment involves a few theories I have either borrowed or thought up of on my own. The true measurement will come as tools are created and either agree or disagree with the theories, but it has been important for me to frame my thoughts about this.

 * The Beginning Laws of Artificial Intelligence
 * A Man, a Box, and a Machine - Theory
 * Forget about the Chinese Box, Let's Talk About Who Made It
 * The Limitations of Language
 
## What Will Arthur Do?

Well, plainly he will do whatever it takes to answer the question, "What will it take for a machine to understand language?", but because of the vagueness of what them means at the moment I find that to be more the direction I walk rather than a desitination I walk to. I hope that as I walk towards that I will need to make as few course corrections as possible, but realistically I think I will instead need to course correct many times in order to iterate through false assumptions I have. So a better question is "What will Arthur do first?"

## What will Arthur Do First?

This is where I feel like I had my first mental breakthrough. Every thing I thought of only brought up more questions and answered few others until I started reading and thinking about Morphemes. I will write more about that in the article "Morphemes, The simplest grammatical unit with no context dependency". Briefly, the more I have thought about langauge the more I have realized how relative it is. Everything takes two varibles into account, Context and Time. In different contexts the same words would mean different things, and in fact in different contexts the same word may have different grammatical rules. When I refer to Time I am refering to the Etymology or how a word or grammar rule changes overtime. 

You may shake or nod your head at that statment but the first breakthrough I had was that Morphemes are the only grammatical structure that only connected to Time. This doesn't mean that it doesn't have a contextual component necessarily but that it has only one Context, the language itself. Meaning you can essentially take that out of the equation as long as you assume you are working from within one language. Further if you work within on short time frame you can ignore for now the constraint of Time. 

The first step will be to create a tool that can simply correctly identify morphemes individually and also define if a word is possible in the current langauge in the context of time. It may seem a simple tool but will be the beginning of a machine being able to understand language, and the first step down a rabbithole I am eager to jump into.

(Also, I would need to talk to an experianced Entymologist but my assumption is that even though words can be created and changed fairly quickly the addition of new Morphemes in a language however is much slower. I think it is also based around when we create new technology or cultural beliefs that require new ways of communicating and those times have fluctuated throughout history but overall have happended in great spurts. Think of the Englightenment or of the rapid increase tody.)

#### Omnimorpheme

###### Goal

> To correctly learn what Morpheme's are from a large body of unnanotated text. Then to correctly identify if a Morpheme combination is possible based on the text it was given. 

This will not be a perfectly unsupervised approach, but I think this is because of the law that, "Nothing can learn a communicable language unsupervised". It will however be as hands off as possible by instead of telling it what to learn it will learn on it's own and we will tell it only things that can not be known outside of it's approach. A defense of this approach is also contained in "Morphemes, The simplest grammatical unit with no context dependency"

This is much simiplar to achieve than grammar as a whole because you can at first ignore the two constraints of grammar, Context and Time. I will note than in the interest of simplicity it will only look at one word morphemes. These can be bound or unbound. If "doghouse" was given in the body of text it would correctly identify that as a possible combination of morphemes, but it would not identify "dog house" as being a morpheme but would return True if both "dog" and "house" appeared in the text.

Steps:

1. Sanitize text into a list individual words.
2. Sanatize words into all possible combination of letters within a word
3. Take both of those sets and create a new data type of morpheme and tie each entry into a dictionary of when it appears.

At this point it can be tested but only to a limited point. "wihand" would be defined as a possible morpheme becaue the word "hand" could technically be combined with "wi" from without. This has no meaning of course but it is not possible for it to know this because it would require an understanding of meaning which it does not yet have. Also "relate" would be listed as possible combinations of the morphemes "re" and "late" and also independantly as "relate". We know that "relate" is itself its' own morpheme and not the comobination of different morphemes but you can only konw this through an understanding of meaning. If you gave it the word "qzrward" it should return false because "q" and "z" never appeard together in the body of text. Give it a string of words and it could tell you which of all of the words are possible. This is probably the most rudimentary grammar check possible, but also the most basic.

4. Teaching it which groups of morphemes are related

Before this step the "mis" in "misadventure, mistake, misalign" would be incorrectly identified in the same group as "mist". Technically it would be defined in the whole group as a possible morpheme or combination of morphemes. We know that these have different meanings and come from different words but you can't know that without a knowledge of the meaning so we would need to teach it that the first group of "mis" all come from the same morpheme.

**Notice**
There is a difference in the approach of giving it morphemes and having it find ones, and having it find all possible morphemes and teaching it which are related. A subtle but important difference. 

*** After this step I am less sure of how it will work because I am not sure what it will learn ***

5. With the knowledge of related morphemes it could give a probability of the existance of a word if it is given a word.
6. When given new text it should know which morphemes it has learned that have no connection to another morpheme or told it stands as its' own and needs to be taught.
