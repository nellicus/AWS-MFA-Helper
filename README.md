# AWS MFA Helper
Automate obtaining MFA (STS) credentials

This utility will request STS credentials from AWS, then update  ~/.aws/credentials with the new credentials. STS credentials are stored in a profile suffixed with -mfa.

If you have [Keyring TOTP Generator](https://github.com/jjfalling/Keyring-TOTP-Generator) installed this utility will attempt to automate the TOTP code generation.

You will need to update your AWS configuration (~/.aws/config) with the following settings:
```
[profile my-aws-profile]
helper_mfa_serial = (your MFA ARN)
helper_totp_service_name = (Optional: service name in TOTP Generatior)
```


You can install the python dependencies with `pip install -r requirements.txt`.

Run with the --help flag for more information.