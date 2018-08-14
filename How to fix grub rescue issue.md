### How to Solve grub rescue issue? 

It was a trial and error method but it worth the every second :)

- grub rescue >```ls```  ~~~It will show all the paritions~~~

eg

(hd0)(hd0,msdos5) (hd0,msdos3) (hd2,msdos2) (hd1,msdos1)

- grub rescue> ```set boot=(hd0,msdos5)```
- grub rescue> ```set prefix=(hd0,msdos5)/boot/grub```
- grub rescue> ```insmod normal```  ~~~if this shows an error message we need to redo the steps~~~


- grub rescue> ```set boot=(hd0,msdos3)```
- grub rescue> ```set prefix=(hd0,msdos3)/boot/grub```
- grub rescue> ```insmod normal```  ~~~if this shows an error message we need to redo the steps~~~



- grub rescue> ```set boot=(hd2,msdos2)```
- grub rescue> ```set prefix=(hd2,msdos2)/boot/grub```
- grub rescue> ```insmod normal```  ~~~if this shows an error message we need to redo the steps~~~
- grub rescue> ```normal```   ~~~It will automatically reboot and show you the Boot Option Menu~~~ :)

#### Gossip 

 I was recently at a training and actually we can work on any platforms. However due to my own interest to know more about [Kali Linux](https://kali.org), I installed it on my host machine and then I messed up with some commands, cause I am a lazy pig and didn't even care to create a separate user (one of the best practice). After which I messed up.


Circumstances hijacked all my possiblities to work on either Kali or uBuntu, therefore, I was left with no option but to work on Window Machine (It is Window 10 though). Although I don't have much positive impression of Window but I found it not bad as I had thought. This semi blog is writing on Window using [Visual Studio Code](https://code.visualstudio.com/download). I had used [Atom](https://atom.io/) Editor in prior and its look and feel is quite similar.  

After googling and youtubing (not sure whether such words are there), I was able to find the solution to fix it. I lost the link from where I got the solution but it was on stackoverflow. I am quite sure you will find it if you wish to check it.

Anyway, that's all. If you were speculating why this guy is making making huge deal; it is because I am practicing Mark Down command on VSCode :)

