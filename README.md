# git_change_previous_commit_history
I had an issue, In my previous commits(around 120 commits) i forgot to add my email id, so the commits wont appear in the profile contribution graph
so i had to add email id to all previous commits and recommit
for this i used this below script :  from Liju


git filter-branch --env-filter '
NEW_NAME="Amaldev"
NEW_EMAIL="amaldev.psn@gmail.com"
    export GIT_COMMITTER_NAME="$NEW_NAME"
    export GIT_COMMITTER_EMAIL="$NEW_EMAIL"
    export GIT_AUTHOR_NAME="$NEW_NAME"
    export GIT_AUTHOR_EMAIL="$NEW_EMAIL"
' --tag-name-filter cat -- --branches --tags

--------------

do git push
