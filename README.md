ef chatbot_response(user_input):
    user_input = user_input.lower()
    
    if "hello" in user_input or "hi" in user_input:
        return "Hello! How can I assist you today?"
    
    elif "who are you" in user_input or "what are you" in user_input:
        return "I am a rule-based chatbot created to assist you with simple queries."
    
    elif "time" in user_input:
        from datetime import datetime
        now = datetime.now()
        current_time = now.strftime("%H:%M:%S")
        return f"The current time is {current_time}."
    
    elif "help" in user_input:
        return "Sure! How can I help you? You can ask me about the time, date, or basic information."
    
    else:
        return "I'm sorry, I didn't understand that. Can you please rephrase your question?"

user_input = input("You: ")
response = chatbot_response(user_input)
print("Bot:", response)
