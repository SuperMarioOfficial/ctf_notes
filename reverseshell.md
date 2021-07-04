## CTF - Boxes - Tutorials
- https://tryhackme.com/room/vulnversity


## netcat<3 stuffs
```nc -nvlp 1234```
On the receiving end,
```nc -l -p 1234 | uncompress -c | tar xvfp -```
On the sending end,
```tar cfp - /some/dir | compress -c | nc -w 3 [destination] 1234```
A much cooler but less useful use of netcat is, it can transfer an image of the whole hard drive over the wire using a command called dd.
On the sender end run,
```dd if=/dev/hda3 | gzip -9 | nc -l 3333```
On the receiver end,
```nc [destination] 3333 | pv -b > hdImage.img.gz```
- https://nc110.sourceforge.io/
- https://www.andreafortuna.org/2017/05/18/reverse-shell-with-netcat-some-use-cases/
- https://stuffjasondoes.com/2018/07/18/bind-shells-and-reverse-shells-with-netcat/
- https://randombio.com/linuxsetup86.html\
- [Python host-webserver for file transfer to the remote machine](https://reptile.haus/blog/the-ultimate-reverse-shell-collection/)


## Links to everything 
- https://reptile.haus/blog/the-ultimate-reverse-shell-collection/
- https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet
- https://highon.coffee/blog/reverse-shell-cheat-sheet/
- https://gtfobins.github.io/gtfobins/systemctl/
- https://www.infosecademy.com/netcat-reverse-shells/
- https://unicornsec.com/home/tryhackme-vulnversity
- https://sckull.github.io/posts/vulnversity/
- https://www.hackingarticles.in/linux-privilege-escalation-automated-script/
