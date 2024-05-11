# ALittleStory 
python

with open ("story.txt" , "r") as f:
    story = f.read()

words = set()
start_of_word = -1

target_start = "<"
target_end = ">"

for i, char in enumerate(story):
    if char == target_start:
        start_of_word = i

    if char == target_end and start_of_word != -1:
        word = story[start_of_word: i + 1]
        words.add(word)
        start_of_word = -1

answers = {}

for word in words:
    answer = input("Enter a word for " + word + ": ")
    answers[word] = answer

for word in words:
    story = story.replace(word, answers[word])

print(story)


TXT FILE UNDER THE PROJECT

Once upon a time in a <place>, there was  <name> with the <name2>.
This <gender> had always dreamed of becoming a famous <occupation>.
One day, while walking through a <place>, <name> found a <color> <object> and decided to <analyze> it. 
The <relation> felt so <emotion> and <emotion2>. 
From that day on <name> and <name2> became known as a <occupation>. 
People from all over the <place> came to see the amazing <occupation> and hear its <famous> stories.
