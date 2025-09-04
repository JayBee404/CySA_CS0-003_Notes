SMTP logs are typically formatted in request/response fashion
They will usually contain a few key pieces of information such as:
- Time of request/response
- Address of recipient
- Size of message
- Status Code

Code 220 - Indicates the server is ready
Code 250 - Indicates the message is accepted
Code 421 - Indicates the service is not available
Code 450 - Indicates that the server can not access the mailbox to deliver a message
Code 451 - Indicates the local server aborted the action due to a processing error
Code 452 - Indicates the local server has insufficient storage space available
