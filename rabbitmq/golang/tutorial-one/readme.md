# Simple process messages broker using rabbitMQ and Go-lang
1. Open your the terminal (command line, powershell, etc.)
2. Installing the package of `amqp` using command  
    ```go
    go get github.com/rabbitmq/amqp091-go
    ```
3. Open the terminal first for run the file `sender.go`
4. Open the terminal second for run the file `receiver.go`
5. Running both file together with running the command in the terminal :
    - fist terminal
    ```go
    go run sender.go
    ```
    
    - second terminal
    ```go
    go run receiver.go
    ```
## Command line result

![command line](./cmd-img-step.PNG)
(**images**: command line when running both file together)  

![check list queue](./cmd-check-listqueue.PNG)
(**images**: check list queue in rabbitmq)