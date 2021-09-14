# Pre-Game H@cktivityCon 2021
___________________________________________________________
#### Challenge Name: *Ladybug*
#### Category: *Web*

#### Description: 
Want to check out the new Ladybug Cartoon?
It's still in production, so feel free to send in suggestions!

___________________________________________________________

#### Solution: 

First thing i did was click everything in the website,<br>
tried getting an LFI from the search bar link but that was a rabbit hole also the contact page doesn't work

So i focused on Categories and when you click them you see:<br>
`http://challenge.ctf.games:30675/film/park/`

and when you remove the slash at the end you will be redirected back to 
`/film/park/` for proper info [click here](https://ahrefs.com/blog/trailing-slash/#:~:text=A%20trailing%20slash%20is%20a,not%20have%20the%20trailing%20slash.&text=These%20days%2C%20URLs%20in%20most,aren%27t%20pointing%20to%20files.)

meaning its a directory, so i changed the park to something else to see what errors am i going to get


By going to `http://challenge.ctf.games:30675/film/anything/`,<br>
i got the Werkzeug Debugger page which should be used only in the development environment,<br>
because it can lead to RCE so you write some python code in the python terminal when you<br>
hover over an error in right side you will see a terminal logo



py script:
```
import os

print(os.popen('ls').read())
print(os.popen('cat flag.txt').read())
```

![[Pasted image 20210915012348.png]]


#### Flag: *`flag{weurkzerg_the_worst_kind_of_debug}`*
