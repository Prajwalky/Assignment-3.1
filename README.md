View(USArrests)

names(USArrests) #to get the column names 

US_States<-rownames(USArrests) # to get the row names, i.e the USA states

US_States

b<-gsub("[^aeiouAEIOU]","C",US_States)#is basically "if not any of 'aeiouAEIOU' then 'C'

#if aeiouAEIOU is NOT in [], its a complete pattern.

# using ^ means, exclude what comes after this

b<-gsub("[^C]","V",b)# is "if not 'C', then 'V

b

library(stringr)

str_count(b,"V") #counts character in a string

sum(str_count(b,"V")) # adds the count of "V" i.e vowels

# 177 Vowels
