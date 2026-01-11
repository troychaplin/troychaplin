# Mac Config

To execute:

```
chmod +x mac-install.sh
./mac-install.sh
```

## Switching Coding Standards

- Check Active standard: `phpcs --config-show`
- Use PSR2 Standard: `phpcs --config-set default_standard PSR2`
- Use WordPress Standard: `phpcs --config-set default_standard WordPress`

## Final Review

Before you format don't forget to backup key elements such as:

- SSH keys and other dot files
- Database app connection details
- Transmit connections

## Followup Notes

To become a set of dot files

- https://github.com/webpro/awesome-dotfiles

---

## Other Installs

- Xcode - `xcode-select --install`
- [How to Install Ruby on Mac OS X with RVM](https://usabilityetc.com/articles/ruby-on-mac-os-x-with-rvm/) (see following)

```
brew install gnupg
gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
\curl -sSL https://get.rvm.io | bash -s stable --ruby
```

## Props

This setup script was built referencing ideas from:

- https://github.com/marceloglacial/macos-fresh-install
- https://github.com/maxyermayank/developer-mac-setup
