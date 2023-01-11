# Routing in rabbitMQ with Go-lang
In this tutorial we're going to add a feature to it - we're going to make it possible to subscribe only to a subset of the messages.

For example, we will be able to direct only critical error messages to the log file (to save disk space), while still being able to print all of the log messages on the console.

- Bindings
- Direct Exhange
- Multiple Bindings
- Emiting Logs
- Subscribing
