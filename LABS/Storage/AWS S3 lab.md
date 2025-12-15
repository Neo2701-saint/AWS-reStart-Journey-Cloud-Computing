# __**Create and configured an S3 bucket**__

**This lab explores the creation of an S3 bucket uploading objects and 
configuring permissions to make the objects accessible through a browser.**

___

**I started the "Create bucket" process and had the "Block all public access" checked (the default secure setting).**

<img width="759" height="309" alt="image" src="https://github.com/user-attachments/assets/ff4f32ca-c5d8-4877-8991-85501797d108" />
<img width="759" height="320" alt="image" src="https://github.com/user-attachments/assets/8a9d28e4-2668-4bcf-a319-f99405a7fa22" />

___

**I then unchecked all "Block public access" settings and 
checked the acknowledgement box stating.**

<img width="754" height="275" alt="image" src="https://github.com/user-attachments/assets/b48c36a0-aa36-4038-b3d7-8925f02325a6" />

___

**I configured the "Encryption type"as Server-side encryption 
with Amazon S3 managed keys (SSE-S3) and enabled the bucket key then created the bucket.**

<img width="767" height="311" alt="image" src="https://github.com/user-attachments/assets/3aa608f8-e56b-4a57-9006-dd2301ee6453" />
<img width="752" height="304" alt="image" src="https://github.com/user-attachments/assets/7354a908-25fc-4733-bd57-5c29845fdb8d" />

___

**I examined and configured settings for an existing bucket, in which the 
"Bucket website endpoint", the public URL for the static website is visible.**

<img width="758" height="305" alt="image" src="https://github.com/user-attachments/assets/ceabadb9-863d-47d2-8832-c76ab30ed73b" />
<img width="750" height="319" alt="image" src="https://github.com/user-attachments/assets/544e864b-a043-4032-a097-f0d13539a9c0" />

___

**I reviewed the Bucket Policy.**

<img width="744" height="299" alt="image" src="https://github.com/user-attachments/assets/5b391065-685e-4f07-87c8-45a4572c142b" />

___

**I then created the folder "images".**

<img width="681" height="257" alt="image" src="https://github.com/user-attachments/assets/57aab616-5d4e-4b01-be4b-5e4a2d7b847a" />

___

**I then navigated into the "images" folder which contains image objects.**

<img width="724" height="285" alt="image" src="https://github.com/user-attachments/assets/9af99010-5e06-49a4-8769-cba433ccf3c4" />

___

# **What I learned**

Learned the essential secure-by-default architecture of S3 and 
policy and block-setting required to override the security for the specific use case of public static website hosting.
