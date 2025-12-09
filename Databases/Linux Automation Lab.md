# __**A detailed walkthrough of the Bash scripting challenge, covering file creation automation, permission management, and output sorting.**__


**The objective was to create a script that generates 25 distinct 
text files named sequentially (e.g., Neo1.txt, Neo2.txt...). 
This tests the ability to use loops and variables within a Bash shell environment.** 

•	Connect via SSH to EC2 Instance

•	Create working directory

•	Initialize script file


___

__Step 1: Connect to Your Linux Environment:__

- ssh ec2-user@<your-ec2-ip>

__Step 2: Create a Working Directory:__

- mkdir bash_challenge
- cd bash_challenge

__Step 3: Create Your Bash Script:__

- nano create_files.sh

<img width="607" height="386" alt="image" src="https://github.com/user-attachments/assets/a1e94170-6e02-4e86-b81b-881f547a4f58" />

---
__Step 4: Save and Exit:__

- Press CTRL+O to save, then CTRL+X to exit Nano.

__Step 5: Make the Script Executable:__

- chmod +x create_files.sh

__Step 6: Run the Script:__
- ./create_files.sh

<img width="604" height="886" alt="image" src="https://github.com/user-attachments/assets/65d89bef-3ee1-43f1-8e6e-04891e98c2df" />

___
__Step 7: Edit the Output:__
- With the use of the command ‘ls -lv’, it arranged the numbered files in chronological order.

<img width="603" height="127" alt="image" src="https://github.com/user-attachments/assets/becda9ba-3a60-4676-aa93-61017d48ddf9" />

___

__**Final Notes**__

•	This challenge tested my looping, conditional logic and file handling in Bash.

•	This helped me practice automation by embedding ‘ls’ commands in the script itself.

•	This also helped me confidently create files with minimal guidance.
