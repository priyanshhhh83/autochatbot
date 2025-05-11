# autochatbot
# bot.py

import time

def bot_response(user_input):
    user_input = user_input.lower()

    if "hello" in user_input or "hi" in user_input:
        return "Hello! How can I help you today?"
    elif "how are you" in user_input:
        return "I'm just a bot, but I'm functioning as expected!"
    elif "bye" in user_input:
        return "Goodbye! Have a great day!"
    else:
        return "I'm not sure how to respond to that."

def chat():
    print("AutoChat Bot 🤖: Type 'bye' to exit the chat.")
    time.sleep(1)

    while True:
        user_input = input("You: ")
        response = bot_response(user_input)
        print("Bot:", response)

        if "bye" in user_input.lower():
            break

if __name__ == "__main__":
    chat()
