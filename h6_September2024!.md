# Hashcat

- I installed Hashcat on Mac with Homebrew using 'brew install hashcat'
- Following the instructions here: https://terokarvinen.com/2022/cracking-passwords-with-hashcat/
  - I created a new directory with 'mkdir hashed', and moved to it with 'cd hashed'
  - I installed 'wget' with Homebrew using 'brew install wget', and downloaded rockyou dictionary
  - I extracted the rockyou.txt file with 'tar xf rockyou.txt.tar.gz'

- Identifying & cracking the hash
  - Using 'hashid -m 6b1628b016dff46e6fa35684be6acc96' I get a list of hash types:
  ![Screenshot 2024-09-26 at 14 00 08](https://github.com/user-attachments/assets/6ca4c3a4-8f97-4bd3-aab2-42dae8872aba)
  - To crack the hash, I use hash type MD5 in the command 'hashcat -m 0 '6b1628b016dff46e6fa35684be6acc96' rockyou.txt -o solved', and save the plaintext password to a file called "solved".
  ![Screenshot 2024-09-26 at 13 36 31](https://github.com/user-attachments/assets/830d64b4-6c4c-4db4-a7db-d44afa8527ac)
  - The data from cracking the hash is shown along with the duration and key details
  - Running 'cat solved' shows the plaintext password.

- I repeated the same commands to crack the hash 'd595b2086532422bbe654bc07ea030df'
![Screenshot 2024-09-26 at 13 52 14](https://github.com/user-attachments/assets/4a385ed0-39b6-4027-81d9-808b9a8b733b)
- I only changed the hashid and the name of the file the password would be saved to.
  - MD5 worked for this hash as well.

