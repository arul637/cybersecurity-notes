## installation 

```bash
sudo apt update 
sudo apt install ruby ruby-dev build-essential -y
sudo gem install haiti-hash
```

it is a cli tool to identify the hash

suppose we ahve hash `7576f3a00f6de47b0c72c5baf2d505b0`

```
haiti -e '7576f3a00f6de47b0c72c5baf2d505b0'
```

to find the hash type we need to use `haiti -e` 

