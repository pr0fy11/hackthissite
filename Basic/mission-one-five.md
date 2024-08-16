
- [Mission 1](#mission-1)
  * [Overview](#overview)
  * [Solution](#solution)
  * [Key Idea](#key-idea)
- [Mission 2](#mission-2)
  * [Overview](#overview-1)
  * [Solution](#solution-1)
  * [Key Idea](#key-idea-1)
- [Mission 3](#mission-3)
  * [Overview](#overview-2)
  * [Solution](#solution-2)
  * [Key Idea](#key-idea-2)
- [Mission 4](#mission-4)
  * [Overview](#overview-3)
  * [Solution](#solution-3)
  * [Key Idea](#key-idea-3)
- [Mission 5](#mission-5)
  * [Overview](#overview-4)
  * [Solution](#solution-4)
  * [Key Idea](#key-idea-4)

# Mission 1
https://www.hackthissite.org/missions/basic/1/

## Overview
This level is what we call "The Idiot Test", if you can't complete it, don't
give up on learning all you can, but, don't go begging to someone else for the
answer, thats one way to get you hated/made fun of. Enter the password and you
can continue.

## Solution
View the page source. Above the password form, there’s a comment that reads:
<!-- the first few levels are extremely easy: password is xxxxxxxx -->
Your password may differ, but just enter the text you see and submit.

## Key Idea
Check the raw HTML and see what you can learn.

# Mission 2
https://www.hackthissite.org/missions/basic/2/

## Overview
Network Security Sam set up a password protection script. He made it load the
real password from an unencrypted text file and compare it to the password the
user enters. However, he neglected to upload the password file...

## Solution
Since the password file is missing, you can simply submit the form with an empty password. Although Sam’s use of an unencrypted text file is problematic, it’s irrelevant here because the file isn’t present.

## Key Idea
Experiment with random or empty inputs. While random inputs alone might not solve the problem, they can provide insights into the backend’s behavior, helping you craft more effective inputs.

# Mission 3
https://www.hackthissite.org/missions/basic/3/

## Overview
This time Network Security Sam remembered to upload the password file, but
there were deeper problems than that.

## Solution
Start by viewing the page source, as in Mission 1. You’ll find this line in the HTML:
`<input type="hidden" name="file" value="password.php" />.`
Navigate to https://www.hackthissite.org/missions/basic/3/password.php. The password is displayed in plain text. Go back, enter the password, and submit.
## Key Idea
Like in Mission 2, hidden files or pages can sometimes be accessed by checking the raw HTML. If found, try accessing them to gather more information.
## Key Idea

# Mission 4
https://www.hackthissite.org/missions/basic/4/

## Overview
This time Sam hardcoded the password into the script. However, the password is
long and complex, and Sam is often forgetful. So he wrote a script that would
email his password to him automatically in case he forgot. Here is the script

[form box]

## Solution
Clicking the "Send password to Sam" button will trigger an email. Then, check the page source. You’ll see this line in the HTML:
`<input type="hidden" name="to" value="sam@hackthissite.org" />.`
What if you change the email address to yours (or the one you used to register on Hack This Site)? Edit the value using Developer Tools and click the button to send the password to your email.

## Key Idea
This mission builds on Missions 1 and 3 by encouraging you to manipulate the raw HTML, which sometimes yields results.

# Mission 5
https://www.hackthissite.org/missions/basic/5/

## Overview
Sam has gotten wise to all the people who wrote their own forms to get the
password. Rather than actually learn the password, he decided to make his
email program a little more secure.

## Solution
Because Sam didn’t address the core issue, the solution from Mission 4 still works. Edit the email address value using Developer Tools and send yourself the password.


