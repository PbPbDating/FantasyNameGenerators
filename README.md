# FantasyNameGenerators
Python code to generate fantasy names

The .py file contains the building blocks to make 5 types of names. First, I will explain how to use the generator. Then, I will explain the types of names.  Finally, I am bad at spelling and github has no spellcheck, so... sorry.

Keep in mind when using the name generators, I usually generate 40 names at once and pick one or two - not every name makes sense or sounds nice, so it is useful to generate a lot. As you discover name types you don't like, edit your code, such as by removing a vowel or chunk you don't like. 


****--------HOW TO USE THE NAME GENERATOR--------****
There are two steps to using this generator:
1) Add your chunks, vowels, and consonants to the specific generator you want to use
2) delete the '#' before the relevant print statement at the bottom

For more clarity on 1.
Pick the name generator you want to use (detailed descriptions below). Right before the "def" statement, you will see that I have defined a bunch of lists. You can tell because it will look like this: 

first_syllable = ["mer"]
second_syllable_male = ["liano"]
second_syllable_female = ["iti"]
where there is a name, then an =, then some of these guys []

This is where the bulk of your work will be. I have left in strings only as examples. For the name generator to work, you need to fill out those lists. When you fill them out, be sure to always put your string in quotes and have a comma after. A final list might look like:

internal_stem = ["ou","ma","a","e","i","o","ä","an","en","in","on","än","am","em","im","om","äm","ik","nin","nim","min","mil","mik","mal","mak","mel","mek","men","man","mar","mer","jo","ja","je","ji","jä","jaz","jäz","jen","jan","tis","sat"]

Note: there is no comma after the last string.

I include recommendations for adding syllabels in the descriptions of each generator below. 

For more clarity on 2:
After you pick which generator you are using and have added everything to the lists, scroll down to the bottom. You will see five lines of code that each begin with "print." Delete the # before the relevant line. If you are making names by syllables with gendered endings, then remove the # before #print(makeNameBySyllableGenderedEnding(40))

You can also change the number 40 to be however many names you want to generate. I recommend starting with at least 24 so you get enough.

It is useful to iterate a few times after creation. Make some names and see which you like and don't like. Maybe there is a certain syllable, vowel, or ending that you can remove from your lists to make better names.

****--------Types of Name Generator--------****

----makeNameBySyllableGenderedEnding----
This name generator produces gendered names by mashing a first syllable with a gendered second syllable. Depending on the types of syllables you use, you can get names of more than two syllables, e.g., if one of your syllables is "alia". Think of the final name as:

first_syllable + gendered_second_syllable

To make names here, I often go to behind the names and pick a few relevant cultures of names to view. I then chunk them. If the name is adelard, I add "ade" to the first_syllable list and "lard" to the second_syllable_male list. After doing this with 100+ names, you can begin bashing names together. If you don't want to use behind the names, you can do the same by simply generating the types of endings you want manually or by starting with a list of existing character names and 'chunking' them. 


----makeNameBySyllableGenderedStart----
This name generator produces gendered names by the first syllable and is very similar to the previous one. This generator also has the option to add an internal stem, which is just something placed into the middle of a name to make the name more unique and longer. 

The final name types are:

gendered_first_syllable + second_syllable
gendered_first_syllable + internal_stem + second_syllable

My recommendation is to generate the chunks as I suggest above (e.g., behind the name, using names that you've already created for your world and chunking them). For internal stems, I recommend keeping them short, just consonant + vowel. I recommend making them end with a vowel so they are more likely to 'flow' with the ending syllable. If all your ending syllables start with vowels, of course then end the internal stem with a consonant, or mix it up.


----makeNameByLetters----
This name generator builds names letter by letter. Specifically, it builds using a starter_cons, a vowel, a middle_cons, and an end_cons (where cons = consonant). This allows you to have blended consonants that only appear at the start of a name, like 'Fr' or 'Shp' and those that only appear in the middle or end. It does not allow you to specify where certain vowels should appear.

From that, it makes 6 types of names, as defined by where the vowels and consonants appear:

CVCVC
VCVCV
CVC
VCV
VCCV
CCVC

This name generator is for someone who knows the types of sounds they want in their names and is quite customizeable. If you don't like a name like Sveirl because of the 'rl' at the end, simply remove 'rl' from end_cons.

Note: Vowels do not need to be a, e, i, o, u - include vowel groups like ei or ai if they fit your culture's naming schemes.


----makeComplexNameByLetter----
This generator is a slightly more complex version of the previous. Instead of using the same types of vowels in every part of the word, it includes generic vowels, starter vowels, and ending vowels. You could decide that 'ei' can appear inside a name but that a name cannot start or end with 'ei' for instance. This generator also checks if two of the same vowel appear in a row and adds a ' to break them up.

It can create four types of names:

CVVC
VCCV
CVCCV
VCCVC


----makeFunkyName----
This name generator is included just to show a bit of what you can do once you know python. My goal was to make a 'vowel circle' so the second vowel in the name is based on the first vowel but not the same. 

This generator produces names like Alf-Laegir according to 2 structures:

CVCo-Vend
VCo-CVEnd

(where Co = Coda, or the end of a syllable)

This name generator is quite culturally specific, which is why I've left in the original strings with vowels, codas, etc. I don't anticipate anyone else actually using this, but thought it was fun to include to show how you can really get into the rules of your world and start building specific names. 




Happy generating!




