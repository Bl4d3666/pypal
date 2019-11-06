Pypal
============

Python port of Pipal for password analytics

This is currently a library with no front end, mainly for use with CrackQ,
but it can be imported into any project to generate a HTML report of a 
password dump analysis.

Uses fuzzy string matching and levenshtine algorithm to identify base words.

**Install**
----------------
```
git clone https://github.com/f0cker/pypal
cd pypal
pip3 install .
```

**Usage**
----------------
```
import pypal
from pathlib import Path

report = pypal.Report(Path('/path/to/cracked/passwords.txt'))
status = report.report_gen()
```

The above will generate a html report at */path/to/cracked/passwords_report.html*


Features/Metrics:

- [x] Top 10 cracked passwords
- [x] Top x passwords by length
- [x] Top x base dictionary words


Todo:

- [ ] Top x base words by city
- [ ] Top x base words by country

- [ ] password complexity (character sets)
- [ ] crack time
- [ ] based on a name
- [ ] based on a country/place
- [ ] based on multiple words
- [ ] based on common password pattern
- [ ] top 10 most popular words/name 
- [ ] top 10 masks
- [ ] top 10 masks by position in password
- [ ] top 10 passwords
- [ ] top 10 patterns?
- [ ] top 10 used numbers
- [ ] top 10 end numbers 1 - 6
- [ ] top 10 most common numerical patterns
- [ ] Months/Year/Day
- [ ] Geomap using location coordinates mapped from matched basewords by location
- [ ] show users with shared passwords
- [ ] show users with blank passwords

AD dump analysis:

- [ ] how many passwords are non-compliant with policy
- [ ] domain admins etc
- [ ] users not-compliant