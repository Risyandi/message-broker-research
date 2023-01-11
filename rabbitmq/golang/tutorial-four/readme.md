# Routing in rabbitMQ with Go-lang
In this tutorial we're going to add a feature to it - we're going to make it possible to subscribe only to a subset of the messages.

For example, we will be able to direct only critical error messages to the log file (to save disk space), while still being able to print all of the log messages on the console.

- Bindings
- Direct Exhange
- Multiple Bindings
- Emiting Logs
- Subscribing

If you want to save only 'warning' and 'error' (and not 'info') log messages to a file, just open a console and type:  
`go run receive_logs_direct.go warning error > logs_from_rabbit.log`  
If you'd like to see all the log messages on your screen, open a new terminal and do:

`go run receive_logs_direct.go info warning error`  
output:    
`# => [*] Waiting for logs. To exit press CTRL+C`  

And, for example, to emit an error log message just type:

`go run emit_log_direct.go error "Run. Run. Or it will explode."`  
output:  
`# => [x] Sent 'error':'Run. Run. Or it will explode.'`
