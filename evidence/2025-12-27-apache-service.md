## Apache HTTP Server – Service Status

### Command
```bash
sudo systemctl status apache2 --no-pager
● apache2.service - The Apache HTTP Server
     Loaded: loaded (/usr/lib/systemd/system/apache2.service; enabled; preset: enabled)
     Active: active (running) since Sat 2025-12-27 01:02:37 CST; 13h ago
       Docs: https://httpd.apache.org/docs/2.4/
   Main PID: 1477 (apache2)
      Tasks: 55 (limit: 18892)
     Memory: 8.7M (peak: 10.1M)
        CPU: 2.461s
     CGroup: /system.slice/apache2.service
             ├─1477 /usr/sbin/apache2 -k start
             ├─1481 /usr/sbin/apache2 -k start
             └─1482 /usr/sbin/apache2 -k start
