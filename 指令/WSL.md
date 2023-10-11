将Windows下的字体目录链接到WSL目录下即可，之后再刷新一下

```
sudo ln -s /mnt/c/Windows/Fonts /usr/share/fonts/font
fc-cache -fv
```

