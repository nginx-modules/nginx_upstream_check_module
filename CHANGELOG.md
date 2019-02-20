<a name="unreleased"></a>
## [Unreleased]

### Add
- Add https support
- Add prometheus gauge response format
- Add 1.9.2+ support

### Added
- Added index to JSON array of upstream servers
- Added support for upstream hash module

### Adding
- Adding feature for fast mark upstream UP on start if they alive
- Adding in a new 1.7.5+ matching format.

### Bugfix
- Bugfix & Support TLSv1.1+

### Check
- check never again when connect failure occurs

### Created
- created check_1.11.1+.patch

### Expose
- expose api ngx_http_upstream_check_upstream_down

### Fix
- Fix memory leak
- Fix config fail when there is Werror in CC flag

### Fixed
- Fixed the issue where checker is not working properly when check_keepalive_requests is set to greater than 1. The checker will only send the first check request and then wait until the upstream timesout the keepalive link. Fix is based on tengine code from https://github.com/alibaba/tengine

### Formatting
- Formatting code style

### GCC
- GCC compiler Werror-warning unused

### I
- I needed to use the ssl_hello check at a client that uses TLSv1.2 only and has some 2012R2 IIS. This required offering not just TLSv1.2 but also the right ciphers and extensions.

### JSON
- JSON server section with index

### Optimize
- optimize output for nginxupstreambeat

### Output
- Output of the total number of alive and down usptream

### Patch
- Patch for nginx 1.14.0+
- Patch for nginx 1.12.1+

### README
- README using Markdown.

### Read
- Read the entire HTTP header instead of closing connection after HTTP status line.

### Remove
- remove the  upstream_name inherit

### Respin
- Respin patch against nginx v1.11.5

### Return
- Return 204 for status if health check is not configured

### Return
- return 503 if not all upstreams are up

### Show
- Show when the first failure happens in the status matrix.

### Update
- update the README for 0.3.0

### Use
- use SSL_free to free openssl data


<a name="v0.3.0"></a>
## [v0.3.0] - 2014-10-02
### Merge
- merge from development branch


<a name="v0.2.0"></a>
## [v0.2.0] - 2014-10-02
### Added
- Added the patch for nginx-1.7.2+

### Added
- added the patch for nginx-1.5.12+

### Stored
- Stored upstream name of peer in shared memory to avoid false count for same IP in different upstream groups while reloading

### Updated
- updated test cases

