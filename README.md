# 8.9.2 疯狂填词

import re
new_text = open('Mad Libs_new.txt', 'w')
text = open('Mad Libs.txt')
content = text.read()
text.close()
print(content)

pattern = re.compile(r'ADJECTIVE|NOUN|ADVERB|VERB')
mo = pattern.findall(content)

for word in mo:
    print('Enter an {}'.format(word).lower())
    repl = input()
    regex = re.compile(word)
    content = regex.sub(repl, content, 1)

new_text.write(content)
new_text.close()
