EnhancedDiscordChatExporterPy
=====================

|version| |license| |language|

.. |license| image:: https://img.shields.io/pypi/l/enhanced-chat-exporter

.. |version| image:: https://img.shields.io/pypi/v/enhanced-chat-exporter

.. |language| image:: https://img.shields.io/github/languages/top/ChickenDevs/EnhancedDiscordChatExporterPy

EnhancedDiscordChatExporterPy is a Python plugin for your discord.py bot, allowing you to export a discord channels history within a guild.

Installing
----------
To install the library to your bot, run the command:

.. code:: sh

    pip install enhanced-chat-exporter

To install the repository, run the command:

.. code:: sh

    git clone https://github.com/ChickenDevs/EnhancedDiscordChatExporterPy

Usage
-----
.. code:: py
    
    import discord
    import enhanced_chat_exporter
    from discord.ext import commands
    
    bot = commands.Bot(command_prefix="!")
    
    
    @bot.event
    async def on_ready():
        print("Live: " + bot.user.name)
    
    
    @bot.command()
    async def save(ctx):
        channel = discord.utils.get(ctx.guild.channels, name="logs")
        await enhanced_chat_exporter.export(ctx, channel)  # channel is optional, if not used, it will send into the current channel
    
    if __name__ == "__main__":
        bot.run("BOT_TOKEN_HERE")

*Optional: If you want the transcript to display Members (Role) Colours then enable the Members Intent.*

Screenshots
-----------

.. image:: https://raw.githubusercontent.com/ChickenDevs/EnhancedDiscordChatExporterPy/master/.screenshots/channel_output.png

.. image:: https://raw.githubusercontent.com/ChickenDevs/EnhancedDiscordChatExporterPy/master/.screenshots/html_output.png

Links
-----
- `Wiki <https://github.com/ChickenDevs/EnhancedDiscordChatExporterPy/wiki/>`_
