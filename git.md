## Git

### Configuration

**Avoid typing credentials or passphrase for RSA too often using cache**

Example for 3 hours
```bash
git config --global credential.helper 'cache --timeout=10800'
```
