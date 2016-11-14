# Ejercicios Linux

##Capitulo 3


###1) Show all the jpg pictures in the current directory.###

```console 
ls *.jpg
```
###2) Display all the files in the directory /usr/bin starting with letter “j”.###
```console 
ls /usr/bin/j*
```
###3) Show all the files in the directory /usr/bin starting with the letter “k”, with an “a” in the 3rd place.
```console 
ls /usr/bin/k?a*
```
###4) Show all the files in the directory /bin ending with “n”.###
```console 
ls /bin/*n
```
###5) Display all the files in the directory /etc and all the files in every subdirectory recursively.
```console 
tree /etc
```
###6) In your home directory, create another directory named test. Copy the file gzip from the directory /bin to test. Create a duplicate of gzip named gzip2 inside test.
```console 
mkdir /home/alumno/test
cp /bin/gzip /home/alumno/test
cp /bin/gzip /home/alumno/gzip2
```
###7) Change the name of the directory test to test2. Create test3 at the same level in the directory tree as test2 and move all the files from test2 to test3. Delete test2.
```console 
mv test test2
mkdir test3
mv test2 test3
rmdir test2
```
###8) Create an empty file named “*?Hello all?*”. Can you? Is it a good idea to name a file this way? Explain your answer.
```console 
Si se puede crear pero no es aconsejable, por que seria con muchos \ y muy liante a la hora de acceder a el.
```
###9) Create a directory named multimedia_test and copy all the content from the directory multimedia into it. Then, create two files in multimedia/video/, one named films.txt and another named actors.txt. Edit the file films.txt and write the title of your favourite movie. Then, create another file in multimedia_test/video/, also named films.txt. Edit this file and now write the titles of your five favourite movies. Copy of all the content of multimedia into multimedia_test ensuring that only most recently modified versions of files remain.To check that everything is ok, check if multimedia_test/video contains the empty file actors.txt and the file films.txt
```console 
mkdir multimedia_test
cp /multimedia /multimedia_test
touch /multimedia/video/films.txt /multimedia/video/actors.txt
nano films.txt ahora escribes las cosas
mkdir /multimedia_test/video/
cp /multimedia/* /multimedia_test
tree /multimedia_test
cat actors.txt films.txt
```

###10) Delete the directory multimedia/pictures/others. The system must ask for confirmation.
```console 
rmdir -i multimedia/pictures/others
```
###11)Move the file films.txt, which is in multimedia/video, to the directory above, at the same time renaming the file to my_films.txt.
```console 
mv films.txt multimedia/video
mv films.txt my_films.txt
```
##Capitulo 4

###1) Complete the following table:
```console
+---+---------+
|654|rw-r-xr--|
+---+---------+
|766|rwxrw-rw-|
+---+---------+
|777|rwxrwxrwx|
+---+---------+
|520|r-x-w----|
+---+---------+
|764|rwxrw-r--|
+---+---------+
|660|r--r-----|
+---+---------+
```
##In the following exercises, you should use the required Linux commands to perform the operations described.
###2) Create the groups office1 and office2.
```console
addgroup office1
addgroup office2
```
###3) Create the users gearoid and paul. These users must belong only to the group office1.
```console
adduser gearoid -g office1
adduser paul -g office1
```




