gpg --full-generate-key

gpg --list-secret-keys --keyid-format=long

gpg --armor --export

git config --global --unset gpg.format

gpg --list-secret-keys --keyid-format=long

git config --global user.signingkey

git config --global commit.gpgsign true

[ -f ~/.bashrc ] && echo -e '\nexport GPG_TTY=$(tty)' >> ~/.bashrc
