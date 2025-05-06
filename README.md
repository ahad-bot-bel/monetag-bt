import telebot

API_TOKEN = '7403803789:AAGOmTkiNkFBhOv8EAkRK94haiixy84_b44'
bot = telebot.TeleBot(API_TOKEN)

ad_link = "https://sawutser.top/4/9300861"

@bot.message_handler(commands=['start'])
def send_welcome(message):
    welcome_text = (
        "স্বাগতম আমাদের বটে!\n\n"
        "আপনার জন্য একটি স্পেশাল অফার:\n"
        f"{ad_link}\n\n"
        "আরও অফার পেতে আমাদের সাথে থাকুন।"
    )
    bot.send_message(message.chat.id, welcome_text)

bot.polling()
