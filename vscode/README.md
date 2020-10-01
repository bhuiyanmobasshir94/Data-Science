## To run visual studio code in remote server 

Please follow this [repo](https://github.com/cdr/code-server)
To have systemd start code-server now and restart on boot:
```
sudo systemctl enable --now code-server@$USER
```
Change the password:
```
sudo nano ~/.config/code-server/config.yaml
```
Restart the service:
```
sudo systemctl restart code-server@$USER
```
