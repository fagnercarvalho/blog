# blog

### How this was created
```shell
winget install Hugo.Hugo.Extended
hugo new site . --force
cd themes
git clone git@github.com:Vimux/Binario.git
# update hugo.toml accordingly
hugo server -D
```