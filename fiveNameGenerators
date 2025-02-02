import random


first_syllable = ["mer"]
second_syllable_male = ["liano"]
second_syllable_female = ["iti"]
name_gender = [1,2]

def makeNameBySyllableGenderedEnding(number):

    generations = 0
    final_names = []
    while generations < number:
        gender = random.choice(name_gender)
        generations = generations + 1
        if gender == 1:
            first = random.choice(first_syllable)
            second = random.choice(second_syllable_male)
            name = first.capitalize() + second + " (M)"
            final_names.append(name)
        if gender == 2:
            first = random.choice(first_syllable)
            second = random.choice(second_syllable_female)
            name = first.capitalize() + second + " (F)"
            final_names.append(name)
    
    return(final_names)



female_start = ["mek"]
male_start = ["men"]
internal_stem = ["ou"]
ending = ["non"]


def makeNameBySyllableGenderedStart (number):
    counter = 0
    final_names = []
    while counter < number:
        counter = counter + 1
        nameType = random.randint(0,3)
        #0 = femme, 1 = masc
        #2 = fem with stem, 3 = masc with stem
        if nameType == 0:
            name = random.choice(female_start).capitalize() + random.choice(ending) + " (F)"
            final_names.append(name)
        if nameType == 1:
            name = random.choice(male_start).capitalize() + random.choice(ending) + " (M)"
            final_names.append(name)
        if nameType == 2:
            name = random.choice(female_start).capitalize() + random.choice(internal_stem) + random.choice(ending) + " (F)"
            final_names.append(name)
        else:
            name = random.choice(male_start).capitalize() + random.choice(internal_stem) + random.choice(ending) + " (M)"
            final_names.append(name)

    return(final_names)

vowel = ["a"]
start_cons = ["ph"]
middle_cons = ["q"]
end_cons = ["b"]

def makeNameByLetters(number):
    generations = 0
    final_names = []
    while generations < number:
        generations = generations + 1
        nameType = random.randint(0,5)
        
        if nameType == 0:
            #CVCVC
            name  = random.choice(start_cons) + random.choice(vowel) + random.choice(middle_cons) + random.choice(vowel) + random.choice(end_cons)
            
        if nameType == 1:
            #VCVCV
            name = random.choice(vowel) + random.choice(middle_cons) + random.choice(vowel) + random.choice(middle_cons) + random.choice(vowel)

        if nameType == 2:
            #CVC
            name  = random.choice(start_cons) + random.choice(vowel) + random.choice(end_cons) 
        if nameType == 3:
            #VCV
            name = random.choice(vowel) + random.choice(middle_cons) + random.choice(vowel)

        if nameType == 4:
            #VCCV
            name = random.choice(vowel) + random.choice(middle_cons) + random.choice(middle_cons) + random.choice(vowel)

        else:
            #CCVC
            name  = random.choice(start_cons) + random.choice(middle_cons) + random.choice(vowel) + random.choice(end_cons) 
        
        final_names.append(name.capitalize())
    return(final_names)


complex_vowel = ["a"]
complex_end_vowel = ["a"]
complex_starter_vowel = ["a"]
complex_first_cons = ["r"]
complex_end_cons = ["r"]
complex_inner_cons = ["z"]
numbers = [1,1,1,1,1,5,5,5,5,2,3,4,5,6,7,8,9,10]
#1 CVVC: Daien 
#2 VCCV: Enzo
#3 CVCCV: Dorrae
#4 VCCVC: Aithen

def makeComplexNameByLetter(number):

    generations = 0
    all_names = []
    while generations < number:

        generations = generations + 1
        type_of_name = random.choice(numbers)
        if type_of_name <4:
            #CVVC Daien
            first = random.choice(complex_first_cons)
            second = random.choice(complex_vowel)
            third = random.choice(complex_end_vowel)
            fourth = random.choice(complex_end_cons)
            if second[-1] == third[0]:
                name = first.capitalize() + second + "'" + third + fourth
            else:
                name = first.capitalize() + second + third + fourth
            
            all_names.append(name)

        if type_of_name < 8:
            #VCCV Enzo
            second = random.choice(complex_inner_cons)
            first = random.choice(complex_starter_vowel)
            fourth = random.choice(complex_end_vowel)
            third = random.choice(complex_end_cons)
            if second[-1] == third[0]:
                name = first.capitalize() + second + "'" + third + fourth
            else:
                name = first.capitalize() + second + third + fourth
            all_names.append(name)

        if type_of_name == 9 or type_of_name == 8:
            #CVCCV: Dorrae
            first = random.choice(complex_first_cons)
            second = random.choice(complex_vowel)
            third = random.choice(complex_inner_cons)
            fourth = random.choice(complex_inner_cons)
            fifth = random.choice(complex_vowel)
            if second[-1] == third[0]:
                name = first.capitalize() + second + "'" + third + fourth + fifth
            else:
                name = first.capitalize() + second + third + fourth + fifth
            all_names.append(name)

        if type_of_name == 10:
            #VCCVC: Aithen
            second = random.choice(complex_inner_cons)
            first = random.choice(complex_starter_vowel)
            fourth = random.choice(complex_end_vowel)
            third = random.choice(complex_end_cons)
            fifth = random.choice(complex_end_cons)
            if second[-1] == third[0]:
                name = first.capitalize() + second + "'" + third + fourth + fifth
            else:
                name = first.capitalize() + second + third + fourth + fifth
            all_names.append(name)

    return(all_names)

