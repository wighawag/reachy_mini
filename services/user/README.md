using user services

(NOTE: I use system service as they works, but I decided to kept what I tried here:)

```
mkdir -p ~/.config/systemd/user
```

add the files

```
systemctl --user daemon-reload
systemctl --user enable --now reachy-mini-conversation.service
```


enable them on boot
```
sudo loginctl enable-linger wighawag
```


see logs
```
journalctl -b _SYSTEMD_USER_UNIT=reachy-mini-daemon.service -f
```