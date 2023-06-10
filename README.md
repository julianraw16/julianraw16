- 👋 Hi, I’m @julianraw16
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
julianraw16/julianraw16 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import discord
from discord.ext import commands
import os
import random

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='$', intents=intents)

# Dan inilah cara Kamu mengganti nama file dari variabel!

@bot.event
async def on_ready():
    print(f'We have logged in as {bot.user}')

@bot.command()
async def hello(ctx):
    await ctx.send(f'Hi! I am a bot {bot.user}!')

organik = ["daun","sayur","kulit pisang"]
anorganik = ["plastik","besi","kabel"]

@bot.command()
async def pilih(ctx, sampah):
    if sampah in organik:
        await ctx.send("Masukkan dalam sampah organik")
    elif sampah in anorganik:
        await ctx.send("Masukkan dalam sampah anorganik")

bot.run("MTEwNjgwNTE4NjA1NzQ5MDQ5Mg.GsxHzM.VZXMNvCIjeh4wM8-yBpcj93D14NCTc5ZYVfC-o")

