import random

class QuizGame:
    def __init__(self, topic):
        self.topic = topic
        self.questions = []
        self.score = 0

    def load_quiz_questions(self):
        # Customize your questions here
        self.questions = [
            {
                'question': 'What is the capital of France?',
                'options': ['A. Berlin', 'B. Paris', 'C. Madrid'],
                'correct_answer': 'B'
            },
            {
                'question': 'Who wrote "Romeo and Juliet"?',
                'options': ['A. William Shakespeare', 'B. Jane Austen', 'C. Charles Dickens'],
                'correct_answer': 'A'
            },
            {
                'question': 'The largest planet in our solar system is?',
                'options': ['A. Earth', 'B. Jupiter', 'C. Mars'],
                'correct_answer': 'B'
            },
            {
                'question': 'The capital of Japan is?',
                'options': ['A. Seoul', 'B. Tokyo', 'C. Beijing'],
                'correct_answer': 'B'
            },
            {
                'question': 'The currency of the United States is?',
                'options': ['A. Euro', 'B. Dollar', 'C. Yen'],
                'correct_answer': 'B'
            },
            {
                'question': 'The Python programming language gets its name from the TV show Monty Python\'s Flying Circus. (True/False)',
                'correct_answer': 'True'
            }
        ]

    def display_welcome_message(self):
        print(f"Welcome to the {self.topic} Quiz Game!")
        print("Rules: Answer the questions to the best of your knowledge.")
        print("You will be given multiple-choice questions and fill-in-the-blank questions.")

    def present_quiz_questions(self):
        for question in self.questions:
            print("\n" + question['question'])
            
            if 'options' in question:
                for option in question['options']:
                    print(option)
                user_answer = input("Your answer (enter the letter of your choice): ")
            else:
                user_answer = input("Your answer: ")

            self.evaluate_user_answer(user_answer, question['correct_answer'])

    def evaluate_user_answer(self, user_answer, correct_answer):
        if user_answer.upper() == correct_answer:
            print("Correct! Well done!")
            self.score += 1
        else:
            print(f"Incorrect. The correct answer is: {correct_answer}")

    def display_final_results(self):
        print("\nQuiz Completed!")
        print(f"Your final score is: {self.score}/{len(self.questions)}")

    def play_again(self):
        return input("Do you want to play again? (yes/no): ").lower() == 'yes'

def main():
    while True:
        topic = input("Enter the topic for the quiz game: ")
        quiz_game = QuizGame(topic)
        quiz_game.load_quiz_questions()
        quiz_game.display_welcome_message()
        quiz_game.present_quiz_questions()
        quiz_game.display_final_results()

        if not quiz_game.play_again():
            print("Thank you for playing. Goodbye!")
            break

if __name__ == "__main__":
    main()
