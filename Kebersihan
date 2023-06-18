import discord
from discord.ext import commands
import random, os

#Buat itents
intents = discord.Intents.default()
intents.message_content = True

#Kenalkan Bot-nya
bot = commands.Bot(command_prefix='$', intents=intents)

#Bot reaksi dan command untuk bot-nya 

@bot.event #agar bot bereaksi ketika ada sesuatu 
async def on_ready(): # ketika bot telah siap
    print(f'Bot Telah Siap!')

@bot.command()
async def idesampah(ctx):
    img_name = random.choice(os.listdir('Kerajinan'))
    with open(f'kerajinan/{img_name}','rb') as gambar: #membuka file gambar dan disimpan di variable 
        # Mari simpan file perpustakaan/library Discord yang dikonversi dalam variabel ini!
        picture = discord.File(gambar)
   # Kita kemudian dapat mengirim file ini sebagai tolok ukur!
    await ctx.send(picture) 

bot.run("")
