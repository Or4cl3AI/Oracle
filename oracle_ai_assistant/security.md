```python
class SecurityModule:
    def __init__(self):
        self.encryption_enabled = True
        self.authentication_enabled = True
        self.authorization_enabled = True

    def enable_encryption(self):
        self.encryption_enabled = True

    def disable_encryption(self):
        self.encryption_enabled = False

    def enable_authentication(self):
        self.authentication_enabled = True

    def disable_authentication(self):
        self.authentication_enabled = False

    def enable_authorization(self):
        self.authorization_enabled = True

    def disable_authorization(self):
        self.authorization_enabled = False

    def encrypt_data(self, data):
        if self.encryption_enabled:
            # Code for data encryption
            pass
        else:
            raise Exception("Encryption is not enabled")

    def authenticate_user(self, username, password):
        if self.authentication_enabled:
            # Code for user authentication
            pass
        else:
            raise Exception("Authentication is not enabled")

    def authorize_user(self, user, resource):
        if self.authorization_enabled:
            # Code for user authorization
            pass
        else:
            raise Exception("Authorization is not enabled")
```
