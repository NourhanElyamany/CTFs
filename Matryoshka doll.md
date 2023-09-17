<a href='https://play.picoctf.org/practice/challenge/129?category=4&page=1&solved=0'><h1>  Matryoshka doll </h1><a>

<h3> The challenge is giving you an image and stating that there may be a hidden files in it </h3>
<img src="Images/4.png">


I used the `binwalk` command to see if there are any files hidden inside this image.
I found compressed files inside it so I extracted using the `binwalk -e` command.

<img src="Images/5.png">

The extracted files gave me a folder called base images that contain another image of the matroyshka doll, so repeat the same command of binwalk to extract if there
are hidden files inside the second image.

<img src="Images/6.png">

Repeat this until you found image number 4 you will find inside it a `flag.txt`, use the `cat` command to show you the content of the file. congratulations you found it.
<img src="Images/7.png">

`flag: picoCTF{96fac089316e094d41ea046900197662} `
