#### Parser Content
```Java
{
Name = secureauth-login-xml-app-authentication-browserfingerprint
  ParserVersion = v1.0.0
  Vendor = SecureAuth
  Product = SecureAuth Login
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """<UserID>""", """: State [INIT_LOGON]""", """<Category>DEBUG</Category>""", """AllowedTokens = BROWSERFINGERPRINT""" ]
  Fields = [
    """Host\s=\s({host}[^;]+)""",
    """<Category>({category}[^<]+)""",
    """User-Agent\s=\s({user_agent}.+?);\s*CompanyID\s=""",
    """CompanyID\s=\s({company}.+)\sCookieName\s=""",
# cookie is removed
  ]


}
```