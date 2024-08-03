# chat-bot
def chatbot_response(user_input):
    responses = {
        "hi": "Hello! How can I help you today?",
        "how are you": "I'm just a bot, but I'm doing great! How about you?",
        "what's your name": "I'm a simple chat bot. You can call me ChatBot!",
        "bye": "Goodbye! Have a great day!"
    }
    
    # Convert user input to lowercase to handle case-insensitivity
    user_input = user_input.lower()
    
    return responses.get(user_input, "Sorry, I didn't understand that.")

# Main loop
print("ChatBot: Hello! Type 'bye' to end the conversation.")
while True:
    user_input = input("You: ")
    response = chatbot_response(user_input)
    print(f"ChatBot: {response}")
    if user_input.lower() == "bye":
        break
