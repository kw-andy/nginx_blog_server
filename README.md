# Nginx Site Configuration and Activation

## Commands to Execute

### 1. View the configuration file
```bash
sudo cat /etc/nginx/sites-available/stat.just-go.dev
```

### 2. Enable the site by creating a symbolic link
```bash
sudo ln -sf /etc/nginx/sites-available/stat.just-go.dev /etc/nginx/sites-enabled/stat.just-go.dev
```

### 3. Test configuration and reload nginx
```bash
sudo nginx -t && sudo systemctl reload nginx
```

## Additional Verification Steps

### Check if config file exists
```bash
ls -la /etc/nginx/sites-available/stat.just-go.dev
```

### Remove conflicting enabled sites (if needed)
```bash
sudo rm -f /etc/nginx/sites-enabled/stat.just-go.dev
```

### Verify symbolic link creation
```bash
ls -la /etc/nginx/sites-enabled/ | grep stat.just-go.dev
```

### Check nginx status after reload
```bash
sudo systemctl status nginx
```

## Potential Missing Steps Analysis

**What you have:**
1. ✅ View the config file
2. ✅ Create symbolic link to enable the site
3. ✅ Test config and reload nginx

**What might be missing:**
- Configuration file verification
- Conflicting site removal
- Post-reload status check
- DNS and firewall considerations
- SSL certificate validation (if using HTTPS)
