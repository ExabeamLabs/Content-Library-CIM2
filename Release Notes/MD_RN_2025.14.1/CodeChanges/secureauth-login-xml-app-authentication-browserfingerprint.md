# Code Changes for secureauth-login-xml-app-authentication-browserfingerprint (Parser)

| Code Change | Field Name | 2025.13.1 | 2025.14.1 |
|-------------|------------|-----------|------------|
| removed_parser | N/A | {"Name": "secureauth-login-xml-app-authentication-browserfingerprint", "ParserVersion": "v1.0.0", "Vendor": "SecureAuth", "Product": "SecureAuth Login", "TimeFormat": "yyyy-MM-dd HH:mm:ss", "Conditions": ["<UserID>", ": State [INIT_LOGON]", "<Category>DEBUG</Category>", "AllowedTokens = BROWSERFINGERPRINT"], "Fields": ["Host\s=\s({host}[^;]+)", "<Category>({category}[^<]+)", "User-Agent\s=\s({user_agent}.+?);\s*CompanyID\s=", "CompanyID\s=\s({company}.+)\sCookieName\s="]} | N/A |