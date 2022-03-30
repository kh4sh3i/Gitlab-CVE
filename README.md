# Gitlab-CVE
a Curated list of gitlab vulnerability



## CVE-2021-22205 [critical]
An issue has been discovered in GitLab CE/EE affecting all versions starting from 11.9. GitLab was not properly validating image files that were passed to a file parser which resulted in a remote command execution.

```
https://target.com/users/sign_in
```

## CVE-2021-22214 [high]
The remote GitLab install contains a Server-side request forgery (SSRF) vulnerability as a result of the internal network for webhooks being enabled. A remote, unauthenticated attacker can exploit a registration-limited GitLab instance causing it to make HTTP requests to an arbitrary domain of the attacker's choosing.

```
http://target.com/api/v4/ci/lint?include_merged_yaml=true
```


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


## CVE-2020-26413 [medium]
Information disclosure via GraphQL results in user email being unexpectedly visible.
```
http://target.com/api/graphql [test@gmail.com]
```


## reference
* [GitLab-SSRF-CVE-2021-22214](https://github.com/kh4sh3i/GitLab-SSRF-CVE-2021-22214)
* [CVE-2021-22205](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-22205)
* [CVE-2021-4191](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-4191)
* [CVE-2020-26413](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2020-26413)
