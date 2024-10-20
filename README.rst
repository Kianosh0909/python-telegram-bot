from telegram.ext import Updater, CommandHandler

def start(update, context):
    update.message.reply_text('سلام! به ربات فروش اکانت مجازی خوش آمدید.')

def main():
    updater = Updater("5903331028:AAGbym0medXI1Go42_Sd-EwMg4XLjcopAQQ", use_context=True)
    dp = updater.dispatcher

    dp.add_handler(CommandHandler("start", start))

    updater.start_polling()
    updater.idle()

if __name__ == '__main__':
    main()
