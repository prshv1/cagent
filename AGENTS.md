# DO NOT TOUCH
Nvr edit any files that are meant to for humans to read. I am not talking abt the actual code files, coz yeah some humans may read them but they are meant for computers to read. I am talking abt files like readme, documentation, etc. 

# Philosophy
Try to keep this project as light weight as possible, coz there will be many docker instances of this running on AWS. if you can get something more effeciently (while maintaing a good codebase), chose that way. But this shld also work locally (on linux/macos), coz that's where i will test this before deploying it.

# Abt the project
I am making a solution for avg joe, to take advantage of AI Agents. You can think of this as concierge for everyone. this shld be as simple for the consumer as possible. Like they can just say "find me a restraunt for my son's bday, and book a apointment at 6" they shld be able to do. this is just one use case to explain what the project is abt, but there is way more it shld be ablt to do it. 

# Architechture
all the files related to harness shld be in ./harness, all tools shld be in ./tools. The harness shld be a simple agents loop, nothing complex. System prompt shld have all the information abt the tool available and all. We will use a deepseek harness like aproach, where the harness is just a loop and everything else is a tool call. but unlike deepseek harness, the harness shld be ultra light, and all error handling & edge case handling shld be handled tool side. 
The tools will be deployed seperatly, the harness will be deployed separetly. This is for efficiency, tools will be like API calls for the harness. 