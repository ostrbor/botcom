botcom
=========

Command bus design pattern for bot communication.

>>> pip install botcom

USE CASE:

commands.py
from botcom import Command, CommandHandler


class PingCommand(Command):
    def __init__(self):
        pass


class PingCommandHandler(CommandHandler):
    def handle(self, command):
        return 'pong'

Client sends command.
Server recieves command and execute it's handler with:
from botcom import Bus

bus = Bus()
result = bus.execute(cmd)
