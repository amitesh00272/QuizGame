# QuizGame
This game is only for entertainment
class QuizGame():
    def __init__(self,questions,option):
        self.question = questions
        self.option = option
        self.answers = ('a','b')

    def showResult(self):
        print(self.question[0])
        option = self.option
        answer = self.answers
        for i in option[0]:
            print(i)

        choice = input('Enter your answer: ')
        if choice == answer[0] or choice == 'A':
            
            print('You are Correct!!\n')
            print(self.question[1])
            option = self.option
            answer = self.answers
            for i in option[1]:
                print(i)

            choice = input('Enter your answer: ')
            if choice == answer[1] or choice == 'B':
                print('You are correct!!')
                print('You won this match!!!')
                quit()

            else:
                print('You are Incorrect!!')
                quit()

        else:
            print('You are Incorrect!!')
            quit()


result = QuizGame(['1.Who is the first prime minister of India?','2.Which is the hardest programming lnguage?'],[['A.Narendra Modi','B.Pt JawharLal Nehru','C.None Of Them'],['A.Python','B.Java','C.Kotlin']])


result.showResult()
