# locales
New `en_US` locale for 24-hour time on Ubuntu
## What is this?
If you live in the US, speak English mostly, and would rather use
24-hour time, then this is for you. This changes only the following in
your locale:

1. 24-hour time instead of 12-hour AM/PM nonsense
2. Change the first day of the week to Monday

## What do I do with this?
The instructions are in the file `en_US` file, but it's pretty straightforward:

1. Copy the `en_US` file to `/usr/share/i18n/locales`. (If you're feeling paranoid, see below.)
2. Run the command: `sudo localedef -f UTF-8 -i en_US en_US.UTF-8`. 
3. Restart anything that you want to show the changes. _Thunderbird_, for example.

## I _am_ paranoid. What should I do?
There's a tag in the repo called *Sysnew*. Check out that tag and compare the file `en_US` to the one in `/usr/share/i18n/locales`. If there are no differences, you can check out _master_ and rest assured you have a fallback if you need it. If they differ, then someone should have a look at those changes. Maybe they should be incorporated into the new file. The rest of that scenario is beyond the scope of this README.

## I am _very_ paranoid and the suggestion above doesn't help.
Make a copy of `/usr/share/i18n/locales/en_US` before you begin the process. You can always run the `localedef` command on that copy later if everything goes pear-shaped.
