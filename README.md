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
