# Code_Alpha_ChatBot
import nltk
from nltk.chat.util import Chat, reflections


nltk.download('punkt')


pairs = [
    [
        r"my name is (.*)",
        ["Hello %1, how can I help you today?",]
    ],
    [
        r"hi|hello|hey",
        ["Hello!", "Hey there!", "Hi!",]
    ],
    [
        r"what is your name?",
        ["I am a chatbot created by Veeresh. You can call me Chatbot.",]
    ],
    [
        r"how are you?",
        ["I'm just a bunch of code, but thanks for asking! How can I assist you?",]
    ]
    [
        r"quit",
        ["Bye! Take care.",]
    ],
]


chatbot = Chat(pairs, reflections)

print("Hi! I am a chatbot. Type 'quit' to exit.")
chatbot.converse()
