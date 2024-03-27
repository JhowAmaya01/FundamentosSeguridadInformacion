## Player: GreyGods
## Goal
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/6/challenge.zip)

Additional details will be available after launching your challenge instance.
## Hints
+ Have you ever played hot or cold? Binary search is a bit like that.
+ You have a very limited number of guesses. Try larger jumps between numbers!
+ The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

## Solution

```bash
─[parrot@parrot]─[~/picoCTF_2024/drop-in]
└──╼ $ssh -p 61918 ctf-player@atlas.picoctf.net
The authenticity of host '[atlas.picoctf.net]:61918 ([18.217.83.136]:61918)' can't be established.
ECDSA key fingerprint is SHA256:ordTMCwK3qpNza5KnIvhhv3zuT2jVOfUn+VlRwYK23s.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:61918,[18.217.83.136]:61918' (ECDSA) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
Im thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 700
Lower! Try again.
Enter your guess: 600
Higher! Try again.
Enter your guess: 650
Higher! Try again.
Enter your guess: 675
Higher! Try again.
Enter your guess: 680
Higher! Try again.
Enter your guess: 690
Higher! Try again.
Enter your guess: 695
Congratulations! You guessed the correct number: 695
Here is your flag: picoCTF{g00d_gu355_de9570b0}
Connection to atlas.picoctf.net closed.
````


## Notes

## References