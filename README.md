class Person:
    def _init_(self, name):
        self.name = name
        self.score = 0

    def ask_question(self, question):
        response = input(f"{question} (yes/no): ")
        if response.lower() in ['yes', 'y']:
            self.score += 1

questions = [
1. What type of parties or events do you find most enjoyable?
 2. Do you enjoy being the center of attention?
 3. Do you enjoy meeting new people?
 4. Do you feel energized in social situation?
 5. Do you prefer group activites over solo ones?
 6. Do yoy feel uncomfortable being alone for long period of time?
 7. Do you like to keep busy with social engagement or activites?
 8. Do you find it easy to start conversation with stangers?
 9. Do you feel happy when you are the one leading conversation or event?
 10. Do you feel energized after social interaction ?
 11. Do you tend to talk before thinking?
 12. Do you constantly seek out new people?
 13. Are you quick to make new friends?
 14. Do you feel more comfortable in quiet, peaceful places? 
15. Do you usually feel energized after attending a big party or social event?
 16. Do you tend to think things through before speaking?
 17. Do you often find yourself reflecting on your thoughts and feelings?
 18. Do you enjoy having deep, meaningful conversations with others?
 19. Do you tend to avoid small talk?
 20. Do you have a small, close-knit group of friends?
 21. Do you feel comfortable in a large social group? 
1. Do you feel comfortable in a large social group? 
2. Do you enjoy striking up conversations with new people? 
3. Do you find yourself more energized after spending time with others? 
4. Do you enjoy attending parties or social events? 
5. Do you often talk before fully thinking through your thoughts? 
6. Are you constantly on the lookout for opportunities to meet new people? 
7. Do you enjoy being the center of attention in social settings? 
8. Do you typically express your excitement or enthusiasm outwardly? 
9. Do you prefer group activities over spending time alone? 
10. Do you make new friends quickly?
]

def determine_personality(person):
    for question in questions:
        person.ask_question(question)
    
    if person.score >= 3:
        return "extrovert"
    else:
        return "introvert"

name = input("Enter your name: ")
person = Person(name)
personality = determine_personality(person)

print(f"{person.name}, you are an {personality}!")
