# my-work
my work in python
import random, string  
save=[]  
adjectives = ['смешных', 'полосатых', 'маленьких', 'хрустальных', 'черных', 'радостных', 'медленных', 'фиолетовых']  
nouns = ['слонов', 'бегемотов', 'крокодилов', 'обезьян', 'драконов', 'котиков', 'единорогов', 'пегасов', 'лягушек']  
verbs = ['бегут', 'летят', 'прыгают', 'читают', 'хрюкают'] 
while True: 
    print("{🔷🔹==========================🔹🔷}") 
    print('Вас привествует генератор паролей!\nвыберите команду: \n1) сгенерировать пароль\n2) сохранить пароль\n3) сохраненные пароли')  
    print("|🔷🔹___________( )____________🔹🔷|") 
    choose=int(input("🔹♦️Введите команду♦️🔹: ")) 
    if choose==1:  
        N = int(input("🔹♦️сколько паролей потребуется♦️🔹?: "))  
        for i in range(N):  
            verb = random.choice(verbs)  
            noun = random.choice(nouns)  
            adjective = random.choice(adjectives)  
            number = str(random.randrange(2, 100))  
            symbol = random.choice(string.punctuation)  
            password = number + adjective + noun + verb + symbol  
            print('🔹♦️новый пароль♦️🔹: ' + password) 
        print("{🔴🔹==========================🔹🔴}")  
        print("🔹♦️не забудьте скопировать пароль♦️🔹") 
        print("|🔴🔹___________( )____________🔹🔴|")  
    elif choose==2:  
        s=input("🔹♦️какой пароль хотите сохранить♦️🔹?:")  
        save.append(s)  
        print("🔹♦️сохранен♦️🔹✅!")  
    elif choose==3:  
        result=str()  
        for i in range(0,len(save)):  
            result=result+f"{i+1}. "+save[i]+"\n"  
        print (result)