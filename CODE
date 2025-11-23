import time
import random

#Examples of setences
def get_sentence():
    sentences = [
        "The quick brown fox jumps over the lazy dog.",
        "Python is a great language for first year engineering students.",
        "Coding is not just about syntax, it is about logic.",
        "Is artificial intelligence less than our intelligence?",
        "Artificial Intelligence is the future of technology."
    ]
    return random.choice(sentences)

# Standard formula: (number of characters / 5) / (time in minutes)
def calculate_wpm(time_taken, typed_text):
    num_chars = len(typed_text)
    wpm = (num_chars / 5) / (time_taken / 60)
    return round(wpm, 2)

# Compare characters one by one up to the length of the shorter string
def calculate_accuracy(original, typed):
    count = 0
    min_len = min(len(original), len(typed))
    
    for i in range(min_len):
        if original[i] == typed[i]:
            count += 1
            
    accuracy = (count / len(original)) * 100
    return round(accuracy, 2)

def run_test():
    print("--- PYTHON TYPING SPEED TESTER ---")
    target_text = get_sentence()
    
    print("\nType the following sentence accurately:")
    print(f"Reference: '{target_text}'")
    
    input("\nPress ENTER to start...")
    
    start_time = time.time()
    user_input = input("Type here: ")
    end_time = time.time()
    
    time_taken = end_time - start_time
    wpm = calculate_wpm(time_taken, user_input)
    accuracy = calculate_accuracy(target_text, user_input)
    
    #Print all the results
    print("\n--- RESULTS ---")
    print(f"Time Taken: {round(time_taken, 2)} seconds")
    print(f"Typing Speed: {wpm} WPM")
    print(f"Accuracy: {accuracy}%")

if __name__ == "__main__":
    run_test()
    
