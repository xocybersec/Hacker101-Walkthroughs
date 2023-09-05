Hacker101 <br>
Postbook

---
Upon being directed to the website, there is a login section to either log in or create an account.
I made a test account and logged in.
When hovering the pointer over the posts links I notice there’s an `id=1` and an `id=3` parameter.
After clicking on one of the posts, I tried to manipulate the parameter to view `id=2`

![image](https://github.com/xocybersec/Hacker101-Walkthroughs/assets/91302698/54b9ef48-221c-48a8-b661-adc069a506a2)
 
That took me to an admin’s private post with a flag available.

![image](https://github.com/xocybersec/Hacker101-Walkthroughs/assets/91302698/bf4e6856-0260-41db-a9f3-c10c4c92d14f)
---
The posts also show the account that made the posts. There’s an `admin` and `user` account. I’ll try to log in as the ‘user’ account with some basic passwords to see if I can get in.
The combo `user:password` granted us access to that account and we are welcomed with a flag.

![image](https://github.com/xocybersec/Hacker101-Walkthroughs/assets/91302698/6c712006-df58-4a7a-a4c6-d2a5bf4d246c)
---
While logged in, I wanted to see what other parameters were able to be manipulated. I clicked on the public post from the admin account and noticed `index.php?page=view` in the URL and tried to see if I could change `view` to `edit`
I was able to edit the admin’s post and after submitting the change there was a flag waiting.

![image](https://github.com/xocybersec/Hacker101-Walkthroughs/assets/91302698/daa4fa38-7c65-43ec-a54b-3040d888cf6e)
---
On the `Write a new post` page the source code reveals parameters that can be manipulated as well. `hidden` can be changed to `show`, `user_id` can be changed and so can `value`.

![image](https://github.com/xocybersec/Hacker101-Walkthroughs/assets/91302698/84dd5280-2d72-47a9-a975-1f0905670899)

With my test account being `3`, that means `user` should be `2`, and `admin` should be `1`
After changing the value to <i>1</i>, entering something random in the text box on the webpage, and submitting it another flag is shown along with the completed submission. The message was posted spoofed as the admin account.

![image](https://github.com/xocybersec/Hacker101-Walkthroughs/assets/91302698/293c2761-ef67-4411-8da7-269f07ed0443)
---
