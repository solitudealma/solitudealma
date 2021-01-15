### Hi there 👋
#!/usr/bin/env bash
# Author: Shixiang Wang 
# LICENSE MIT@2020

echo "This program reset the origin repository from gitee to github."

remote=$(git status && echo $(git remote -v | grep fetch | sed -E 's/.*(http[s][^ ]*).*/\1/') || echo "Not a git repo")

if [[ $remote == "Not a git repo" ]]; then
    echo "!! Not a git repo, exit..."
    exit 1
fi

remote=$(echo $remote | sed -E 's/.*(http[s][^ ]*)$/\1/')
remote=$(echo $remote | sed -E 's/gitee/github/')

git remote remove origin
git remote add origin $remote

echo "Done."
<!--
**solitudealma/solitudealma** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
