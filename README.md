# Ejercicios Linux

#Ejercicios. Capitulo 4


**1) Show all the jpg pictures in the current directory.**

ls *.jpg

**2) Display all the files in the directory /usr/bin starting with letter “j”.**

ls /usr/bin/j*

**3) Show all the files in the directory /usr/bin starting with the letter “k”, with an “a” 
in the 3rd place.**

ls /usr/bin k?a*

**4) Show all the files in the directory /bin ending with “n”.**

ls /bin *n

**5) Display all the files in the directory /etc and all the files in every subdirectory
recursively.**

tree /etc

**6) In your home directory, create another directory named test. Copy the file gzip from
the directory /bin to test. Create a duplicate of gzip named gzip2 inside test.**

touch /home/alumno test | 
cp /bin/gzip /home/alumno/test | 
cp /bin/gzip /home/alumno/gzip2

**7) Change the name of the directory test to test2. Create test3 at the same level in
the directory tree as test2 and move all the files from test2 to test3. Delete test2.**

mv test test2 | 
touch test3 | 
cp test2 test3 | 
rm test2

**8) Create an empty file named “*?Hello all?*”. Can you? Is it a good idea to name a file
this way? Explain your answer.**

Si se puede crear pero no es aconsejable, por que seria con muchos \ y muy liante a la hora de acceder a el.

**9) Create a directory named multimedia_test and copy all the content from the
directory multimedia into it. Then, create two files in multimedia/video/, one
named films.txt and another named actors.txt. Edit the file films.txt and write
the title of your favourite movie. Then, create another file in multimedia_test/video/,
also named films.txt. Edit this file and now write the titles of your five favourite movies.
Copy of all the content of multimedia into multimedia_test ensuring that
only most recently modified versions of files remain.To check that
everything is ok, check if multimedia_test/video contains the empty file
actors.txt and the file films.txt**

mkdir multimedia_test | cp /multimedia /multimedia_test | touch /multimedia/video/films.txt /multimedia/video/actors.txt | 

nano films.txt ahora escribes las cosas | mkdir /multimedia_test/video/ | cp /multimedia/* /multimedia_test | 

tree /multimedia_test | cat actors.txt films.txt


**10) Delete the directory multimedia/pictures/others. The system must ask for
confirmation.**

rmdir -i multimedia/pictures/others

**11)Move the file films.txt, which is in multimedia/video, to the directory above,
at the same time renaming the file to my_films.txt.**

mv films.txt multimedia/video | mv films.txt my_films.txt
