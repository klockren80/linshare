
# Using OIDC and LDAP server as user providers for domain  to search  users

When you configure the domain user provider as OIDC provider you will face the problem when you share file with another internal user that is not already authenticated and in this case he will be considered as external or guest user.

You can avoid this problem by :

1- Creating a new LDAP connection (UI-Admin -> Configuration -> Remote servers) and set LDAP information.
2- Creating new User filter (UI-Admin -> Configuration -> User filters) and set LDAP information.

After that you should add those lines in linshare.properties :

### Update `linshare.properties` guide

Two properties have been introduced:
```
oidc.ldap.connectionUuid=76ef5ee0-6513-4a64-b711-90a1bbdbfc55
oidc.ldap.provider.patternUuid=cd02e600-f324-4cea-9724-21d8647e9533
```
They allow to link every oidc connection to a ldap connection and pattern to be used as backup user provider (to retrieve client informations if absent from the DB)
