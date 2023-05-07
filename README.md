# Bandit-OverTheWire
This repository contain the file explaining how I got through some of the level of Bandit from Over The Wire.

##LVL0:
commande utilisé:
ls (to show all files)
cat readme(to read what's inside the file)
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

##LVL1:
commande utilisé:
ls
cat ./- (adding ./ because it's not a word like before)
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi

##LVL2:
ls
cat "spaces in this filename" (adding the "" because the name of the file has spaces in it so to be considered as one file we need to combine them with the "")
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG

##LVL3:
cd inhere (cd followed by the directory name to enter in the directory)
ls
ls -1a (because it says it's a hidden file we need to add -1a after ls to find all the possible hidden files)
cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

##LVL4:
cd inhere
ls
ls -1a (to order it in a row)
file ./* (to show all the extension of every file)
cat ./-file07 (because it's the only txt file among them)
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

##LVL5:
cd inhere
ls
find . -size 1033c (to find in which directory the file is supposed to be by finding it with his size)
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

##LVL6:
find / -user bandit7 -group bandit6 -size 33c(as mentionned it is owned by bandit7 owned by group bandit6 and has the size of 33 bytes)
cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs

##LVL7:
ls
*avoid doing cat data.txt because it will read a millions of data stored in it*
cat data.txt | grep millionth (it will only show the line of the specified word that is millionth and next to it will be the password)
TESKZC0XvTetK0S9xNwm25STk5iWrBvP

##LVL8:
ls
cat data.txt | sort | uniq -u (using sort will sort them in an alphabetical order and as for the uniq it duplicates lines of text from its input and adding -u will only print the lines that aren't duplicate)
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

##LVL9:
strings data.txt | grep = (strings will print all the printable characters like /*-+... but here we used grep to find all the line that has = on it)
G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

##LVL10:
cat data.txt | base64 --decode (as it was said it has a base64 encoded data and we used that command --decode to decode all the base64 encoded data)
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

##LVL11:
cat data.txt | tr a-zA-Z n-za-mN-ZA-M (This command translates the characters in the input stream by mapping each letter in the range a-zA-Z to the corresponding letter in the range n-za-mN-ZA-M.)
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

##LVL13:
ls

ssh bandit14@localhost -i(because it says the file is stored in directory only readable by the user bandit14 so we are entering as the user bandit14)
sshkey.private

NO

##LVL14:
cat /etc/bandit_pass/bandit14

telnet localhost 30000 
(We now have to paste the password in the escape characters to get the correct password)

BfMYroe26WYalil77FoDi9qh59eK5xNr

##LVL15:
openssl s_client -connect
localhost:30001 -ign_eof
(We past the previous password from the previous level)

cluFn7wTiGryunymYOu4RcffSxQluehd

##LVL16:
nmap -A localhost -p 31000-32000
openssl s_client -client
localhost:31790
(entering the previous password)
(then copy the RSA private key)
mkdir /tmp/techyrick_ssh
cd /tmp/techyrick_ssh
nano techyrick.private
(paste the RSA key in nano techyrick.private)

chmod 600 pavan.private
ssh bandit17@localhost -i
pavan.private

Not required

##LVL17:
ls
diff passwords.old passwords.new (to check all the changes made between them)
kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd

##LVL18:
ssh -T bandit18@localhost

(we will see a blank terminal after entering the previous command, after that we will enter the following commands)
ls
cat readme
ctrl+c(then log out from the bandit18 to enter in the *ssh bandit 19@localhost*)

##LVL19:
ls
./bandit20-do

./bandit20-do cat
/etc/bandit_pass/bandit20

GbKksEFF4yrVs6il55v6gwY5aVje5f0j
