*) Upgraded OpenSSL to 3.5.9 from 3.5.8 (Changelog)

  *) Upgraded pcre2 to 10.49 from 10.48 (Changelog)

  *) Upgraded expat to 2.8.5 from 2.8.4  (Changelog)

ASF changes:

  *) SECURITY: CVE-2026-93546: mod_dav_fs namespace overflow
    (cve.mitre.org)
    Integer overflow in mod_dav_fs in Apache HTTP Server through
    2.4.68 allows an authenticated WebDAV client with write access
    to crash worker processes and persistently corrupt a directory's
    property database via PROPPATCH requests declaring many XML
    namespaces.
    Credits: Zhen Kong

  *) SECURITY: CVE-2026-79768: mod_userdir information disclosure
    (cve.mitre.org)
    Path equivalence: '/./' (single dot directory) vulnerability in
    Apache HTTP Server's mod_userdir module when configured
    with absolute non-wildcard UserDir directive (the 2nd form
    in https://httpd.apache.org/docs/2.4/mod/mod_userdir.html#userdir)
    This issue affects Apache HTTP Server: from 2.4.0 through 2.4.68.
    Credits: Vlatko Kosturjak, Marlink Cyber

  *) SECURITY: CVE-2026-73637: mod_auth_digest DoS attack
    (cve.mitre.org)
    Use after free in mod_auth_digest in Apache Software Foundation
    Apache HTTP Server before 2.4.69 on all platforms allows an
    unauthenticated remote client to cause authentication state
    corruption via concurrent Digest authentication requests when
    AuthDigestNcCheck is enabled or AuthDigestNonceLifetime is set
    to 0.
    Users are recommended to upgrade to version 2.4.69, which fixes
    this issue.
    Credits: Zhen Kong