### Pull Requests
- Merge pull request [#40](https://github.com/nginx-modules/nginx_upstream_check_module/issues/40) from saravsars/master
- Merge pull request [#34](https://github.com/nginx-modules/nginx_upstream_check_module/issues/34) from jbergstroem/nginx-1.7.2


<a name="v0.1.9"></a>
## [v0.1.9] - 2013-07-14
### Add
- add the docs for 1.2.2+.patch
- add the docs for nginx-sticky-module
- add a new patch for nginx-1.2.1+
- add chomp script

### Added
- added the patch for nginx-1.2.6+ and nginx-1.3.9+
- added the patch for jvm_route module
- added static keyword for some static global variables
- added skip section with least_conn test cases for nginx-1.2.1-
- added the test cases for least_conn
- added the least-conn patch for nginx-1.2.2+
- added the patch for nginx-sticky-module

### Change
- change to srand to srandom
- change the test scripts
- change the get_shm_name function to static string

### Check
- check active close from peer in ngx_http_check_recv_handler()

### Chomp
- chomp the space in the end of line
- chomp the space in the end of line

### Fix
- fix the error type of DEBUG log formats, coding style
- fix the mysql check
- fix a bug of wrong peer number
- fix a bug of untriggered clean event
- fix the coding style
- fix the coding style in the patch
- fix the coding style

### Fixed
- fixed typo
- fixed a segment fault bug with upstream check module when check timeout is longer than the check interval
- fixed docs
- fixed an bug with wrong array index This could cause the connection left in old work process when reloading
- fixed an compile warning in CentOS 5.7 i386
- fixed a memory overflow bug with check_status directive with thousands of check servers

### Inherit
- inherit the peer state from the old shared memory when reload
- inherit the shared memory when you reload nginx

### Merge
- Merge branch 'master' of github.com:yaoweibin/nginx_upstream_check_module

### Remove
- remove the useless code
- remove the status section in the docs
- remove the docs for imap and pop3
- remove the imap and pop3 check method
- remove the dependence with Ragel
- remove the smtp check feature

### Send
- send data later when send() returns zero in ngx_http_check_send_handler()

### Test
- test the zero configure parameter

### Update
- update test scripts version
- update docs

### Updated
- updated the test cases
- updated the docs

### Pull Requests
- Merge pull request [#20](https://github.com/nginx-modules/nginx_upstream_check_module/issues/20) from chobits/master


<a name="v0.1.5"></a>
## [v0.1.5] - 2012-12-21

<a name="0.1.8"></a>
## [0.1.8] - 2012-12-21
### Add
- add the docs for 1.2.2+.patch
- add the docs for nginx-sticky-module
- add a new patch for nginx-1.2.1+

### Added
- added the patch for jvm_route module
- added static keyword for some static global variables
- added skip section with least_conn test cases for nginx-1.2.1-
- added the test cases for least_conn
- added the least-conn patch for nginx-1.2.2+
- added the patch for nginx-sticky-module

### Change
- change to srand to srandom
- change the test scripts
- change the get_shm_name function to static string

### Chomp
- chomp the space in the end of line

### Fix
- fix the error type of DEBUG log formats, coding style
- fix the mysql check
- fix a bug of wrong peer number
- fix a bug of untriggered clean event
- fix the coding style

### Fixed
- fixed typo
- fixed a segment fault bug with upstream check module when check timeout is longer than the check interval
- fixed docs
- fixed an bug with wrong array index This could cause the connection left in old work process when reloading
- fixed an compile warning in CentOS 5.7 i386
- fixed a memory overflow bug with check_status directive with thousands of check servers

### Inherit
- inherit the peer state from the old shared memory when reload
- inherit the shared memory when you reload nginx

### Remove
- remove the useless code
- remove the status section in the docs
- remove the docs for imap and pop3
- remove the imap and pop3 check method
- remove the dependence with Ragel

### Test
- test the zero configure parameter

### Update
- update test scripts version


<a name="v0.1.6"></a>
## [v0.1.6] - 2012-04-18
### Add
- add chomp script
- add the patch for upstream ip_hash and fair module. add test scripts and docs
- add upstream name and remove busyness, access_count in the status page

### Chomp
- chomp the space in the end of line

### Fix
- fix the coding style in the patch
- fix the coding style
- fix an bug when using variable in proxy_pass Thanks to 彭琦(jinglong.pq[@taobao](https://github.com/taobao).com)
- fix the above when without --with-debug
- fix the problem of "-Werror=unused-but-set-variable"
- fix a bug with the option of backup
- fix a bug of segment fault when reloading Thanks to Markus Linnala

### Make
- make it comtiable with c99

### Merge
- Merge branch 'master' of github.com:yaoweibin/nginx_upstream_check_module
- Merge branch 'master' of github.com:yaoweibin/nginx_upstream_check_module

### Mv
- mv wiki to doc

### No
- no touch the shared memory after reloading

### Remove
- remove the smtp check feature

### Update
- update docs


<a name="v0.1.4"></a>
## v0.1.4 - 2010-12-24
### Add
- add the Matthieu to copyright
- add the name of Matthieu to README
- add more test scripts, fix a bug with implicitly defined upstream
- add a MACRO wrapping the patch
- add the option of default_down
- add the README
- add the check type of ajp
- add module.h

### Add
- Add back supervisord support
- Add some return code checking and spealing stuffz
- Add sample mods to README
- Add license to readme
- Add nginx.patch file

### Clarify
- Clarify README file

### Create
- create the upstream_check init main structure

### First
- First commit of upstream healthcheck plugin

### First
- first test succ
- first compile succ

### Fix
- Fix health_status XML
- Fix patch format (issue [#1](https://github.com/nginx-modules/nginx_upstream_check_module/issues/1) in upstream repository).
- Fix build with nginx-0.8.22+.

### Fix
- fix a bug of segment fault after reload
- fix a bug with kqueue, change the test scripts to public domain
- fix a possible bug
- fix the wrong ssl_hello packet
- fix the #issue/1,2,3,4 Thanks to Matthieu Tourne
- fix docs
- fix docs
- fix the problem with ngx_log_debug
- fix a bug of default type. Add test scripts

### Make
- Make it work with kqueue (by sending request after we connect).
- Make it work with ngx_supervisord.
- Make it work with standard round-robin and ip_hash load banalcers.

### Make
- make nginx-0.8.22+ happy

### Merge
- Merge remote branch 'remotes/piotr/master'
- Merge remote branch 'remotes/piotr/master'
- Merge commit 'upstream/master'

### Minor
- Minor debug changes with an extra state

### Modify
- modify the peers_conf -> peers, peer_conf -> peer

### Reduce
- reduce the patch, move the main configration and server configration

### Tidy
- tidy the source

### Update
- Update docs and health title

### Update
- update README

### Use
- use the ngx_http_conf_upstream_srv_conf to get the server configration

### Use
- Use <td> correctly


[Unreleased]: https://github.com/nginx-modules/nginx_upstream_check_module/compare/v0.3.0...HEAD
[v0.3.0]: https://github.com/nginx-modules/nginx_upstream_check_module/compare/v0.2.0...v0.3.0
[v0.2.0]: https://github.com/nginx-modules/nginx_upstream_check_module/compare/v0.1.9...v0.2.0
[v0.1.9]: https://github.com/nginx-modules/nginx_upstream_check_module/compare/v0.1.5...v0.1.9
[v0.1.5]: https://github.com/nginx-modules/nginx_upstream_check_module/compare/0.1.8...v0.1.5
[0.1.8]: https://github.com/nginx-modules/nginx_upstream_check_module/compare/v0.1.6...0.1.8
[v0.1.6]: https://github.com/nginx-modules/nginx_upstream_check_module/compare/v0.1.4...v0.1.6
