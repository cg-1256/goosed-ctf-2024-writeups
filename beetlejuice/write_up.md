# Beetlejuice

Firstly download the file and navigate to the appropriate folder.

## Cracking the Zip
I am going to use JohnTheRipper, but if you prefer a different password cracker than I will leave that to you to do the equivilent steps.

Make sure to install JohnTheRipper if you do not have it installed.

Firstly you are going to want to find the hashes of the file with the command:
`zip2john Beetlejuice.zip > hashes.txt`

Once you have done that, use John to find the password with the command:
`john hashes.txt` 

This will spit out the password "qwertyuiop" which can be found as the second to last entry on the fasttrack.txt wordlist. Now that you have this password, you can run the following command and use that when prompted for the password:
`unzip Beetlejuice.zip`

This will give you a PNG file called "BeetlejuiceBeetlejuice".

## Finding the Flag
Now that you have the PNG file, the next step is to find the flag. The flag is hidden in the Least Significant Bit (LSB) and can be discovered, either by creating a script to read the data contained in the LSB or use 'Extract LSB' option on CyberChef (cyberchef.org)
