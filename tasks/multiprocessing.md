# Multiprocessing

## Helpful information

Study following links:
 - https://pymotw.com/2/multiprocessing/index.html
 - https://pymotw.com/2/multiprocessing/mapreduce.html
 - https://docs.python.org/2/library/multiprocessing.html
 - https://docs.python.org/2/howto/argparse.html


## Subtask 1

Create multiprocessing generator `links_finder` to find links on
sites using HTML parser or regular expression like on example:

```python
links = links_finder(["http://www.goole.com", "http://www.github.com"])
pprint(links)
# {
#     "http://www.goole.com": ["link1", "link2", "link3"],
#     "http://www.github.com": ["link1", "link2", "link3"]
# }
```


## Subtask 2

Create multiprocessing script `grep.py` analog of Linux `grep` command for
performing parallel search. Nice to have following option implemented:
 - `-R` recursive search
 - `-n` number of line
 - `-p` number of processes (by default number of cores)

```bash
$ grep.py -R -n 'user' /etc
/etc/pam.d/sshd:51:# to run in the user's context should be run after this.
/etc/pam.d/sudo:3:auth       required   pam_env.so readenv=1 user_readenv=0
```


## Subtask 3

Create multiprocessing function `words_counter` to count occurrence of words in
text files in specified path like on example:

```python
exclude = ["if", "else", "on", "at"]
words = words_counter(path='/home/keda',
                      glob_patterns=('*.py', '*.txt'),
                      ingnored_words=('else', 'ret*'),
                      min_word_len=3)
pprint(words)
# {
#     "import", 33,
#     "print", 65,
#     ...
# }
```

_Note: try to implement your own words counter, link finder (do not just
copy from examples above)._

_Note: try to implement your home tasks for multiprocessing using different
aproches._