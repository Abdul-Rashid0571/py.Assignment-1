+ #!/usr/bin/env python3
+ # -*- coding: utf-8 -*-
+ """
+ Simple Personal Assistant - Input/Output Project
+ Prompt the user for the personal iformation, summarizes it, and optionally save it.
+ """

+ import random

+ def get_user_data():
+ # Required questions (always asked)
+ required_questions = [
+ ("name", "what is yourname? "),
+ ("age", "How old are you? ")
+ ]

+ #Fun optional questions to randomize
+ optional_questions = [
+ ("color", "What is your favorite color? "),
+ ("food", "What is your favorite food? "),
+ ("city", "Which city do you live in? "),
+ ("school", "Which SHS did you attend? "),
+ ("team", "What is your favorite soccer team? ")
+ ]
+ 
+ # Select 2 to 4 optional questions randomly
+ selected_optional = random.sample (optional_quetions, k=random.randint (2, 4))

+ # Combine required and selectednoption questions
+ all_questins = required_question + selected_optional
+ responses = {}

+ for key, prompt in all_questions:
+ responses[Key] = input(prompt)

+ return responses

+ def display_summary(responses):
+ print("
+ ---Personlizeed Summary ---")
+ print(f"Hello, {responses.get('name', 'Friend')}!")

+ if 'age' in responses:
+ print(f"You are {responses['age']} years old, ", end=' ')
+ if 'color' in responses:
+ print(f"love the color { responses['color']},", end='')
+ if 'food' in responses:
+ print(f" and enjoy eating {responses['food' ]}.")
+ else:
+ print()
+ if 'city' in responses:
+ print(f"Life must be awesome in {responses['city']}!")
+ if 'school' in responses:
+ print(f"You went to {responses['school']}! SHS.")
+ if 'team' in responses:
+ print(f"Go {responses['team"]}!")

+ def save_to_file(responses, rating):
+ filename = f"{responses.get ('name', 'user')}.txt"
+ with open(filename,'w', encoding='utf-8')as f:
+ f.write("User Summary
+ ")
+ f.write("==========
+ ")
+ for key, value in responses.item()
+ f.write(f"{Key.capitalize()}:
+ ")
+ f.write(f"Rating: {rating}/5
+ ")
+ print(f"Summary saved to {filename}")

+ def main():
+ While True:
+ responses = get_user_data()
+ display_summary(responses)
+ 
+ save = input("
+ Do you want to save this summary? (yes/no): ").strip().lower()
+ if save == "yes":
+ While True:
+ try
+ rating = int(input ("Please rate
