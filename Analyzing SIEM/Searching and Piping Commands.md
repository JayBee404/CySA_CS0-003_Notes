Creating a SIEM correlation rule usually involves searching with strings

Regular Expression (regex) - A group of characters that describe how to execute a specific search pattern on a given text
A good cybersecurity analyst can use regex efficiently, but you just need to know the basics for the CySA+ exam

\[...] - Matches a single instance of a character within the brackets, such as \[a-z], \[A-Z], \[0-9], \[a-zA-Z0-9], \[\\s], (white space), or \[\\d] (single digit)

\+ - Matches one or more occurrences and is called a quantifier, such as \\d+ matching on or more digits

\* - Matches zero or more occurrences, such as \\d\* matching zero or more digits

? - Matches one or non times, such as \\d? matching zero or one digits

{} - Matches the number of times within the curly braces, such as \\d{3} matching 3 digits or \\d{7-10} matching seven to ten digits

(...) - Defines a matching group with a regex sequence placed within the parentheses, and then each group can subsequently be referred to by \\1 for the first group, \\2 for the second, and so on

| - The OR logical operator to match conditions as "this or that"

^ - The regex will only match at the start of a line when searching

$ - The regex will only match at the end of a line when searching

https://www.regexr.com - learn more about regex and practice building them with an interactive tool

grep - A command on Unix/Linux/macOS systems that involves simple string matching or regex syntax to search text files for specific strings

`grep -F 192.168.1.10 access.log`

`grep "192\.168\.1\.10" *`

`grep -r 192\.168\.1\.[\d]{1,3} .`

Common grep flags:
- -i (ignore case sensitivity)
- -v (return non-matching lines)
- -w (match whole words only)
- -c (return a count of matching lines)
- -l (return names of files with matching lines)
- -L (return names of files without matching lines)
- -F - treat as string literal
- -r - recursive search

Windows doesn't include grep in its command line and instead uses `find` for basic strings and `findstr` for regex searching

cut - A command that enables the user to specify which text on a line they want removed from the results

`cut -c5 syslog.txt` - returns only the fifth character in each line from the syslog.txt file

`cut-c5-5 syslog.txt` - Returns only the fifth through tenth characters in each line from the syslog.txt file

`cut -d " " -f1-4 syslog.txt` - Returns the first four entries of each line as delimited by the " " (space character)

sort - A command that can be used to change the output order

`sort syslog.txt` - Returns the contents of the syslog.txt file in alphabetical order (a-z)

`sort -r syslog.txt` - Returns the contents of the syslog.txt file in reverse alphabetical order (z-a)

`sort -n syslog.txt` - Returns the contents of the syslog.txt file in numerical order (0-9)

`sort -k 2 syslog.txt` - Returns the contents of the syslog.txt file in order based on the column (2) specified

`sort -t "," -k 2 syslog.txt` - Returns the contents of the syslog.txt file in order based on the column specified, such as the column specified, such as the second column, while delimiting the columns using comma separated values

head - A command that outputs the first 10 lines of a file specified

`head syslog.txt` - Returns the first 10 lines of syslog.txt

tail - A command that outputs the last 10 lines of a file specified

Piping ('|') - The process of using the output of one command as the input for a second command

`grep "NetworkManager" /var/log/syslog | cut -d " " -f1-5 | sort -t " " -k 3`