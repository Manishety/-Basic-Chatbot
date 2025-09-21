def get_response(user_input):
    """
    This function processes the user's input and returns a predefined response.
    The input is converted to lowercase to make the chatbot case-insensitive.
    """
    user_input = user_input.lower()

    if "hello" in user_input:
        return "Hi there!"
    elif "how are you" in user_input:
        return "I'm a bot, so I'm always doing great! Thanks for asking."
    elif "bye" in user_input or "goodbye" in user_input:
        return "Goodbye! Have a great day."
    else:
        return "I'm sorry, I don't understand that. Can you rephrase?"

def main_chatbot():
    """
    This is the main loop that runs the chatbot.
    """
    print("🤖 Simple Chatbot: Hi! I'm a simple chatbot. Type 'bye' or 'goodbye' to exit.")

    while True:
        user_message = input("You: ")
        
        # Check if the user wants to exit
        if user_message.lower() in ["bye", "goodbye"]:
            print(f"Chatbot: {get_response(user_message)}")
            break  # Exit the loop

        # Get and print the chatbot's response
        response = get_response(user_message)
        print(f"Chatbot: {response}")

# Run the chatbot
if __name__ == "__main__":
    main_chatbot()
