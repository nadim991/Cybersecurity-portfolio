# Web Security Findings

## Target

Target: Metasploitable2
IP: 192.168.196.129
Testing Environment: Local VMware Lab

## 1. Web Server Information

The target is running:

Apache 2.2.8 (Ubuntu)
PHP 5.2.4-2ubuntu5.10
WebDAV/2

The HTTP service responded with HTTP 200 OK.

## 2. HTTP OPTIONS

A request to the root directory using the OPTIONS method returned HTTP 200 OK.

The response did not expose an Allow header for the root directory.

## 3. WebDAV Enabled

The /dav/ directory supports WebDAV.

The server returned:

DAV: 1,2
MS-Author-Via: DAV

Allowed methods included:

OPTIONS
GET
HEAD
POST
DELETE
TRACE
PROPFIND
PROPPATCH
COPY
MOVE
LOCK
UNLOCK

## 4. WebDAV File Upload Testing

davtest successfully created a test directory:

/dav/DavTestDir_huWkQDeB

Multiple file types could be uploaded using the PUT method.

The test included:

.aspx
.shtml
.pl
.php
.jsp
.asp
.cgi
.txt
.jhtml
.html
.cfm

## 5. File Execution

The PHP test file was reported as executable by davtest.

The TXT and HTML test files were also reported as executable.

Other tested file types failed execution.

## Security Impact

The ability to upload files through WebDAV increases the attack surface.

The successful PHP execution result is particularly significant because a server-side PHP file could potentially execute on the web server.

## Recommendation

Disable WebDAV if it is not required.

Restrict PUT and other write methods.

Require authentication and authorization for WebDAV.

Prevent execution of uploaded files.

Restrict WebDAV access to trusted users and networks.

Monitor uploaded files and WebDAV activity.