#One syllable name - Two syllable name
#CVCC or VCC
#e.g., Alf - Laegir 
#vowel circle, go to the next vowel, then a closing vowel
#adding the funky name generator just to show some fun things that python can let you do

funky_vowel = ["a","e","ai","ei","ú","i","u","ü","ör","a","e","ai","i","u","a","e","ai","i","u"]
funky_onset = ["nj","kh","z","t","s","n","v","y","p","th","fr","sk","sv","r","nj","bj",
             "l","j","k","hr","g","gr","fj","fr","br"]
funky_coda = ["lf","lv","ngr","sk","ld","rf","lv","bv","mb","dr","kr","mb","md","rl",
            "rn","nk","nkh","nts","drs","tg","ng","rg","nz","nt","nb","lg","lg",]
funky_ending = ["dingr","dumr","dun","dum","dal","vir","var","gir","er","on","ja","ya",
              "angdr","da","ra","ni","ki","in","en","an","nar","nir","ner","nic","var","gar","vir","ga","fa","fja","mund",
              "di","gor","yra","yr","dis","tan","nai","seg","yar","tar","taar","ne","tu","maa","gis","rir","rar","bir",
              "vaa","vön","dem","meg","tar","baatar","tulga","zorig","rel","relt","lan","ral","tseg",
              "üi","bayar","yuun","nai","ngo","dör","anga","yr","yra","hya","hja","jo"]


funky_name_type = [1,2,3,4]
#1 CV
#2 VC
#3 CV avante garde
#4 VC avante garde

def makeFunkyName(number):
    generations = 0
    final_names = []
    while generations < number:
        type = random.choice(funky_name_type)
        if type == 1:
            #CVCo-VEnd
            generations = generations + 1
            firstC = random.choice(funky_onset)
            firstV = random.choice(funky_vowel)
            firstCo = random.choice(funky_coda)
            secondC = random.choice(funky_onset)
            secondV = random.choice(funky_vowel)
            firstEnd = random.choice(funky_ending)
            name = firstC.capitalize() + firstV + firstCo + "-" + firstV.capitalize() + firstEnd 
            final_names.append(name)
        if type == 2:
            #VCo-CVEnd
            generations = generations + 1
            firstC = random.choice(funky_onset)
            firstV = random.choice(funky_vowel)
            firstCo = random.choice(funky_coda)
            secondC = firstC[0]
            secondV = random.choice(funky_vowel)
            firstEnd = random.choice(funky_ending)
            name = firstV.capitalize() + firstCo + "-" + secondC.capitalize() + firstV + firstEnd 
            final_names.append(name)
        if type == 3:
            #CVCo-VEnd
            generations = generations + 1
            firstC = random.choice(funky_onset)
            firstV = random.choice(funky_vowel)
            firstCo = random.choice(funky_coda)
            secondC = random.choice(funky_onset)
            secondV = random.choice(funky_vowel)
            firstEnd = random.choice(funky_ending)
            name = firstC.capitalize() + firstV + firstCo + "-" + secondV.capitalize() + firstEnd 
            final_names.append(name)
        if type == 4:
            #VCo-CVEnd
            generations = generations + 1
            firstC = random.choice(funky_onset)
            firstV = random.choice(funky_vowel)
            firstCo = random.choice(funky_coda)
            secondC = firstC[0]
            secondV = random.choice(funky_vowel)
            firstEnd = random.choice(funky_ending)
            name = firstV.capitalize() + firstCo + "-" + secondC.capitalize() + secondV + firstEnd 
            final_names.append(name)

    
    return(final_names)






#print(makeNameBySyllableGenderedEnding(40))
#print(makeNameBySyllableGenderedStart(40))
#print(makeNameByLetters(40))
#print(makeComplexNameByLetter(40))
#print(makeFunkyName(40))
