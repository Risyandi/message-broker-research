# Topics in rabbitMQ with Go-lang
Messages sent to a topic exchange can't have an arbitrary routing_key - it must be a list of words, delimited by dots. The words can be anything, but usually they specify some features connected to the message.  

A few valid routing key examples: *"stock.usd.nyse"*, *"nyse.vmw"*, *"quick.orange.rabbit"*. There can be as many words in the routing key as you like, up to the limit of 255 bytes.

To receive all the logs:  
`go run receive_logs_topic.go "#"`  

To receive all logs from the facility **"kern"**:  
`go run receive_logs_topic.go "kern.*"`  

Or if you want to hear only about **"critical"** logs:  
`go run receive_logs_topic.go "*.critical"`  

You can create multiple bindings:  
`go run receive_logs_topic.go "kern.*" "*.critical"`  

And to emit a log with a routing key **"kern.critical"** type:  
`go run emit_log_topic.go "kern.critical" "A critical kernel error"`