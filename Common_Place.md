# Pre-Game H@cktivityCon 2021
___________________________________________________________
#### Challenge Name: *Common Place*
#### Category: *Warmups*

#### Description: 
asd7138: can you find the flag here?<br>
tcm3137: no, i dont see it<br>
jwh8163: i cant find it either<br>
rfc5785: i found it<br>
asd7138: what!? where?!<br>
jwh8163: tell us!<br>

___________________________________________________________

#### Solution:

First of all lets look at the descreption and see what do we recognize,<br>
of course if you focus you will see an `rfc` or Request for comments <br>
`rfc` is document that describes the standards, protocols, technologies<br>
of the internet.

if you google the rfc5785 you will find a document from IETF or the internet engineering task force.

```
Defining Well-Known Uniform Resource Identifiers (URIs)

Abstract

   This memo defines a path prefix for "well-known locations",
   "/.well-known/", in selected Uniform Resource Identifier (URI)
   schemes.
```

we care about the directory **`/.well-known/`**<br>  also i would suggest when you find an rfc read the use cases.

when we try to access the directory we get the `flag.txt` file in the `/.well-known/` directory .

Flag Location: http://challenge.ctf.games:30032/.well-known/flag.txt


#### Flag: *`flag{rfc5785_defines_yet_another_common_place}`*
