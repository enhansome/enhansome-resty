# awesome-resty with stars

A List of OpenResty / Nginx modules, Lua libraries, and related resources.

## What is OpenResty

![OpenResty Logo](https://github.com/bungle/awesome-resty/raw/master/images/logo.png)

OpenResty is a full-fledged web platform by integrating the standard Nginx core, LuaJIT, many carefully written Lua libraries, lots of high quality 3rd-party Nginx modules, and most of their external dependencies. It is designed to help developers easily build scalable web applications, web services, and dynamic web gateways.

By taking advantage of various well-designed Nginx modules (most of which are developed by the OpenResty team themselves), OpenResty effectively turns the nginx server into a powerful web app server, in which the web developers can use the Lua programming language to script various existing nginx C modules and Lua modules and construct extremely high-performance web applications that are capable to handle 10K \~ 1000K+ connections in a single box.

OpenResty aims to run your server-side web app completely in the Nginx server, leveraging Nginx's event model to do non-blocking I/O not only with the HTTP clients, but also with remote backends like MySQL, PostgreSQL, Memcached, and Redis.

Real-world applications of OpenResty range from dynamic web portals and web gateways, web application firewalls, web service platforms for mobile apps/advertising/distributed storage/data analytics, to full-fledged dynamic web applications and web sites. The hardware used to run OpenResty also ranges from very big metals to embedded devices with very limited resources. It is not uncommon for our production users to serve billions of requests daily for millions of active users with just a handful of machines.

OpenResty is not an Nginx fork. It is just a software bundle. Most of the patches applied to the Nginx core in OpenResty have already been submitted to the official Nginx team and most of the patches submitted have also been accepted. We are trying hard not to fork Nginx and always to use the latest best Nginx core from the official Nginx team.

## Official Channels

* Web Site: <http://openresty.org/>
* Mailing List: <https://groups.google.com/forum/#!forum/openresty-en> ([Chinese List](https://groups.google.com/forum/#!forum/openresty))
* Github Organization: <https://github.com/openresty>
* Lead Developer: [@agentzh](https://github.com/agentzh)
* OpenResty Package Manager (`opm`): [package repository](https://opm.openresty.org/), [opm sources](https://github.com/openresty/opm) ⭐ 486 | 🐛 30 | 🌐 Lua | 📅 2026-08-13

## How to Contribute on this List?

There are at least three different ways to contribute:

1. [Create a New Issue](https://github.com/bungle/awesome-resty/issues/new) ⭐ 2,482 | 🐛 2 | 📅 2026-05-26 where you describe the needed additions, deletions or changes.
2. [Fork this repository](https://github.com/bungle/awesome-resty/fork) ⭐ 2,482 | 🐛 2 | 📅 2026-05-26 and make the changes, and create a pull request.
3. [Post a reply](https://groups.google.com/forum/#!topic/openresty-en/VSj4_8GNORI) in the awesome-resty thread in openresty-en mailing list.

## Contents

* [Modules](#modules)
  * [Core Modules](#core-modules)
  * [Core Nginx Modules](#core-nginx-modules)
  * [Third-party Nginx Modules](#third-party-nginx-modules)
* [Libraries](#libraries)
  * [Core Libraries](#core-libraries)
  * [Web Frameworks](#web-frameworks)
  * [Web Development Essentials](#web-development-essentials)
  * [Routing Libraries](#routing-libraries)
  * [Traffic Management](#traffic-management)
  * [Request Argments Parsers](#request-argments-parsers)
  * [Middleware and API Tools](#middleware-and-api-tools)
  * [Templating](#templating)
  * [Validation](#validation)
  * [Authentication and Authorization](#authentication-and-authorization)
  * [Cryptography](#cryptography)
  * [Networking](#networking)
  * [Databases and Storages](#databases-and-storages)
  * [Testing and Profiling](#testing-and-profiling)
  * [Message Queuing and Task Management](#message-queuing-and-task-management)
  * [Bar Codes and QR Codes](#bar-codes-and-qr-codes)
  * [Utilities](#utilities)
  * [Date and Time](#date-and-time)
  * [Compression](#compression)
  * [Text Formats](#text-formats)
  * [Binary Formats](#binary-formats)
  * [Document Formats](#document-formats)
  * [Image Formats](#image-formats)
  * [Localization](#localization)
  * [Caching](#caching)
  * [Metrics and Statistics](#metrics-and-statistics)
  * [Logging](#logging)
  * [Functional Programming](#functional-programming)
  * [Web APIs](#web-apis)
  * [Security](#security)
  * [Other Sources for Libraries](#other-sources-for-libraries)
* [Books and Tutorials](#books-and-tutorials)
  * [Books](#books)
  * [Tutorials and Guides](#tutorials-and-guides)
* [Videos](#videos)
* [Conferences, Workshops and Events](#conferences-workshops-and-events)
* [Demo Applications](#demo-applications)
* [See Also](#see-also)
* [License](#license)

## Modules

#### Core Modules

Core modules come bundled in OpenResty package.

* [ngx\_openresty](https://github.com/openresty/openresty) ⭐ 14,002 | 🐛 332 | 🌐 C | 📅 2026-08-14 — Turning Nginx into a full-fledged Web App Server - Sources for OpenResty Bundle Generation
* [lua-nginx-module](https://github.com/openresty/lua-nginx-module) ⭐ 11,787 | 🐛 392 | 🌐 C | 📅 2026-08-14 — Embed the power of Lua into Nginx
* [headers-more-nginx-module](https://github.com/openresty/headers-more-nginx-module) ⭐ 1,783 | 🐛 52 | 🌐 C | 📅 2026-07-17 — Set and clear input and output headers...more than "add"!
* [echo-nginx-module](https://github.com/openresty/echo-nginx-module) ⭐ 1,193 | 🐛 32 | 🌐 C | 📅 2026-07-17 — An Nginx module for bringing the power of "echo", "sleep", "time" and more to Nginx's config file
* [ngx\_devel\_kit](https://github.com/simpl/ngx_devel_kit) ⭐ 1,027 | 🐛 4 | 🌐 C | 📅 2025-02-20 — an Nginx module that adds additional generic tools that module developers can use in their own modules
* [redis2-nginx-module](https://github.com/openresty/redis2-nginx-module) ⭐ 905 | 🐛 29 | 🌐 C | 📅 2026-07-17 — Nginx upstream module for the Redis 2.0 protocol
* [stream-lua-nginx-module](https://github.com/openresty/stream-lua-nginx-module) ⭐ 750 | 🐛 49 | 🌐 C | 📅 2026-07-17 — Embed the power of Lua into Nginx stream/TCP Servers
* [ngx\_postgres](https://github.com/FRiCKLE/ngx_postgres) ⭐ 551 | 🐛 37 | 🌐 C | 📅 2020-09-29 — Upstream module that allows Nginx to communicate directly with PostgreSQL database
* [lua-upstream-nginx-module](https://github.com/openresty/lua-upstream-nginx-module) ⭐ 511 | 🐛 27 | 🌐 C | 📅 2026-07-17 — Nginx C module to expose Lua API to ngx\_lua for Nginx upstreams
* [srcache-nginx-module](https://github.com/openresty/srcache-nginx-module) ⭐ 486 | 🐛 28 | 🌐 C | 📅 2026-07-17 — Transparent subrequest-based caching layout for arbitrary nginx locations
* [set-misc-nginx-module](https://github.com/openresty/set-misc-nginx-module) ⭐ 402 | 🐛 17 | 🌐 C | 📅 2026-07-17 — Various set\_xxx directives added to nginx's rewrite module (md5/sha1, sql/json quoting, and many more)
* [drizzle-nginx-module](https://github.com/openresty/drizzle-nginx-module) ⭐ 335 | 🐛 14 | 🌐 C | 📅 2026-07-17 — An Nginx upstream module that talks to mysql and drizzle by libdrizzle
* [memc-nginx-module](https://github.com/openresty/memc-nginx-module) ⭐ 213 | 🐛 11 | 🌐 C | 📅 2026-07-17 — An extended version of the standard memcached module that supports set, add, delete, and many more memcached commands
* [encrypted-session-nginx-module](https://github.com/openresty/encrypted-session-nginx-module) ⭐ 203 | 🐛 19 | 🌐 C | 📅 2026-07-17 — Encrypt and decrypt Nginx variable values
* [rds-json-nginx-module](https://github.com/openresty/rds-json-nginx-module) ⭐ 154 | 🐛 4 | 🌐 C | 📅 2026-07-17 — An nginx output filter that formats Resty DBD Streams generated by ngx\_drizzle and others to JSON
* [xss-nginx-module](https://github.com/openresty/xss-nginx-module) ⭐ 151 | 🐛 2 | 🌐 C | 📅 2026-07-17 — Native support for cross-site scripting (XSS) in an nginx
* [form-input-nginx-module](https://github.com/calio/form-input-nginx-module) ⭐ 119 | 🐛 3 | 🌐 Perl | 📅 2017-10-27 — This is a nginx module that reads HTTP POST and PUT request body encoded in "application/x-www-form-urlencoded", and parse the arguments in request body into nginx variables.
* [array-var-nginx-module](https://github.com/openresty/array-var-nginx-module) ⭐ 68 | 🐛 2 | 🌐 C | 📅 2026-07-17 — Add support for array variables to nginx config files
* [ngx\_coolkit](https://github.com/FRiCKLE/ngx_coolkit) ⭐ 56 | 🐛 2 | 🌐 C | 📅 2017-02-05 — Collection of small and useful nginx add-ons
* [rds-csv-nginx-module](https://github.com/openresty/rds-csv-nginx-module) ⭐ 21 | 🐛 2 | 🌐 C | 📅 2026-07-17 — Nginx output filter module to convert Resty-DBD-Streams (RDS) to Comma-Separated Values (CSV)

Please also note that there is **`resty`** command line client included in OpenResty bundle. The [command line client sources](https://github.com/openresty/resty-cli) ⭐ 269 | 🐛 11 | 🌐 Perl | 📅 2026-07-17 can be found on Github.

#### Core Nginx Modules

To learn more about Nginx Core Modules, please refer [Nginx Documentation](http://nginx.org/en/docs/). Some modules that come with Nginx are (not all of them are build by default):

* [ngx\_http\_core\_module](http://nginx.org/en/docs/http/ngx_http_core_module.html)
* [ngx\_http\_ssl\_module](http://nginx.org/en/docs/http/ngx_http_ssl_module.html) — The ngx\_http\_ssl\_module module provides the necessary support for HTTPS
* [ngx\_http\_v2\_module](https://nginx.org/en/docs/http/ngx_http_v2_module.html) — The ngx\_http\_v2\_module module provides support for HTTP/2
* [ngx\_http\_realip\_module](http://nginx.org/en/docs/http/ngx_http_realip_module.html) — The ngx\_http\_realip\_module module is used to change the client address and optional port to the one sent in the specified header fields
* [ngx\_http\_addition\_module](http://nginx.org/en/docs/http/ngx_http_addition_module.html) — The ngx\_http\_addition\_module module is a filter that adds text before and after a response
* [ngx\_http\_xslt\_module](http://nginx.org/en/docs/http/ngx_http_xslt_module.html) — The ngx\_http\_xslt\_module is a filter that transforms XML responses using one or more XSLT stylesheet
* [ngx\_http\_image\_filter\_module](http://nginx.org/en/docs/http/ngx_http_image_filter_module.html) — The ngx\_http\_image\_filter\_module module is a filter that transforms images in JPEG, GIF, and PNG formats
* [ngx\_http\_geoip\_module](http://nginx.org/en/docs/http/ngx_http_geoip_module.html) — The ngx\_http\_geoip\_module module creates variables with values depending on the client IP address, using the precompiled MaxMind databases
* [ngx\_http\_sub\_module](http://nginx.org/en/docs/http/ngx_http_sub_module.html) — The ngx\_http\_sub\_module module is a filter that modifies a response by replacing one specified string by another
* [ngx\_http\_dav\_module](http://nginx.org/en/docs/http/ngx_http_dav_module.html) — The ngx\_http\_dav\_module module is intended for file management automation via the WebDAV protocol. The module processes HTTP and WebDAV methods PUT, DELETE, MKCOL, COPY, and MOVE
* [ngx\_http\_flv\_module](http://nginx.org/en/docs/http/ngx_http_flv_module.html) — The ngx\_http\_flv\_module module provides pseudo-streaming server-side support for Flash Video (FLV) files
* [ngx\_http\_mp4\_module](http://nginx.org/en/docs/http/ngx_http_mp4_module.html) — The ngx\_http\_mp4\_module module provides pseudo-streaming server-side support for MP4 files. Such files typically have the .mp4, .m4v, or .m4a filename extensions
* [ngx\_http\_gunzip\_module](http://nginx.org/en/docs/http/ngx_http_gunzip_module.html) — The ngx\_http\_gunzip\_module module is a filter that decompresses responses with “Content-Encoding: gzip” for clients that do not support “gzip” encoding method. The module will be useful when it is desirable to store data compressed to save space and reduce I/O costs
* [ngx\_http\_gzip\_static\_module](http://nginx.org/en/docs/http/ngx_http_gzip_static_module.html) — The ngx\_http\_gzip\_static\_module module allows sending precompressed files with the “.gz” filename extension instead of regular files
* [ngx\_http\_auth\_request\_module](http://nginx.org/en/docs/http/ngx_http_auth_request_module.html) — The ngx\_http\_auth\_request\_module module implements client authorization based on the result of a subrequest
* [ngx\_http\_random\_index\_module](http://nginx.org/en/docs/http/ngx_http_random_index_module.html) — The ngx\_http\_random\_index\_module module processes requests ending with the slash character (‘/’) and picks a random file in a directory to serve as an index file
* [ngx\_http\_secure\_link\_module](http://nginx.org/en/docs/http/ngx_http_secure_link_module.html) — The ngx\_http\_secure\_link\_module module (0.7.18) is used to check authenticity of requested links, protect resources from unauthorized access, and limit link lifetime
* [ngx\_http\_slice\_module](https://nginx.org/en/docs/http/ngx_http_slice_module.html) — The ngx\_http\_slice\_module module is a filter that splits a request into subrequests, each returning a certain range of response
* [ngx\_http\_stub\_status\_module](https://nginx.org/en/docs/http/ngx_http_stub_status_module.html) — The ngx\_http\_stub\_status\_module module provides access to basic status information
* [ngx\_http\_charset\_module](http://nginx.org/en/docs/http/ngx_http_charset_module.html) — The ngx\_http\_charset\_module module adds the specified charset to the “Content-Type” response header field
* [ngx\_http\_gzip\_module](http://nginx.org/en/docs/http/ngx_http_gzip_module.html) — The ngx\_http\_gzip\_module module is a filter that compresses responses using the “gzip” method
* [ngx\_http\_ssi\_module](http://nginx.org/en/docs/http/ngx_http_ssi_module.html) — The ngx\_http\_ssi\_module module is a filter that processes SSI (Server Side Includes) commands in responses passing through it
* [ngx\_http\_userid\_module](http://nginx.org/en/docs/http/ngx_http_userid_module.html) — The ngx\_http\_userid\_module module sets cookies suitable for client identification
* [ngx\_http\_access\_module](http://nginx.org/en/docs/http/ngx_http_access_module.html) — The ngx\_http\_access\_module module allows limiting access to certain client addresses
* [ngx\_http\_auth\_basic\_module](http://nginx.org/en/docs/http/ngx_http_auth_basic_module.html) — The ngx\_http\_auth\_basic\_module module allows limiting access to resources by validating the user name and password using the “HTTP Basic Authentication” protocol
* [ngx\_http\_autoindex\_module](http://nginx.org/en/docs/http/ngx_http_autoindex_module.html) — The ngx\_http\_autoindex\_module module processes requests ending with the slash character (‘/’) and produces a directory listing
* [ngx\_http\_geo\_module](http://nginx.org/en/docs/http/ngx_http_geo_module.html) — The ngx\_http\_geo\_module module creates variables with values depending on the client IP address
* [ngx\_http\_map\_module](http://nginx.org/en/docs/http/ngx_http_map_module.html) — The ngx\_http\_map\_module module creates variables whose values depend on values of other variables
* [ngx\_http\_split\_clients\_module](http://nginx.org/en/docs/http/ngx_http_split_clients_module.html) — The ngx\_http\_split\_clients\_module module creates variables suitable for A/B testing, also known as split testing
* [ngx\_http\_referer\_module](http://nginx.org/en/docs/http/ngx_http_referer_module.html) — The ngx\_http\_referer\_module module is used to block access to a site for requests with invalid values in the “Referer” header field
* [ngx\_http\_rewrite\_module](http://nginx.org/en/docs/http/ngx_http_rewrite_module.html) — The ngx\_http\_rewrite\_module module is used to change request URI using PCRE regular expressions, return redirects, and conditionally select configurations
* [ngx\_http\_proxy\_module](http://nginx.org/en/docs/http/ngx_http_proxy_module.html) — The ngx\_http\_proxy\_module module allows passing requests to another server
* [ngx\_http\_fastcgi\_module](http://nginx.org/en/docs/http/ngx_http_fastcgi_module.html) — The ngx\_http\_fastcgi\_module module allows passing requests to a FastCGI server
* [ngx\_http\_uwsgi\_module](http://nginx.org/en/docs/http/ngx_http_uwsgi_module.html) — The ngx\_http\_uwsgi\_module module allows passing requests to a uwsgi server
* [ngx\_http\_scgi\_module](http://nginx.org/en/docs/http/ngx_http_scgi_module.html) — The ngx\_http\_scgi\_module module allows passing requests to an SCGI server
* [ngx\_http\_memcached\_module](http://nginx.org/en/docs/http/ngx_http_memcached_module.html) — he ngx\_http\_memcached\_module module is used to obtain responses from a memcached server
* [ngx\_http\_limit\_conn\_module](http://nginx.org/en/docs/http/ngx_http_limit_conn_module.html) — The ngx\_http\_limit\_conn\_module module is used to limit the number of connections per the defined key, in particular, the number of connections from a single IP address
* [ngx\_http\_limit\_req\_module](http://nginx.org/en/docs/http/ngx_http_limit_req_module.html) — he ngx\_http\_limit\_req\_module module is used to limit the request processing rate per a defined key, in particular, the processing rate of requests coming from a single IP address
* [ngx\_http\_empty\_gif\_module](http://nginx.org/en/docs/http/ngx_http_empty_gif_module.html) — The ngx\_http\_empty\_gif\_module module emits single-pixel transparent GIF
* [ngx\_http\_browser\_module](http://nginx.org/en/docs/http/ngx_http_browser_module.html) — The ngx\_http\_browser\_module module creates variables whose values depend on the value of the “User-Agent” request header field
* [ngx\_http\_upstream\_module](http://nginx.org/en/docs/http/ngx_http_upstream_module.html) — <http://nginx.org/en/docs/http/ngx_http_upstream_module.html>
* [ngx\_http\_perl\_module](http://nginx.org/en/docs/http/ngx_http_perl_module.html) — The ngx\_http\_perl\_module module is used to implement location and variable handlers in Perl and insert Perl calls into SSI
* [ngx\_mail\_core\_module](http://nginx.org/en/docs/mail/ngx_mail_core_module.html)
* [ngx\_mail\_ssl\_module](http://nginx.org/en/docs/mail/ngx_mail_ssl_module.html) — The ngx\_mail\_ssl\_module module provides the necessary support for a mail proxy server to work with the SSL/TLS protocol
* [ngx\_mail\_smtp\_module](http://nginx.org/en/docs/mail/ngx_mail_smtp_module.html)
* [ngx\_mail\_imap\_module](http://nginx.org/en/docs/mail/ngx_mail_imap_module.html)
* [ngx\_mail\_pop3\_module](http://nginx.org/en/docs/mail/ngx_mail_pop3_module.html)
* [ngx\_stream\_core\_module](http://nginx.org/en/docs/stream/ngx_stream_core_module.html)
* [ngx\_stream\_ssl\_module](http://nginx.org/en/docs/stream/ngx_stream_ssl_module.html) — The ngx\_stream\_ssl\_module module provides the necessary support for a stream proxy server to work with the SSL/TLS protocol
* [ngx\_stream\_proxy\_module](http://nginx.org/en/docs/stream/ngx_stream_proxy_module.html) — The ngx\_stream\_proxy\_module module allows proxying data streams over TCP, UDP, and UNIX-domain sockets

#### Third-party Nginx Modules

* [NAXSI](https://github.com/nbs-system/naxsi) ⚠️ Archived — NAXSI is an open-source, high performance, low rules maintenance WAF for NGINX; NAXSI means Nginx Anti Xss & Sql Injection
* [ngx\_pagespeed](http://ngxpagespeed.com/) ([Github](https://github.com/pagespeed/ngx_pagespeed) ⚠️ Archived) — Automatic PageSpeed optimization module for Nginx
* [nchan](https://nchan.io/) ([Github](https://github.com/slact/nchan) ⭐ 3,064 | 🐛 128 | 🌐 C | 📅 2026-06-09) — Fast, horizontally scalable, multiprocess pub/sub queuing server and proxy for HTTP, long-polling, Websockets and EventSource (SSE)
* [nginx-upsync-module](https://github.com/weibocom/nginx-upsync-module) ⭐ 1,847 | 🐛 76 | 🌐 C | 📅 2023-04-07 — Nginx C module, syncing upstreams from consul or others, dynamiclly adjusting backend servers weight, needn't reload nginx
* [ngx\_lua\_ipc](https://github.com/slact/ngx_lua_ipc) ⭐ 109 | 🐛 3 | 🌐 C | 📅 2019-07-31 — Interprocess communication for Lua Nginx Module and OpenResty — send named alerts with string data between Nginx worker processes
* [lua-var-nginx-module](https://github.com/api7/lua-var-nginx-module) ⭐ 57 | 🐛 2 | 🌐 Perl | 📅 2022-07-27 — Fetchs Nginx variable by Luajit with FFI way which is fast and cheap
* [sass-nginx-module](https://github.com/mneudert/sass-nginx-module) ⭐ 39 | 🐛 0 | 🌐 Perl | 📅 2020-05-03 — Syntactically Awesome Nginx Module
* [ModSecurity](https://www.modsecurity.org/) — Open Source Web Application Firewall
* [More 3rd Party Modules](https://www.nginx.com/resources/wiki/modules/)

## Libraries

#### Core Libraries

Core Libraries are bundled in OpenResty package, and you don't need to separately install them.

* [lua-resty-redis](https://github.com/openresty/lua-resty-redis) ⭐ 1,956 | 🐛 75 | 🌐 Lua | 📅 2026-07-17 — Lua Redis client driver for the ngx\_lua based on the cosocket API
* [lua-resty-core](https://github.com/openresty/lua-resty-core) ⭐ 854 | 🐛 71 | 🌐 Lua | 📅 2026-07-17 — New FFI-based Lua API for the ngx\_lua module
* [lua-resty-mysql](https://github.com/openresty/lua-resty-mysql) ⭐ 726 | 🐛 54 | 🌐 Lua | 📅 2026-06-20 — Non-blocking Lua MySQL client driver for ngx\_lua based on the cosocket API
* [lua-resty-upstream-healthcheck](https://github.com/openresty/lua-resty-upstream-healthcheck) ⭐ 544 | 🐛 47 | 🌐 Lua | 📅 2026-07-17 — Health Checker for Nginx Upstream Servers in Pure Lua
* [lua-resty-websocket](https://github.com/openresty/lua-resty-websocket) ⭐ 523 | 🐛 32 | 🌐 Lua | 📅 2026-08-17 — Lua WebSocket implementation for the ngx\_lua module
* [lua-cjson](https://github.com/openresty/lua-cjson) ⭐ 498 | 🐛 27 | 🌐 C | 📅 2026-06-28 — Lua cJSON is a fast JSON encoding / parsing module for Lua
* [lua-resty-lrucache](https://github.com/openresty/lua-resty-lrucache) ⭐ 460 | 🐛 15 | 🌐 Lua | 📅 2026-07-17 — Lua-land LRU Cache based on LuaJIT FFI
* [lua-resty-string](https://github.com/openresty/lua-resty-string) ⭐ 443 | 🐛 26 | 🌐 Lua | 📅 2026-07-17 — String utilities and common hash functions for ngx\_lua and LuaJIT
* [lua-resty-upload](https://github.com/openresty/lua-resty-upload) ⭐ 414 | 🐛 19 | 🌐 Lua | 📅 2026-07-17 — Streaming reader and parser for HTTP file uploading based on ngx\_lua cosocket
* [lua-resty-dns](https://github.com/openresty/lua-resty-dns) ⭐ 338 | 🐛 17 | 🌐 Lua | 📅 2026-07-17 — DNS resolver for the Nginx Lua module
* [lua-resty-lock](https://github.com/openresty/lua-resty-lock) ⭐ 323 | 🐛 9 | 🌐 Lua | 📅 2026-07-17 — Simple nonblocking lock API for ngx\_lua based on shared memory dictionaries
* [lua-resty-memcached](https://github.com/openresty/lua-resty-memcached) ⭐ 216 | 🐛 8 | 🌐 Lua | 📅 2026-07-17 — Lua memcached client driver for the ngx\_lua based on the cosocket API
* [lua-resty-shell](https://github.com/openresty/lua-resty-shell) ⭐ 133 | 🐛 7 | 🌐 Raku | 📅 2026-07-17 — Lua module for nonblocking system shell command executions
* [lua-tablepool](https://github.com/openresty/lua-tablepool) ⭐ 122 | 🐛 1 | 🌐 Raku | 📅 2026-07-17 — Lua table recycling pools for LuaJIT
* [lua-redis-parser](https://github.com/openresty/lua-redis-parser) ⭐ 94 | 🐛 3 | 🌐 C | 📅 2026-05-14 — Redis reply parser and request constructor library for Lua
* [lua-resty-signal](https://github.com/openresty/lua-resty-signal) ⭐ 34 | 🐛 2 | 🌐 Raku | 📅 2026-07-17 — Lua library for killing or sending signals to Linux processes
* [lua-resty-shdict-simple](https://github.com/openresty/lua-resty-shdict-simple) ⭐ 33 | 🐛 0 | 🌐 Perl | 📅 2026-05-07 — Simple applicaton-oriented interface to the OpenResty shared dictionary API
* [lua-resty-memcached-shdict](https://github.com/openresty/lua-resty-memcached-shdict) ⭐ 33 | 🐛 0 | 🌐 Lua | 📅 2019-01-15 — Powerful memcached client with a shdict caching layer and many other features
* [lua-resty-resolver](https://github.com/jkeys089/lua-resty-resolver) ⭐ 29 | 🐛 4 | 🌐 Raku | 📅 2025-06-23 — Caching DNS resolver for ngx\_lua and LuaJIT
* [lua-rds-parser](https://github.com/openresty/lua-rds-parser) ⭐ 20 | 🐛 1 | 🌐 C | 📅 2026-05-14 — Resty-DBD-Stream (RDS) parser for Lua written in C

#### Web Frameworks

* [Vanilla](https://github.com/idevz/vanilla) ⭐ 1,038 | 🐛 3 | 🌐 Perl | 📅 2019-01-09 — An OpenResty Web Framework
* [lor](http://lor.sumory.com/) ([Github](https://github.com/sumory/lor) ⭐ 1,018 | 🐛 12 | 🌐 Lua | 📅 2024-01-02) — A fast and minimalist web framework based on OpenResty
* [Sailor](https://github.com/sailorproject/sailor) ⭐ 935 | 🐛 48 | 🌐 Lua | 📅 2022-10-28 — A Lua MVC Web Framework
* [GIN](https://github.com/ostinelli/gin) ⭐ 240 | 🐛 4 | 🌐 Lua | 📅 2025-12-17 — A fast, low-latency, low-memory footprint, web JSON-API framework with Test Driven Development helpers and patterns
* [MOOCHINE](https://github.com/appwilldev/moochine) ⭐ 239 | 🐛 0 | 🌐 Lua | 📅 2014-05-28 — A simple and lightweight web framework based on OpenResty
* [fasty](https://github.com/solisoft/fasty) ⭐ 180 | 🐛 23 | 🌐 JavaScript | 📅 2026-02-04 - A CMS based on openresty, arangoDB, lapis & riotjs
* [luastar](https://github.com/luastar/luastar) ⭐ 140 | 🐛 0 | 🌐 Lua | 📅 2026-01-27 — A HTTP server and web framework based on OpenResty
* [Quick Server](https://github.com/dualface/quickserver) ⭐ 140 | 🐛 4 | 🌐 Lua | 📅 2015-12-04 — A Server Framework Based on OpenResty
* [Lusty](https://github.com/Olivine-Labs/lusty) ⭐ 107 | 🐛 1 | 🌐 Lua | 📅 2015-10-19 — Lua RESTful Web Application Framework, an extensible and speedy web framework
* [lua-resty-rack](https://github.com/pintsized/lua-resty-rack) ⭐ 82 | 🐛 1 | 🌐 Lua | 📅 2012-08-09 — A simple and extensible HTTP server framework for OpenResty
* [sinatra-openresty](https://github.com/jtarchie/sinatra-openresty) ⚠️ Archived — Sinatra ported to OpenResty framework
* [lj-web](https://github.com/kindy/lj-web) ⭐ 35 | 🐛 0 | 🌐 Lua | 📅 2013-09-23 — Lightweight Web Framework Based On ngx\_openresty
* [Gimlet Cocktail](https://github.com/losinggeneration/gimlet) ⭐ 27 | 🐛 0 | 🌐 MoonScript | 📅 2017-03-23 — A micro web application framework for OpenResty written in Moonscript inspired by Martini & Sinatra
* [vicky](https://github.com/RocksonZeta/vicky) ⭐ 27 | 🐛 0 | 🌐 Lua | 📅 2021-12-10 — A restful framework for openresty,inspired by expressjs and koa.
* [Octopus](https://github.com/cyberz-eu/octopus) ⭐ 25 | 🐛 0 | 🌐 Lua | 📅 2025-06-04 — The Lua Web Platform
* [lua-resty-stack](https://github.com/antonheryanto/lua-resty-stack) ⭐ 12 | 🐛 0 | 🌐 Lua | 📅 2017-10-03 — OpenResty Simple Application Stack
* [zLua](https://github.com/mrxx/zLua) ⭐ 11 | 🐛 0 | 🌐 Lua | 📅 2014-07-02 — A Codeigniter like Lua framework based on OpenResty
* [durap](https://github.com/doujiang24/durap) ⭐ 10 | 🐛 0 | 🌐 HTML | 📅 2015-11-26 — Durap is a Lua Web Framework based on OpenResty.
* [Ziggy Stardust](https://github.com/bakins/stardust) ⭐ 8 | 🐛 0 | 🌐 Lua | 📅 2013-07-09 — Ziggy Stardust (or just "stardust") is a simple nginx/Lua framework inspired by Sinatra, Express, and Mercury
* [dodolu](https://github.com/zhangf911/dodolu) ⭐ 7 | 🐛 0 | 🌐 Lua | 📅 2014-12-12 — A lightweight web framework based on OpenResty
* [Lapis](http://leafo.net/lapis/) — Lapis is a framework for building web applications using MoonScript or Lua that runs inside of a customized version of Nginx called OpenResty

#### Web Development Essentials

* [lua-resty-jwt](https://github.com/SkyLothar/lua-resty-jwt) ⭐ 538 | 🐛 37 | 🌐 Perl | 📅 2024-01-03 — JWT (JSON Web Tokens) for The Great OpenResty
* [lua-resty-cookie](https://github.com/cloudflare/lua-resty-cookie) ⚠️ Archived — Lua library for HTTP cookie manipulations for OpenResty/ngx\_lua
* [lua-resty-session](https://github.com/bungle/lua-resty-session) ⭐ 343 | 🐛 27 | 🌐 Lua | 📅 2025-11-24 — Session library for OpenResty implementing Secure Cookie Protocol
* [Mio](https://github.com/iresty/Mio) ⭐ 284 | 🐛 3 | 🌐 Lua | 📅 2016-12-06 — API statistics/summary and health datas in NGINX based on OpenResty, just like NGINX Plus
* [neturl](https://github.com/golgote/neturl) ⭐ 260 | 🐛 8 | 🌐 Lua | 📅 2024-12-07 — URL and Query string parser, builder, normalizer for Lua
* [lua-resty-woothee](https://github.com/woothee/lua-resty-woothee) ⭐ 65 | 🐛 0 | 🌐 Lua | 📅 2021-10-13 — The Lua-Openresty implementation of Project Woothee, which is a multi-language user-agent strings parsers
* [lua-resty-cors](https://github.com/detailyang/lua-resty-cors) ⭐ 57 | 🐛 2 | 🌐 Lua | 📅 2018-11-05 — The Cross-Origin Resource Sharing (CORS) implementation for OpenResty
* [lua-resty-url](https://github.com/3scale/lua-resty-url) ⭐ 42 | 🐛 3 | 🌐 Lua | 📅 2022-10-03 — URL parser for OpenResty
* [lua-resty-mobile](https://github.com/isage/lua-resty-mobile) ⭐ 34 | 🐛 1 | 🌐 Lua | 📅 2019-07-02 — This library parses HTTP headers and detects mobile device
* [lua-resty-jwt-verification](https://github.com/anvouk/lua-resty-jwt-verification) ⭐ 16 | 🐛 1 | 🌐 Lua | 📅 2026-06-27 — JWT verification library for OpenResty with JWKS integration
* [lua-redis-admin](https://github.com/lifeblood/lua-redis-admin) — redis client tool,redis web client,redis web ui,openresty lor lua framework support

#### Routing Libraries

* [lua-radix-router](https://github.com/vm-001/lua-radix-router) ⭐ 198 | 🐛 4 | 🌐 Lua | 📅 2025-06-10 - A lightweight, high-performance, radix tree based and OpenAPI friendly API Router for Lua / LuaJIT / OpenResty.
* [router.lua](https://github.com/APItools/router.lua) ⚠️ Archived — A barebones router for Lua, it matches URLs and executes Lua functions
* [lua-resty-route](https://github.com/bungle/lua-resty-route) ⭐ 103 | 🐛 3 | 🌐 Lua | 📅 2018-06-26 — A URL routing library for OpenResty supporting multiple route matchers, middleware, and HTTP and WebSockets handlers to mention a few of its features
* [lua-resty-libr3](https://github.com/iresty/lua-resty-libr3) ⭐ 56 | 🐛 8 | 🌐 Perl | 📅 2021-06-21 — High-performance path dispatching library base on [libr3](https://github.com/c9s/r3) ⭐ 821 | 🐛 30 | 🌐 C | 📅 2026-08-18 for OpenResty
* [lua-resty-r3](https://github.com/toritori0318/lua-resty-r3) ⭐ 39 | 🐛 0 | 🌐 Lua | 📅 2015-12-23 — [libr3](https://github.com/c9s/r3) ⭐ 821 | 🐛 30 | 🌐 C | 📅 2026-08-18 OpenResty implementation, libr3 is a high-performance path dispatching library. It compiles your route paths into a prefix tree (trie). By using the constructed prefix trie in the start-up time, you may dispatch your routes with efficiency

#### Traffic Management

* [lua-resty-redis-ratelimit](https://github.com/timebug/lua-resty-redis-ratelimit) ⭐ 169 | 🐛 2 | 🌐 Perl | 📅 2026-06-01 — Limit the request processing rate between multiple NGINX instances backed by Redis
* [lua-resty-limit-rate](https://github.com/upyun/lua-resty-limit-rate) ⭐ 73 | 🐛 0 | 🌐 Perl | 📅 2021-06-11 - Lua module for limiting request rate for OpenResty/ngx\_lua, using the "token bucket" method
* [lua-resty-global-throttle](https://github.com/ElvinEfendi/lua-resty-global-throttle) ⭐ 26 | 🐛 6 | 🌐 Lua | 📅 2024-01-22 — Distributed rate limiter / throttler based on [Cloudflare's blog post on approximate sliding window](https://blog.cloudflare.com/counting-things-a-lot-of-different-things/)

#### Request Argments Parsers

* [lua-resty-reqargs](https://github.com/bungle/lua-resty-reqargs) ⭐ 54 | 🐛 5 | 🌐 Lua | 📅 2017-07-14 — Helper to Retrieve application/x-www-form-urlencoded, multipart/form-data, and application/json Request Arguments
* [lua-resty-multipart-parser](https://github.com/agentzh/lua-resty-multipart-parser) ⭐ 40 | 🐛 2 | 🌐 Lua | 📅 2016-10-23 — Simple multipart data parser for OpenResty / Lua
* [lua-resty-post](https://github.com/antonheryanto/lua-resty-post) ⭐ 35 | 🐛 2 | 🌐 Lua | 📅 2021-06-24 — HTTP Post Utility for OpenResty (File Uploading Helper)
* [lua-resty-multipart](https://github.com/thibaultcha/lua-resty-multipart) ⭐ 6 | 🐛 1 | 🌐 Lua | 📅 2016-10-25 — Multipart parsing library for OpenResty

#### Middleware and API Tools

* [Kong](https://getkong.org/) ([GitHub](https://github.com/Kong/kong) ⭐ 44,003 | 🐛 189 | 🌐 Lua | 📅 2026-08-16) — KONG: Microservice Management Layer (Secure, Manage & Extend your APIs and Microservices)
* [APISIX](https://github.com/iresty/apisix) ⭐ 17,005 | 🐛 243 | 🌐 Lua | 📅 2026-08-19 — APISIX is a Cloud-Native Microservices API Gateway
* [Sumory Orange](https://github.com/sumory/orange) ⭐ 2,308 | 🐛 77 | 🌐 Lua | 📅 2023-08-25 — API Gateway
* [Slardar](https://github.com/upyun/slardar) ⚠️ Archived - Updating your upstream list and run lua scripts without reloading Nginx
* [3scale APIcast](https://github.com/3scale/apicast) ⭐ 323 | 🐛 61 | 🌐 Lua | 📅 2026-07-20 — API gateway module of Red Hat 3scale API Management
* [apigateway](https://github.com/adobe-apiplatform/apigateway) ⭐ 300 | 🐛 11 | 🌐 Lua | 📅 2026-03-04 — A Performant API Gateway based on Nginx and OpenResty
* [tl-ops-manage](https://github.com/iamtsm/tl-ops-manage) ⭐ 253 | 🐛 2 | 🌐 Lua | 📅 2023-07-31 - Framework for service management based on openresty
* [lua-resty-grpc-gateway](https://github.com/ysugimoto/lua-resty-grpc-gateway) ⭐ 86 | 🐛 18 | 🌐 Lua | 📅 2023-10-25 — Provides request transformation between REST <-> gRPC with Openresty
* [LSSO](https://github.com/maiome-development/lsso) ⭐ 47 | 🐛 6 | 🌐 Lua | 📅 2017-01-02 — A Lightweight SSO middleware for Nginx + Lua
* [Monarch API Gateway](https://github.com/monarchapis/gateway-openresty) ⭐ 8 | 🐛 0 | 🌐 Lua | 📅 2016-02-11  — OpenResty-based API Gateway

#### Templating

* [lua-resty-template](https://github.com/bungle/lua-resty-template) ⭐ 923 | 🐛 15 | 🌐 Lua | 📅 2023-07-21 — A Compiling (HTML) templating engine for Lua and OpenResty
* [Alternatives](https://github.com/bungle/lua-resty-template#alternatives) ⭐ 923 | 🐛 15 | 🌐 Lua | 📅 2023-07-21 — Some alternative Lua templating solutions that may work just fine with OpenResty
* [etlua](https://github.com/leafo/etlua) ⭐ 258 | 🐛 5 | 🌐 Lua | 📅 2023-10-02 — Embedded Lua templates
* [lemplate](https://github.com/openresty/lemplate) ⭐ 54 | 🐛 2 | 🌐 Perl | 📅 2019-11-05 — OpenResty/Lua template framework implementing Perl's TT2 templating language
* [lua-resty-aries](https://github.com/DoubleSpout/lua-resty-aries) ⭐ 46 | 🐛 0 | 🌐 Lua | 📅 2017-04-12 — OpenResty and Lua multi-function template, it can correct show your error line
* [liquid-lua](https://github.com/chenxianyu2015/liquid-lua) ⭐ 15 | 🐛 5 | 🌐 Lua | 📅 2022-06-18 — A Lua implementation of Liquid for OpenResty platform
* [lua-resty-tmpl](https://github.com/lloydzhou/lua-resty-tmpl) ⭐ 6 | 🐛 0 | 🌐 Lua | 📅 2016-01-08 — A simple template engine for Lua and OpenResty, derived from [lua-template](https://github.com/dannote/lua-template) ⭐ 66 | 🐛 1 | 🌐 Lua | 📅 2025-05-10.

#### Validation

* [lua-resty-validation](https://github.com/bungle/lua-resty-validation) ⭐ 155 | 🐛 2 | 🌐 Lua | 📅 2021-08-31 — An extendable chaining validation and filtering library for Lua and OpenResty
* [valua](https://github.com/sailorproject/valua) ⭐ 81 | 🐛 3 | 🌐 Lua | 📅 2022-10-24 — Validation for lua! A module for making chained validations. Create your objects, append your tests, use and reuse it!

#### Authentication and Authorization

* [lua-resty-openidc](https://github.com/pingidentity/lua-resty-openidc) ⭐ 1,073 | 🐛 71 | 🌐 Lua | 📅 2026-07-01 — lua-resty-openidc is a library for NGINX implementing the OpenID Connect Relying Party (RP) and the OAuth 2.0 Resource Server (RS) functionality
* [micro-auth](https://github.com/hypebeast/micro-auth) ⭐ 473 | 🐛 0 | 🌐 Lua | 📅 2017-03-23 — A microservice that makes adding authentication with Google and Github to your application easy (Note: before using it in production, see: <https://news.ycombinator.com/item?id=13682682> — hopefully we can remove this remark in a future)
* [lua-resty-macaroons](https://github.com/bungle/lua-resty-macaroons) ⭐ 10 | 🐛 2 | 🌐 Lua | 📅 2016-07-06 — LuaJIT FFI Bindings to libmacaroons – Macaroons are flexible authorization credentials that support decentralized delegation, attenuation, and verification
* [lua-resty-casbin](https://github.com/casbin-lua/lua-resty-casbin) ⭐ 6 | 🐛 1 | 🌐 Lua | 📅 2023-07-06 — Casbin is an authorization library that supports access control models like ACL, RBAC, ABAC in Lua (OpenResty). This is a Casbin authorization plugin for OpenResty.
* [lua-resty-duo-mobile](https://github.com/p0pr0ck5/lua-resty-duo-mobile) ⭐ 2 | 🐛 0 | 🌐 Lua | 📅 2018-06-22 — OpenResty client for the Duo Mobile Auth API

#### Cryptography

* [lua-resty-auto-ssl](https://github.com/GUI/lua-resty-auto-ssl) ⭐ 1,987 | 🐛 124 | 🌐 Lua | 📅 2026-01-21 — On the fly (and free) SSL registration and renewal inside OpenResty/nginx with Let's Encrypt
* [lua-resty-string](https://github.com/openresty/lua-resty-string) ⭐ 443 | 🐛 26 | 🌐 Lua | 📅 2026-07-17 — String utilities and common hash functions for ngx\_lua and LuaJIT
* [lua-resty-chash](https://github.com/agentzh/lua-resty-chash) ⭐ 337 | 🐛 15 | 🌐 Lua | 📅 2026-05-07 — A generic consistent hash implementation for OpenResty/Lua
* [lua-resty-rsa](https://github.com/spacewander/lua-resty-rsa) ⭐ 268 | 🐛 11 | 🌐 Lua | 📅 2024-11-09 — RSA functions for LuaJIT
* [lua-resty-acme](https://github.com/fffonion/lua-resty-acme) ⭐ 202 | 🐛 8 | 🌐 Lua | 📅 2025-09-01 — Automatic Let's Encrypt certificate serving and Lua implementation of ACMEv2 procotol
* [lua-resty-nettle](https://github.com/bungle/lua-resty-nettle) ⭐ 186 | 🐛 5 | 🌐 Lua | 📅 2023-06-08 — LuaJIT FFI bindings for Nettle (a low-level cryptographic library)
* [lua-resty-openssl](https://github.com/fffonion/lua-resty-openssl) ⭐ 170 | 🐛 7 | 🌐 Lua | 📅 2026-08-14 — FFI-based OpenSSL binding for LuaJIT
* [lua-resty-letsencrypt](https://github.com/torhve/lua-resty-letsencrypt) ⭐ 67 | 🐛 4 | 🌐 Lua | 📅 2017-06-14 — Automatically fetch and renew TLS certificates on the fly using LetsEncrypt CA.
* [lua-resty-hmac](https://github.com/jamesmarlowe/lua-resty-hmac) ⭐ 42 | 🐛 4 | 🌐 Lua | 📅 2022-05-09 — Lua driver for making and receiving hmac signed requests
* [lua-resty-murmurhash2](https://github.com/bungle/lua-resty-murmurhash2) ⭐ 30 | 🐛 0 | 🌐 Lua | 📅 2015-12-16 — LuaJIT MurmurHash 2 bindings to Nginx / OpenResty murmurhash2 implementation
* [lua-resty-jump-consistent-hash](https://github.com/ruoshan/lua-resty-jump-consistent-hash) ⭐ 28 | 🐛 0 | 🌐 Perl | 📅 2019-01-15 — Jump Consistent Hash for LuaJIT
* [lua-argon2-ffi](https://github.com/thibaultCha/lua-argon2-ffi) ⭐ 22 | 🐛 0 | 🌐 Lua | 📅 2019-07-11 — LuaJIT FFI binding for the Argon2 password hashing algorithm
* [lua-resty-scrypt](https://github.com/bungle/lua-resty-scrypt) ⭐ 18 | 🐛 0 | 🌐 Lua | 📅 2017-07-06 — LuaJIT FFI-based scrypt library for OpenResty
* [lua-resty-xxhash](https://github.com/bungle/lua-resty-xxhash) ⭐ 18 | 🐛 1 | 🌐 Lua | 📅 2015-12-03 — LuaJIT FFI-bindings to xxHash, an Extremely fast non-cryptographic hash algorithm
* [WXBizMsgCrypt](https://github.com/TheNorthMemory/WXBizMsgCrypt) ⭐ 13 | 🐛 0 | 🌐 Lua | 📅 2018-11-27 — Lua version of the WeChat Message Cryptography
* [lua-resty-peter\_sslers](https://github.com/aptise/lua-resty-peter_sslers) ⭐ 9 | 🐛 1 | 🌐 Perl | 📅 2025-07-14 — Automaticly loads/cache SSL certificates based on SNI from caches or backend json servers
* [lua-resty-urandom](https://github.com/p0pr0ck5/lua-resty-urandom) ⭐ 9 | 🐛 1 | 🌐 Perl | 📅 2017-05-21 — Buffered wrapper for Linux/BSD kernel space CSPRNG
* [lua-resty-hawk](https://github.com/golgote/lua-resty-hawk) ⭐ 4 | 🐛 0 | 🌐 Lua | 📅 2015-10-28 — Hawk authentication on Nginx with Lua and OpenResty
* [lua-resty-des](https://github.com/lilien1010/lua-resty-des) ⭐ 4 | 🐛 2 | 🌐 Lua | 📅 2017-12-22 — Lua interface to make DES ECB encryption
* [lua-resty-aead](https://github.com/tmthrgd/lua-resty-aead) ⚠️ Archived — AEAD cipher library for lua-nginx-module. BoringSSL only.
* [lua-resty-fastpbkdf2](https://github.com/mynameiscfed/lua-resty-fastpbkdf2) ⭐ 0 | 🐛 0 | 🌐 C | 📅 2016-04-04 — Lua bindings to fastpbkdf2
* [luasodium](https://github.com/jprjr/luasodium) - Lua bindings to libsodium, compatible with both Lua C and LuaJIT FFI APIs.

#### Networking

* [lua-resty-http](https://github.com/pintsized/lua-resty-http) ⭐ 2,079 | 🐛 42 | 🌐 Lua | 📅 2026-08-11 by [@pintsized](https://github.com/pintsized) — Lua HTTP client cosocket driver for OpenResty / ngx\_lua
* [lua-resty-waf](https://github.com/p0pr0ck5/lua-resty-waf) ⭐ 1,324 | 🐛 38 | 🌐 Perl | 📅 2024-01-31 — High-performance WAF built on the OpenResty stack
* [lua-resty-limit-traffic](https://github.com/openresty/lua-resty-limit-traffic) ⭐ 852 | 🐛 38 | 🌐 Lua | 📅 2026-07-17 — Lua library for limiting and controlling traffic in OpenResty/ngx\_lua
* [lua-resty-websocket](https://github.com/openresty/lua-resty-websocket) ⭐ 523 | 🐛 32 | 🌐 Lua | 📅 2026-08-17 — Lua WebSocket implementation for the ngx\_lua module
* [lua-resty-balancer](https://github.com/openresty/lua-resty-balancer) ⭐ 337 | 🐛 15 | 🌐 Lua | 📅 2026-05-07 — A generic consistent hash implementation for OpenResty
* [lua-resty-checkups](https://github.com/upyun/lua-resty-checkups) ⭐ 261 | 🐛 10 | 🌐 Lua | 📅 2019-11-26 — Manage Nginx upstreams in pure ngx\_lua
* [lua-resty-iputils](https://github.com/hamishforbes/lua-resty-iputils) ⭐ 253 | 🐛 7 | 🌐 Perl | 📅 2022-05-03 — Utility functions for working with IP addresses in OpenResty
* [lua-resty-http](https://github.com/liseen/lua-resty-http) ⭐ 188 | 🐛 12 | 🌐 Lua | 📅 2017-06-23 by [@liseen](https://github.com/liseen) — Lua http client driver for the ngx\_lua based on the cosocket API
* [lua-resty-requests](https://github.com/tokers/lua-resty-requests) ⭐ 170 | 🐛 11 | 🌐 Lua | 📅 2020-05-06 — Yet Another HTTP Library for OpenResty
* [lua-resty-dns-client](https://github.com/Kong/lua-resty-dns-client) ⚠️ Archived — Lua library containing a DNS client, several utilities, and a load-balancer
* [lua-capnproto](https://github.com/cloudflare/lua-capnproto) ⭐ 154 | 🐛 2 | 🌐 Lua | 📅 2026-04-24 — Cap’n Proto is an insanely fast data interchange format and capability-based RPC system
* [lua-resty-healthcheck](https://github.com/Kong/lua-resty-healthcheck) ⭐ 146 | 🐛 10 | 🌐 Lua | 📅 2026-08-13 — Healthcheck library for OpenResty to validate upstream service status
* [lua-resty-ipmatcher](https://github.com/api7/lua-resty-ipmatcher) ⭐ 136 | 🐛 7 | 🌐 Lua | 📅 2023-06-19 — High performance match IP address for OpenResty Lua
* [lua-resty-consul](https://github.com/hamishforbes/lua-resty-consul) ⭐ 130 | 🐛 1 | 🌐 Perl | 📅 2021-08-18 — Library to interface with the consul HTTP API from ngx\_lua
* [lua-resty-upstream](https://github.com/hamishforbes/lua-resty-upstream) ⭐ 116 | 🐛 3 | 🌐 Perl | 📅 2019-12-19 — Upstream connection load balancing and failover module
* [lua-resty-sniproxy](https://github.com/fffonion/lua-resty-sniproxy) ⭐ 86 | 🐛 2 | 🌐 Lua | 📅 2020-08-31 — SNI Proxy based on stream-lua-nginx-module
* [lua-resty-upstream-etcd](https://github.com/rrfeng/lua-resty-upstream-etcd) ⭐ 82 | 🐛 0 | 🌐 Lua | 📅 2020-04-27 — A Lua module for OpenResty, can dynamically update the upstreams from etcd and Kubernetes
* [lua-resty-http-simple](https://github.com/bakins/lua-resty-http-simple) ⭐ 80 | 🐛 2 | 🌐 Lua | 📅 2014-11-05 — Simple Lua HTTP client driver for ngx\_lua
* [lua-resty-http2](https://github.com/tokers/lua-resty-http2) ⭐ 79 | 🐛 3 | 🌐 Lua | 📅 2020-02-04 — The HTTP/2 Protocol (Client Side) Implementation for OpenResty
* [lua-resty-dns-server](https://github.com/vislee/lua-resty-dns-server) ⭐ 75 | 🐛 3 | 🌐 Lua | 📅 2023-03-14 — Lua DNS server driver for the OpenResty
* [lua-resty-httpipe](https://github.com/timebug/lua-resty-httpipe) ⭐ 71 | 🐛 1 | 🌐 Perl | 📅 2020-07-22 — Lua HTTP client cosocket driver for OpenResty / ngx\_lua
* [lua-resty-multiplexer](https://github.com/fffonion/lua-resty-multiplexer) ⭐ 62 | 🐛 1 | 🌐 Lua | 📅 2020-09-10 — Transparent port service multiplexer for stream subsystem
* [lua-resty-socks5](https://github.com/starius/lua-resty-socks5) ⭐ 34 | 🐛 7 | 🌐 Lua | 📅 2016-06-03 — Lua SOCKS5 client for the ngx\_lua based on the cosocket API
* [lua-resty-tarpit](https://github.com/p0pr0ck5/lua-resty-tarpit) ⭐ 28 | 🐛 1 | 🌐 Lua | 📅 2022-10-11 — OpenResty response time inflation, capture and delay unwanted requests
* [lua-resty-jsonrpc-batch](https://github.com/mosasiru/lua-resty-jsonrpc-batch) ⭐ 24 | 🐛 1 | 🌐 Perl | 📅 2015-07-15 — JSON-RPC 2.0 Batch Request protocol module for OpenResty
* [lua-resty-fastcgi](https://github.com/benagricola/lua-resty-fastcgi) ⭐ 23 | 🐛 2 | 🌐 Lua | 📅 2017-09-28 — Lua FCGI client driver for ngx\_lua based on the cosocket API
* [lua-resty-ftpclient](https://github.com/Ahsialh/lua-resty-ftpclient) ⭐ 15 | 🐛 0 | 🌐 Lua | 📅 2023-02-26 — Lua FTP client driver for the ngx\_lua based on the cosocket API
* [lua-resty-httpclient](https://github.com/oneoo/lua-resty-httpclient) ⭐ 14 | 🐛 0 | 🌐 Lua | 📅 2014-08-22 — Nonblocking Lua HTTP Client library for aLiLua & ngx\_lua
* [lua-resty-mediador](https://github.com/Kong/lua-resty-mediador) ⭐ 11 | 🐛 0 | 🌐 Lua | 📅 2021-09-30 — Determines address of proxied request and does IP address / CIDR blocks handling (both IPv4 and IPv6)
* [lua-tus-server](https://github.com/mmatuska/lua-tus-server) ⭐ 11 | 🐛 0 | 🌐 Perl | 📅 2020-03-20 - Server-side implementation of the tus protocol in Lua
* [lua-resty-tornera](https://github.com/pinge/lua-resty-tornera) ⭐ 10 | 🐛 0 | 🌐 Lua | 📅 2016-04-09 — A traffic replay tool with an easy to use HTTP API for OpenResty / LuaJIT
* [lua-resty-limits](https://github.com/membphis/lua-resty-limits) ⭐ 8 | 🐛 0 | 🌐 Lua | 📅 2015-06-30 — Limits request every second or minute
* [lua-resty-readurl](https://github.com/jamesmarlowe/lua-resty-readurl) ⭐ 5 | 🐛 1 | 🌐 Perl | 📅 2014-10-22 — Lua library for capturing urls, decoding, and logging results
* [lua-resty-wrr](https://github.com/vislee/lua-resty-wrr) ⭐ 3 | 🐛 0 | 🌐 Perl | 📅 2021-11-29 - weight round robin for Openresty. Similar to ngx\_http/stream\_upstream\_round\_robin module.
* [lua-httpcli-resty](https://github.com/mah0x211/lua-httpcli-resty) ⭐ 1 | 🐛 0 | 🌐 Lua | 📅 2015-09-16 — Lua HTTP client module for OpenResty
* [lua-resty-dycert](https://github.com/vislee/lua-resty-dycert) ⭐ 1 | 🐛 0 | 🌐 Perl | 📅 2023-11-23 - Dynamically generate a certificate based on a CSR and sign it with a CA.
* [lua-resty-http](https://github.com/DorianGray/lua-resty-http) ⭐ 0 | 🐛 0 | 🌐 Perl | 📅 2015-07-22 by [@DorianGray](https://github.com/DorianGray) — Lua HTTP client driver for ngx\_lua based on the cosocket API

#### Databases and Storages

* [lua-resty-redis](https://github.com/openresty/lua-resty-redis) ⭐ 1,956 | 🐛 75 | 🌐 Lua | 📅 2026-07-17 — Lua Redis client driver for the ngx\_lua based on the cosocket API
* [lua-resty-mysql](https://github.com/openresty/lua-resty-mysql) ⭐ 726 | 🐛 54 | 🌐 Lua | 📅 2026-06-20 — Non-blocking Lua MySQL client driver for ngx\_lua based on the cosocket API
* [pgmoon](https://github.com/leafo/pgmoon) ⭐ 432 | 🐛 22 | 🌐 MoonScript | 📅 2026-08-11 — A pure Lua Postgres driver for use in OpenResy & more
* [resty-redis-cluster](https://github.com/steve0511/resty-redis-cluster) ⭐ 386 | 🐛 32 | 🌐 Perl | 📅 2023-08-04 — OpenResty Redis cluster-aware client based on resty-redis-cluster
* [lua-resty-redis-connector](https://github.com/pintsized/lua-resty-redis-connector) ⭐ 245 | 🐛 9 | 🌐 Lua | 📅 2026-01-23 — Connection utilities for lua-resty-redis, making it easy and reliable to connect to Redis hosts, either directly or via Redis Sentinel
* [lua-resty-memcached](https://github.com/openresty/lua-resty-memcached) ⭐ 216 | 🐛 8 | 🌐 Lua | 📅 2026-07-17 — Lua memcached client driver for the ngx\_lua based on the cosocket API
* [lua-resty-etcd](https://github.com/api7/lua-resty-etcd) ⭐ 203 | 🐛 22 | 🌐 Lua | 📅 2026-08-17 — Nonblocking Lua etcd driver library for OpenResty
* [lua-resty-redis-util](https://github.com/anjia0532/lua-resty-redis-util) ⭐ 125 | 🐛 2 | 🌐 Lua | 📅 2022-09-06 — Based on `lua-resty-redis` and makes it easier to operate the Redis
* [lua-resty-moongoo](https://github.com/isage/lua-resty-moongoo) ⭐ 120 | 🐛 8 | 🌐 Lua | 📅 2020-09-15 — MongoDB library for OpenResty, highly inspired by Perl Mango
* [lua-cassandra](https://github.com/thibaultCha/lua-cassandra) ⭐ 102 | 🐛 12 | 🌐 Lua | 📅 2022-09-20 - Pure Lua, feature-rich, and cluster-aware Cassandra client
* [lua-resty-redis-cluster](https://github.com/cuiweixie/lua-resty-redis-cluster) ⭐ 101 | 🐛 15 | 🌐 Perl | 📅 2020-06-17 — OpenResty Redis Cluster Client
* [lua-resty-ssdb](https://github.com/LazyZhu/lua-resty-ssdb) ⭐ 101 | 🐛 6 | 🌐 Lua | 📅 2019-07-11 — Lua ssdb client driver for the ngx\_lua based on the cosocket API, SSDB is a leveldb server
* [lua-resty-smtp](https://github.com/duhoobo/lua-resty-smtp) ⭐ 86 | 🐛 12 | 🌐 Lua | 📅 2021-02-28 — A bridge between HTTP and SMTP
* [lua-resty-fastdfs](https://github.com/azurewang/lua-resty-fastdfs) ⭐ 82 | 🐛 5 | 🌐 Lua | 📅 2015-04-20 — Nonblocking Lua FastDFS driver library for ngx\_lua
* [iqiyi/lua-resty-couchbase](https://github.com/iqiyi/lua-resty-couchbase) ⭐ 79 | 🐛 1 | 🌐 Lua | 📅 2020-08-28 — Lua couchbase client driver for the ngx\_lua based on the cosocket API
* [lua-resty-mail](https://github.com/GUI/lua-resty-mail) ⭐ 72 | 🐛 2 | 🌐 Lua | 📅 2026-02-04 — A high-level, easy to use, and non-blocking email and SMTP library for OpenResty
* [lua-resty-cassandra](https://github.com/jbochi/lua-resty-cassandra) ⭐ 68 | 🐛 5 | 🌐 Lua | 📅 2017-06-09 — Pure Lua Cassandra client using CQL binary protocol
* [lua-resty-postgres](https://github.com/azurewang/lua-resty-postgres) ⭐ 65 | 🐛 6 | 🌐 Lua | 📅 2022-04-18 — Nonblocking Lua PostgreSQL driver library for ngx\_lua
* [lua-resty-tarantool](https://github.com/perusio/lua-resty-tarantool) ⭐ 46 | 🐛 4 | 🌐 Lua | 📅 2025-02-27 — Library for working with Tarantool from Nginx with the embedded Lua module or with OpeRresty
* [lua-resty-mongol](https://github.com/Olivine-Labs/resty-mongol/) ⭐ 45 | 🐛 11 | 🌐 Perl | 📅 2020-04-29 — Native Lua Mongodb driver which supports both luasocket and ngx\_lua based on the cosocket API
* [lua-resty-orm](https://github.com/kran/lua-resty-orm) ⭐ 31 | 🐛 0 | 🌐 Lua | 📅 2026-04-01 — Simple ORM for OpenResty
* [lua-resty-influx](https://github.com/p0pr0ck5/lua-resty-influx) ⭐ 28 | 🐛 3 | 🌐 Perl | 📅 2020-12-16 — OpenResty client for InfluxDB
* [lua-resty-riak](https://github.com/bakins/lua-resty-riak) ⭐ 26 | 🐛 3 | 🌐 Lua | 📅 2014-09-10 — Lua riak protocol buffer client driver for the ngx\_lua based on the cosocket API
* [lua-resty-mongo](https://github.com/nightsailer/lua-resty-mongo) ⭐ 22 | 🐛 2 | 🌐 Lua | 📅 2012-03-11 — Lua mongodb client driver for the ngx\_lua based on the cosocket API
* [lua-nginx-tarantool](https://github.com/ziontab/lua-nginx-tarantool) ⭐ 18 | 🐛 3 | 🌐 Lua | 📅 2017-08-17 — A driver for a NoSQL database in a Lua script Tarantool build on fast nginx cosockets
* [lua-shdict-nginx-module](https://github.com/rainingmaster/lua-shdict-nginx-module) ⭐ 18 | 🐛 0 | 🌐 Perl | 📅 2018-05-25 — An upgraded version of [ngx.shared.DICT](https://github.com/openresty/lua-nginx-module#ngxshareddict) ⭐ 11,787 | 🐛 392 | 🌐 C | 📅 2026-08-14, capable of sharing data between `stream` and `http` modules
* [lua-resty-mvc](https://github.com/pronan/lua-resty-mvc) ⭐ 17 | 🐛 0 | 🌐 Lua | 📅 2017-02-13 — You don't need that complicated MVC framework! With just a plain folder with several simple files, you can enjoy basic but most frequently used MVC features.
* [lua-resty-kyototycoon](https://github.com/cloudflare/lua-resty-kyototycoon) ⭐ 17 | 🐛 0 | 🌐 Perl | 📅 2013-12-06 by [@cloudflare](https://github.com/cloudflare/) — Lua client driver for KyotoTycoon using its native wire protocol (OpenResty/ngx\_lua)
* [lua-resty-bloomd](https://github.com/jie123108/lua-resty-bloomd) ⭐ 15 | 🐛 1 | 🌐 Lua | 📅 2015-12-30 — A client library based on ngx\_lua to interface with [bloomd servers](https://github.com/armon/bloomd) ⭐ 1,248 | 🐛 3 | 🌐 C | 📅 2023-02-14
* [lua-resty-couchdb](https://github.com/paragasu/lua-resty-couchdb) ⭐ 12 | 🐛 0 | 🌐 Lua | 📅 2020-08-23 — Lua resty minimal couchdb client using nginx proxy ngx.location\_capture
* [lua-resty-kyototycoon](https://github.com/sjnam/lua-resty-kyototycoon) ⚠️ Archived by [@sjnam](https://github.com/sjnam/) — Lua client driver for KyotoTycoon using its binary protocol
* [lua-resty-couchbase](https://github.com/ZigzagAK/lua-resty-couchbase) ⭐ 7 | 🐛 0 | 🌐 Lua | 📅 2020-07-22 — OpenResty CouchBase module
* [lua-mongo](https://github.com/boyxuper/lua-mongo) ⭐ 6 | 🐛 0 | 🌐 C | 📅 2015-03-18 — A simple Lua Mongo driver (a fork made to work with co-sockets)
* [ledis-openresty](https://github.com/holys/ledis-openresty) ⭐ 5 | 🐛 0 | 🌐 Lua | 📅 2016-06-25 — Lua LedisDB client driver for the ngx\_lua based on the cosocket API
* [lua-telegraf](https://github.com/lblasc/lua-telegraf) ⭐ 4 | 🐛 0 | 🌐 Lua | 📅 2020-12-19 — Lua/OpenResty client for Telegraf/InfluxDB
* [lua-resty-mysql-connector](https://github.com/myselfghost/lua-resty-mysql-connector) ⭐ 1 | 🐛 0 | 🌐 Lua | 📅 2018-04-18 —
  Connection utilities for lua-resty-mysql, support for read and write separation，support for instantiating different databases
* [lua-resty-mogilefs](https://github.com/sunkan/lua-resty-mogilefs) ⭐ 0 | 🐛 0 | 🌐 Lua | 📅 2017-02-08 — A Lua mogilefs client driver for the ngx\_lua based on the cosocket API
* [lua-resty-statsd](https://github.com/mediba-system/lua-resty-statsd) — StatsD client for OpenResty
* [lua-resty-dogstatsd](https://github.com/mediba-system/lua-resty-dogstatsd) — A client for DogStatsD, an extension of the StatsD metric server for Datadog. Using nginx cosocket API
* [openresty-statsd](https://github.com/lonelyplanet/openresty-statsd) — A Lua module for OpenResty to send metrics to StatsD

#### Testing and Profiling

* [FlameGraph](https://github.com/brendangregg/FlameGraph) ⭐ 19,681 | 🐛 174 | 🌐 Perl | 📅 2024-10-20 — Flame graphs are a visualization of profiled software, allowing the most frequent code-paths to be identified quickly and accurately
* [Test::Nginx](http://search.cpan.org/~agent/Test-Nginx-0.24/lib/Test/Nginx.pm) — Data-driven test scaffold for Nginx C module and OpenResty Lua library development (see real-word tests in [lua-resty-redis](https://github.com/openresty/lua-resty-redis/tree/master/t) ⭐ 1,956 | 🐛 75 | 🌐 Lua | 📅 2026-07-17)
* [nginx-systemtap-toolkit](https://github.com/openresty/nginx-systemtap-toolkit) ⭐ 1,669 | 🐛 28 | 🌐 Perl | 📅 2023-03-14 — Real-time analyzing and diagnosing tools for Nginx based on SystemTap
* [busted](http://olivinelabs.com/busted/) ([Github](https://github.com/Olivine-Labs/busted) ⭐ 1,628 | 🐛 66 | 🌐 Lua | 📅 2026-07-30) — Elegant Lua unit testing
* [stapxx](https://github.com/openresty/stapxx) ⭐ 711 | 🐛 21 | 🌐 Perl | 📅 2022-05-09 — Simple macro language extentions to systemtap
* [Telescope](http://telescope.luaforge.net/) ([Github](https://github.com/norman/telescope) ⭐ 164 | 🐛 8 | 🌐 Lua | 📅 2017-08-05) — Telescope is a highly customizable test library for Lua that allows for declarative tests with nested contexts
* [lua-resty-test](https://github.com/membphis/lua-resty-test) ⭐ 136 | 🐛 2 | 🌐 Lua | 📅 2019-09-25 — Test frame based on OpenResty
* [lua-resty-busted](https://github.com/thibaultCha/lua-resty-busted) ⭐ 36 | 🐛 0 | 🌐 Lua | 📅 2023-12-22 — Test OpenResty scripts with busted

#### Message Queuing and Task Management

* [lua-resty-kafka](https://github.com/doujiang24/lua-resty-kafka) ⭐ 814 | 🐛 83 | 🌐 Lua | 📅 2023-11-03 — Lua kafka client driver for the ngx\_lua based on the cosocket API
* [lua-resty-rabbitmqstomp](https://github.com/wingify/lua-resty-rabbitmqstomp) ⭐ 194 | 🐛 3 | 🌐 Lua | 📅 2020-04-27 — Lua RabbitMQ client library which uses cosocket api for communication over STOMP 1.2 with a RabbitMQ broker which has the STOMP plugin
* [lua-resty-qless](https://github.com/pintsized/lua-resty-qless) ⭐ 97 | 🐛 3 | 🌐 Lua | 📅 2022-07-08 — Lua binding to Qless (Queue / Pipeline management) for OpenResty (see also: [Qless Web Interface](https://github.com/hamishforbes/lua-resty-qless-web) ⭐ 13 | 🐛 0 | 🌐 JavaScript | 📅 2017-04-19 implemented with OpenResty)
* [lua-resty-gearman](https://github.com/zhhchen/lua-resty-gearman) ⭐ 26 | 🐛 2 | 🌐 Lua | 📅 2013-11-20 — Lua gearman client driver for the ngx\_lua based on the cosocket API
* [lua-resty-nsq](https://github.com/rainingmaster/lua-resty-nsq) ⭐ 21 | 🐛 2 | 🌐 Lua | 📅 2020-06-09 — [NSQ](https://nsq.io/) client for for the ngx\_lua based on the cosocket API
* [lua-resty-beanstalkd](https://github.com/bakins/lua-resty-beanstalkd) ⭐ 16 | 🐛 0 | 🌐 Lua | 📅 2012-08-17 — Lua beanstalkd client driver for the ngx\_lua based on the cosocket API
* [lua-resty-ironmq](https://github.com/bakins/lua-resty-ironmq) ⭐ 0 | 🐛 0 | 🌐 Lua | 📅 2013-12-13 — Simple IronMQ client for OpenResty

#### Bar Codes and QR Codes

* [lua-resty-QRcode](https://github.com/dcshi/lua-resty-QRcode) ⭐ 31 | 🐛 0 | 🌐 C | 📅 2013-08-19 — QR encode tool for ngx\_lua
* [lua-resty-QRDecode](https://github.com/dcshi/lua-resty-QRDecode) ⭐ 12 | 🐛 1 | 📅 2013-02-02 — QR decoder for ngx\_lua

#### Utilities

* [Inspect](https://github.com/kikito/inspect.lua) ⭐ 1,537 | 🐛 3 | 🌐 Lua | 📅 2026-01-05 — Inspect is a library that transforms any Lua value into a human-readable representation. It is especially useful for debugging errors in tables.
* [lua-resty-radixtree](https://github.com/api7/lua-resty-radixtree) ⭐ 282 | 🐛 21 | 🌐 C | 📅 2024-11-28 — Lua / OpenResty implementation based on FFI for [rax](https://github.com/antirez/rax) ⭐ 1,265 | 🐛 25 | 🌐 C | 📅 2023-11-26
* [lua-resty-jit-uuid](https://github.com/thibaultCha/lua-resty-jit-uuid) ⭐ 209 | 🐛 0 | 🌐 Perl | 📅 2020-01-10 — A pure LuaJIT (no dependencies) uuid generator tuned for performance
* [lua-resty-worker-events](https://github.com/Kong/lua-resty-worker-events) ⭐ 204 | 🐛 3 | 🌐 Lua | 📅 2022-06-02 — Inter process events for Nginx worker processes
* [lua-resty-repl](https://github.com/saks/lua-resty-repl) ⭐ 184 | 🐛 6 | 🌐 Lua | 📅 2017-07-28 — Interactive console (REPL) for OpenResty and LuaJIT code
* [lua-resty-shell](https://github.com/juce/lua-resty-shell) ⭐ 148 | 🐛 3 | 🌐 Lua | 📅 2022-09-28 — Tiny non-blocking subprocess / shell library to use with OpenResty application server (using [sockproc](https://github.com/juce/sockproc) ⭐ 96 | 🐛 3 | 🌐 C | 📅 2019-06-02)
* [lua-resty-maxminddb](https://github.com/anjia0532/lua-resty-maxminddb) ⭐ 122 | 🐛 0 | 🌐 Lua | 📅 2025-12-08 by [@anjia0532](https://github.com/anjia0532) — A Lua library for reading MaxMind's Geolocation database format (aka mmdb or geoip2)
* [lua-resty-uuid](https://github.com/bungle/lua-resty-uuid) ⭐ 60 | 🐛 1 | 🌐 Lua | 📅 2026-05-07 — LuaJIT FFI bindings for libuuid, a DCE compatible Universally Unique Identifier library
* [lua-resty-sync](https://github.com/upyun/lua-resty-sync) ⭐ 42 | 🐛 1 | 🌐 Lua | 📅 2018-01-03 - This lua-resty library help you to synchronize data(from redis, mysql, memcached and so on) based on the version changes
* [lua-resty-libinjection](https://github.com/p0pr0ck5/lua-resty-libinjection) ⭐ 38 | 🐛 0 | 🌐 Lua | 📅 2018-06-22 — LuaJIT FFI bindings for libinjection, a SQL/SQLi tokenizer and analyzer
* [lua-resty-socket](https://github.com/thibaultcha/lua-resty-socket) ⭐ 38 | 🐛 4 | 🌐 Perl | 📅 2023-02-08 — Automatic LuaSocket/cosockets compatibility module
* [lua-resty-counter](https://github.com/Kong/lua-resty-counter) ⭐ 23 | 🐛 4 | 🌐 Perl | 📅 2023-05-13 — Lock-free counter for OpenResty
* [lua-resty-base-encoding](https://github.com/spacewander/lua-resty-base-encoding) ⭐ 18 | 🐛 0 | 🌐 C | 📅 2021-08-05 — Provides base32/base16/... encoding for OpenResty applications.
* [lua-resty-wirefilter](https://github.com/satrobit/lua-resty-wirefilter) ⭐ 15 | 🐛 1 | 🌐 Lua | 📅 2021-01-30 — LuaJIT FFI bindings to wirefilter - An execution engine for Wireshark-like filters
* [lua-resty-mime-sniff](https://github.com/spacewander/lua-resty-mime-sniff) ⭐ 13 | 🐛 0 | 🌐 Lua | 📅 2018-04-05 — Sniff the real MIME type of given data
* [lua-resty-fileinfo](https://github.com/bungle/lua-resty-fileinfo) ⭐ 12 | 🐛 0 | 🌐 Lua | 📅 2015-12-16 — LuaJIT FFI bindings to libmagic, magic number recognition library - tries to determine file types
* [lua-resty-tsort](https://github.com/bungle/lua-resty-tsort) ⭐ 12 | 🐛 1 | 🌐 Lua | 📅 2016-04-07 — Performs a topological sort on input data
* [lua-resty-maxminddb](https://github.com/lilien1010/lua-resty-maxminddb) ⭐ 12 | 🐛 2 | 🌐 Lua | 📅 2020-08-06 by [@lilien1010](https://github.com/lilien1010) — LuaJIT FFI Bindings to official libmaxminddb, to get ip location with ip database offered by maxmind
* [lua-resty-postal](https://github.com/bungle/lua-resty-postal) ⭐ 10 | 🐛 0 | 🌐 Lua | 📅 2016-02-25 — LuaJIT FFI Bindings to libpostal – a fast statistical parser/normalizer for street addresses around the world.
* [lua-resty-taglib](https://github.com/bungle/lua-resty-taglib) ⭐ 5 | 🐛 0 | 🌐 Lua | 📅 2015-12-16 — LuaJIT FFI bindings for TagLib - An Audio Meta-Data Library
* [lua-resty-unique-id](https://github.com/hqzxzb/lua-resty-unique-id) ⭐ 5 | 🐛 0 | 🌐 Lua | 📅 2018-04-16 — Lua library for generating a unique ID for OpenResty
* [lua-resty-worker-manager](https://github.com/Kong/lua-resty-worker-manager) ⭐ 4 | 🐛 0 | 🌐 Perl | 📅 2021-09-15 — Tracks worker processes and nodes starting / restarting / reloading / stopping
* [lua-resty-hyperloglog](https://github.com/vislee/lua-resty-hyperloglog) ⭐ 4 | 🐛 0 | 🌐 Lua | 📅 2021-06-05 - hyperloglog for openresty.
* [lua-resty-batch](https://github.com/starius/lua-resty-batch) ⭐ 3 | 🐛 0 | 🌐 Perl | 📅 2016-03-31 — Merge multiple requests in nginx to a single sub-request
* [lua-jsonschema-mocker](https://github.com/vm-001/lua-jsonschema-mocker) ⭐ 3 | 🐛 0 | 🌐 Lua | 📅 2023-12-08 - JSON Schema mocker.
* [NetStorageKit-Lua](https://github.com/rainingmaster/NetStorageKit-Lua) ⭐ 0 | 🐛 0 | 🌐 Lua | 📅 2020-02-05 — Akamai Netstorage (File/Object Store) API for Openresty
* [lua-resty-exec](https://github.com/jprjr/lua-resty-exec) — Non-blocking, non-shell-spawning, streaming and non-streaming subprocess library (using [sockexec](https://github.com/jprjr/sockexec))

#### Date and Time

These libraries are not build to using `lua-nginx-module`s date time functions (except luatz) like [`ngx.today`](https://github.com/openresty/lua-nginx-module#ngxtoday) ⭐ 11,787 | 🐛 392 | 🌐 C | 📅 2026-08-14, [`ngx.time`](https://github.com/openresty/lua-nginx-module#ngxtime) ⭐ 11,787 | 🐛 392 | 🌐 C | 📅 2026-08-14, [`ngx.now`](https://github.com/openresty/lua-nginx-module#ngxnow) ⭐ 11,787 | 🐛 392 | 🌐 C | 📅 2026-08-14, [`ngx.localtime`](https://github.com/openresty/lua-nginx-module#ngxlocaltime) ⭐ 11,787 | 🐛 392 | 🌐 C | 📅 2026-08-14, or [`ngx.utctime`](https://github.com/openresty/lua-nginx-module#ngxutctime) ⭐ 11,787 | 🐛 392 | 🌐 C | 📅 2026-08-14, but they may still come handy. At some point we may need a more "official" time library for OpenResty.

* [LuaDate](https://github.com/Tieske/date) ⭐ 275 | 🐛 1 | 🌐 Lua | 📅 2026-02-17 — Lua Date and Time module for Lua 5.x
* [luatz](https://github.com/daurnimator/luatz) ⭐ 140 | 🐛 4 | 🌐 Lua | 📅 2025-10-19 — A Lua library for time and date manipulation (has a fallback to `ngx.now`)
* [SciLua Time Library](http://scilua.org/time.html) — Library for the manipulation of dates and periods according to the Gregorian calendar, i.e. the internationally accepted calendar for most uses

#### Compression

* [lua-resty-zstd](https://github.com/sjnam/lua-resty-zstd) ⚠️ Archived —  LuaJIT bindings to Facebook Zstandard using FFI
* [lua-resty-snappy](https://github.com/bungle/lua-resty-snappy) ⭐ 21 | 🐛 1 | 🌐 Lua | 📅 2015-12-16 — LuaJIT FFI bindings for Snappy, a fast compressor/decompressor
* [lua-resty-brotli](https://github.com/sjnam/lua-resty-brotli) ⚠️ Archived — LuaJIT FFI bindings for Google Brotli
* [lua-resty-zip](https://github.com/doujiang24/lua-resty-zip) ⭐ 11 | 🐛 0 | 🌐 Lua | 📅 2019-08-12 — ZIP functions(compress/uncompress) for LuaJIT

#### Text Formats

* [lua-resty-json](https://github.com/cloudflare/lua-resty-json) ⭐ 178 | 🐛 4 | 🌐 C | 📅 2026-04-24 — JSON library for Lua and C (decoder only).
* [lua-aho-corasick](https://github.com/cloudflare/lua-aho-corasick) ⚠️ Archived — C++ and Lua Implementation of the Aho-Corasick (AC) string matching algorithm
* [lua-gumbo](https://github.com/craigbarnes/lua-gumbo) ⭐ 137 | 🐛 0 | 🌐 C | 📅 2024-08-20 — Lua bindings for the Gumbo HTML5 parsing library, with a set of DOM APIs implemented in pure Lua
* [jsonschema](https://github.com/api7/jsonschema) ⭐ 136 | 🐛 21 | 🌐 Lua | 📅 2026-04-29 — JSON schema validator
* [lua-resty-libcjson](https://github.com/bungle/lua-resty-libcjson) ⭐ 53 | 🐛 2 | 🌐 Lua | 📅 2016-11-25 — LuaJIT FFI-based cJSON library for OpenResty
* [lua-resty-ini](https://github.com/doujiang24/lua-resty-ini) ⭐ 49 | 🐛 1 | 🌐 Lua | 📅 2020-06-10 —  Lua INI-file parser
* [lua-re2](https://github.com/cloudflare/lua-re2) ⚠️ Archived — C and Lua wrapper for RE2 regular expression library.
* [lua-resty-prettycjson](https://github.com/bungle/lua-resty-prettycjson) ⭐ 34 | 🐛 1 | 🌐 Lua | 📅 2020-09-01 — Lua cJSON Pretty Formatter
* [lua-resty-hoedown](https://github.com/bungle/lua-resty-hoedown) ⭐ 26 | 🐛 1 | 🌐 Lua | 📅 2015-12-16 — LuaJIT FFI bindings to Hoedown, a standards compliant, fast, secure markdown processing library in C
* [lua-resty-sass](https://github.com/bungle/lua-resty-sass) ⭐ 10 | 🐛 4 | 🌐 Lua | 📅 2017-02-17 — LuaJIT FFI bindings for libsass - A C/C++ implementation of a Sass compiler (<http://libsass.org/>)
* [lua-resty-jsonschema](https://github.com/tianchaijz/lua-resty-jsonschema) ⭐ 10 | 🐛 0 | 🌐 Lua | 📅 2020-03-26 — <https://github.com/tianchaijz/lua-resty-jsonschema> ⭐ 10 | 🐛 0 | 🌐 Lua | 📅 2020-03-26
* [lua-resty-unistring](https://github.com/bungle/lua-resty-unistring) ⭐ 7 | 🐛 1 | 🌐 Lua | 📅 2015-12-16 — LuaJIT FFI bindings for GNU libunistring - A Unicode string manipulation lIbrary (<https://www.gnu.org/software/libunistring/>)
* [lua-resty-htmlentities](https://github.com/detailyang/lua-resty-htmlentities) ⭐ 7 | 🐛 0 | 🌐 C | 📅 2017-02-24 — Backport the entities to LuaJIT with the FFI binding as the entities to UTF-8 decoder
* [lua-resty-lanli](https://github.com/bungle/lua-resty-lanli) ⭐ 5 | 🐛 0 | 🌐 Lua | 📅 2015-11-24 — LuaJIT FFI Bindings to Lanli HTML Sanitizer Library
* [lua-resty-utf8rewind](https://github.com/bungle/lua-resty-utf8rewind) ⭐ 4 | 🐛 0 | 🌐 Lua | 📅 2016-05-30 — LuaJIT FFI bindings for utf8rewind - a system library written in C designed to extend the default string handling functions with support for UTF-8 encoded text
* [lua-resty-jsdecode](https://github.com/detailyang/lua-resty-jsdecode) ⭐ 4 | 🐛 0 | 🌐 C | 📅 2017-02-22 — Javascript Escape Notation decoding to UTF-8 bytes
* [lua-resty-breeze](https://github.com/weibreeze/lua-resty-breeze) ⭐ 0 | 🐛 0 | 🌐 Lua | 📅 2020-03-31 — Breeze serialize for Lua and OpenResty
* [lua-laxjson](https://github.com/sjnam/lua-laxjson) - Lua binding to a relaxed streaming JSON parser, [liblaxjson](https://github.com/andrewrk/liblaxjson) ⭐ 33 | 🐛 0 | 🌐 C | 📅 2019-07-04 for LuaJIT using FFI

#### Binary Formats

* [luajit-msgpack-pure](https://github.com/catwell/luajit-msgpack-pure) ⚠️ Archived — MessagePack for LuaJIT (using FFI, no bindings, V4 API)
* [lua-resty-msgpack](https://github.com/chronolaw/lua-resty-msgpack) ⭐ 15 | 🐛 0 | 🌐 Lua | 📅 2018-07-11 — Lua Message Pack for OpenResty

#### Document Formats

* [lua-resty-libxl](https://github.com/bungle/lua-resty-libxl) ⭐ 16 | 🐛 2 | 🌐 Lua | 📅 2015-12-16 — LuaJIT FFI-based LibXL (Excel) library for OpenResty
* [lua-resty-haru](https://github.com/bungle/lua-resty-haru) ⭐ 9 | 🐛 2 | 🌐 Lua | 📅 2023-04-12 — LuaJIT FFI-based libHaru (PDF) library for OpenResty
* [lua-resty-hpdf](https://github.com/tavikukko/lua-resty-hpdf) ⭐ 8 | 🐛 1 | 🌐 Lua | 📅 2014-01-08 — LuaJIT FFI-based libHaru (PDF) library for OpenResty

#### Image Formats

* [magick](https://github.com/leafo/magick) ⭐ 427 | 🐛 29 | 🌐 Lua | 📅 2024-05-17 — Lua Bindings to ImageMagick for LuaJIT using FFI
* [lua-vips](https://github.com/jcupitt/lua-vips) ⭐ 147 | 🐛 7 | 🌐 Lua | 📅 2025-12-11 — LuaJIT binding for libvips
* [Lua IMagick](https://github.com/isage/lua-imagick) ⭐ 79 | 🐛 1 | 🌐 Lua | 📅 2024-07-25 — Lua Pure-C Bindings to ImageMagick
* [lua-resty-imagick](https://github.com/kwanhur/lua-resty-imagick) ⭐ 11 | 🐛 0 | 🌐 Lua | 📅 2018-04-20 — Lua bindings to ImageMagick's MagicWand for LuaJIT using FFI
* [giflib](https://github.com/leafo/giflib) ⭐ 6 | 🐛 3 | 🌐 MoonScript | 📅 2021-02-08 — Lua bindings to GIFLIB for LuaJIT using FFI
* [fi-luajit](https://github.com/nyfair/fi-luajit) ⭐ 3 | 🐛 1 | 🌐 Lua | 📅 2016-08-03 — A LuaJIT interface to FreeImage

#### Localization

* [lua-resty-gettext](https://github.com/bungle/lua-resty-gettext) ⭐ 9 | 🐛 0 | 🌐 Lua | 📅 2015-12-16 — LuaJIT FFI-based gettext library for OpenResty

#### Caching

* [lua-resty-lrucache](https://github.com/openresty/lua-resty-lrucache) ⭐ 460 | 🐛 15 | 🌐 Lua | 📅 2026-07-17 — Lua-land LRU Cache based on LuaJIT FFI
* [Ledge](https://github.com/pintsized/ledge) ⭐ 458 | 🐛 16 | 🌐 Lua | 📅 2021-05-07 — A Lua application for OpenResty, providing HTTP cache functionality for Nginx, using Redis as a cache / metadata store
* [lua-resty-mlcache](https://github.com/thibaultcha/lua-resty-mlcache) ⭐ 421 | 🐛 8 | 🌐 Perl | 📅 2024-02-09 — Modern and flexible multi-level caching using lua-resty-lrucache, shared dictionaries, and cache stampede protection.
* [shcache](https://github.com/mtourne/ngx.shcache) ⭐ 59 | 🐛 3 | 🌐 Lua | 📅 2016-05-11 — shcache is an attempt at using ngx.shared.DICT with a caching state machine layed on top
* [lua-resty-cache](https://github.com/lloydzhou/lua-resty-cache) ⭐ 56 | 🐛 3 | 🌐 Lua | 📅 2015-11-22 — HTTP Cache to Redis, can serve stale response, and using `lua-resty-lock` only allow one request to populate a new cache
* [lua-resty-tlc](https://github.com/hamishforbes/lua-resty-tlc) ⭐ 19 | 🐛 1 | 🌐 Perl | 📅 2017-04-19 — Two Layer Cache implementation using lua-resty-lrucache and shared dictionaries.

#### Metrics and Statistics

* [ngxtop](https://github.com/lebinh/ngxtop) ⭐ 6,525 | 🐛 62 | 🌐 Python | 📅 2026-03-02 — Real-Time metrics for nginx server
* [lua-resty-moesif](https://github.com/Moesif/lua-resty-moesif) ⭐ 3 | 🐛 0 | 🌐 Lua | 📅 2025-01-21 — Lua Client Library for Moesif, compatible with OpenResty
* [LUAMETER](https://luameter.com/) — A Lua module for Nginx that records and provides key status and performance metrics, right from within Nginx and in real-time (Proprietary)

#### Logging

* [lua-resty-logger-socket](https://github.com/cloudflare/lua-resty-logger-socket) ⭐ 494 | 🐛 36 | 🌐 Raku | 📅 2026-04-24 — Raw-socket-based Logger Library for Nginx (based on ngx\_lua)
* [raven-lua](https://github.com/cloudflare/raven-lua) ⭐ 120 | 🐛 21 | 🌐 Lua | 📅 2026-04-24 — A small Lua interface to Sentry that also has a helpful wrapper function call() that takes any arbitrary Lua function (with arguments) and executes it, traps any errors and reports it automatically to Sentry
* [lua-resty-logger](https://github.com/kedyyan/lua-resty-logger) ⭐ 13 | 🐛 1 | 🌐 Lua | 📅 2013-01-26 — Custom Logger Library for OpenResty
* [lua-nginx-logging](https://github.com/Lumate/lua-nginx-logging) ⭐ 12 | 🐛 0 | 🌐 Lua | 📅 2014-10-13 — Logging utilities for Nginx written in Lua
* [lua-resty-rfc5424](https://github.com/detailyang/lua-resty-rfc5424) ⭐ 8 | 🐛 0 | 🌐 Lua | 📅 2016-12-03 — An implementation of the RFC5424(syslog) in the OpenResty
* [lua-resty-fluentd](https://github.com/msempere/lua-resty-fluentd) ⭐ 3 | 🐛 0 | 🌐 Lua | 📅 2016-09-17 — Lua fluentd logger for the ngx\_lua based on the cosocket API
* [lua-resty-fluent-logger](https://github.com/mediba-system/lua-resty-fluent-logger) — A structured logger for Fluentd (OpenResty / ngx\_lua)

#### Functional Programming

* [Lua Fun](https://github.com/rtsisyk/luafun) ⭐ 2,260 | 🐛 46 | 🌐 Lua | 📅 2025-04-15 — Lua Fun is a high-performance functional programming library for Lua designed with LuaJIT's trace compiler in mind
* [Penlight](https://github.com/stevedonovan/Penlight) ⭐ 2,124 | 🐛 44 | 🌐 Lua | 📅 2026-08-15 — Penlight brings together a set of generally useful pure Lua modules, focusing on input data handling (such as reading configuration files), functional programming (such as map, reduce, placeholder expressions, etc), and OS path management
* [Moses](https://github.com/Yonaba/Moses) ⭐ 655 | 🐛 5 | 🌐 Lua | 📅 2019-12-18 — A Lua utility-belt library for functional programming. It complements the built-in Lua table library, making easier operations on arrays, lists, collections
* [Underscore.lua](https://github.com/mirven/underscore.lua) ⭐ 403 | 🐛 15 | 🌐 Lua | 📅 2016-03-22 — Underscore.lua is a Lua library that provides a set of utility functions for dealing with iterators, arrays, tables, and functions
* [Lodash.lua](https://github.com/axmat/lodash.lua) ⭐ 67 | 🐛 4 | 🌐 Lua | 📅 2022-12-02 — A functional programming library for Lua in respect to the Javascript library Lodash
* [Search for more "Functional Lua" projects on GitHub...](https://github.com/search?l=Lua\&o=desc\&q=lua+functional\&s=stars\&type=Repositories\&utf8=%E2%9C%93)

#### Web APIs

* [api-gateway-aws](https://github.com/adobe-apiplatform/api-gateway-aws) ⭐ 172 | 🐛 14 | 🌐 Lua | 📅 2021-03-23 — Lua module for AWS APIs. The missing AWS SDK from Nginx / OpenResty. Use it to proxy AWS APIs in a simple fashion, with any HTTP Client that you prefer.
* [lua-payments](https://github.com/leafo/lua-payments) ⭐ 70 | 🐛 1 | 🌐 MoonScript | 📅 2026-07-13 — Bindings to various payment provider APIs for use in Lua (with OpenResty or anything that supports LuaSocket)
* [lua-resty-17mon](https://github.com/icowan/lua-resty-17mon) ⭐ 55 | 🐛 0 | 🌐 Lua | 📅 2016-10-22 — ipip.net IP for OpenResty
* [lua-resty-s3](https://github.com/jamesmarlowe/lua-resty-s3) ⭐ 41 | 🐛 2 | 🌐 Lua | 📅 2015-04-22 — Lua driver for uploading content to Amazon S3
* [lua-resty-aws](https://github.com/Kong/lua-resty-aws) ⭐ 35 | 🐛 10 | 🌐 Lua | 📅 2026-01-27 — AWS SDK for OpenResty
* [lua-resty-aws-auth](https://github.com/paragasu/lua-resty-aws-auth) ⭐ 29 | 🐛 1 | 🌐 Lua | 📅 2024-09-27 — Simple Lua resty utilities to generate Amazon v4 authorization and signature headers
* [lua-mailgun](https://github.com/leafo/lua-mailgun) ⭐ 25 | 🐛 2 | 🌐 MoonScript | 📅 2022-04-08 — A Lua library for sending emails and interacting with the Mailgun API. Compatible with OpenResty via Lapis HTTP API, or any other Lua script via LuaSocket.
* [lua-resty-aws-sdk](https://github.com/kiddkai/lua-resty-aws-sdk) ⭐ 15 | 🐛 0 | 🌐 Lua | 📅 2016-12-01 — A raw AWS SDK generated from API specification
* [lua-resty-upyun](https://github.com/aCayF/lua-resty-upyun) ⭐ 15 | 🐛 0 | 🌐 Lua | 📅 2014-06-16 — Upyun cloud-based platform
* [lua-resty-newrelic](https://github.com/saks/lua-resty-newrelic) ⭐ 13 | 🐛 2 | 🌐 Lua | 📅 2021-04-12 — Lua newrelic SDK for the ngx\_lua based on the C SDK
* [lua-resty-s3uploader](https://github.com/lilien1010/lua-resty-s3uploader) ⭐ 12 | 🐛 0 | 🌐 Lua | 📅 2016-10-01 — An AWS S3 upload client，easy to use
* [lua-resty-tencent-cos-signature](https://github.com/mashirozx/lua-resty-tencent-cos-signature) ⭐ 9 | 🐛 1 | 🌐 Lua | 📅 2021-02-02 Tencent QCloud COS request signature authorization headers generator
* [lua-resty-paypal](https://github.com/Chewbye/lua-resty-paypal) ⭐ 8 | 🐛 0 | 🌐 Lua | 📅 2014-11-08 — Lua Paypal client using express checkout for OpenResty
* [lua-resty-github](https://github.com/jamesmarlowe/lua-resty-github) ⭐ 5 | 🐛 0 | 🌐 Lua | 📅 2014-10-23 — Lua library for using the github api in the ngx\_lua nginx module
* [lua-resty-aws-email](https://github.com/paragasu/lua-resty-aws-email) ⭐ 4 | 🐛 0 | 🌐 Lua | 📅 2019-06-12 — Send email using Amazon Simple Email Service(SES) API
* [lua-resty-hipchat](https://github.com/jamesmarlowe/lua-resty-hipchat) ⭐ 3 | 🐛 0 | 🌐 Lua | 📅 2014-08-14 — Lua library for using the hipchat api

#### Security

* [Nginx-Lua-Anti-DDoS](https://github.com/C0nw0nk/Nginx-Lua-Anti-DDoS) ⭐ 1,625 | 🐛 0 | 🌐 Lua | 📅 2026-08-19) — A Anti-DDoS script to protect Nginx web servers using Lua with a Javascript based authentication puzzle inspired by Cloudflare
* [lua-resty-ddos](https://github.com/satrobit/lua-resty-ddos) ⭐ 17 | 🐛 0 | 🌐 Lua | 📅 2020-03-11 — This library uses Cookie Validation to detect bots from real users

#### Other Sources for Libraries

* [OpenResty Package Manager Repository](https://opm.openresty.org/)
* [LuaRocks Repository](https://luarocks.org/) ([Search for *resty* libraries in LuaRocks](https://luarocks.org/search?q=resty\&non_root=on))
* [Github Search for lua-resty-\* Libraries](https://github.com/search?o=desc\&q=lua-resty+in%3Aname\&ref=searchresults\&s=stars\&type=Repositories\&utf8=%E2%9C%93), or [the recently updated ones](https://github.com/search?o=desc\&q=lua-resty+in%3Aname\&ref=searchresults\&s=updated\&type=Repositories\&utf8=%E2%9C%93)
* [Lua Toolbox](https://lua-toolbox.com/)
* [luapower — Lua, JIT, batteries](https://luapower.com/)
* [List of Available LuaJIT Packages](http://wiki.luajit.org/FFI-Native-Libraries)
* [List of Available LuaJIT FFI Bindings](http://wiki.luajit.org/FFI-Bindings)

## Books and Tutorials

#### Books

* [Programming OpenResty](https://www.gitbook.com/book/openresty/programming-openresty/details) — Scripting an NGINX-based Web Platform (Work-in-Progress)
* [OpenResty Best Practices](https://github.com/moonbingbing/openresty-best-practices) ⭐ 3,608 | 🐛 38 | 🌐 Lua | 📅 2024-06-13 ([GitBook](https://www.gitbook.com/book/moonbingbing/openresty-best-practices/details)) (Chinese, use e.g. Google Translate)

#### Tutorials and Guides

* [agentzh's Nginx Tutorials](http://openresty.org/download/agentzh-nginx-tutorials-en.html)
* [Definitely an OpenResty Guide](http://www.staticshin.com/programming/definitely-an-open-resty-guide/)
* [Top ten things about OpenResty](http://www.staticshin.com/top-tens/things-about-openresty.html)
* The Latest and Greatest from ngx\_lua: New Features & Tools ([Summary](https://nginx.busyconf.com/activities/53d854c1c9e255cf2d00007b), [Slides](http://agentzh.org/misc/slides/nginx-conf-2014/#1), [PDF](http://agentzh.org/misc/slides/nginx-conf-2014.pdf), [Video](https://www.youtube.com/watch?v=Z0fQabvVhIk))
* [Nginx Configuration Snippets](https://github.com/lebinh/nginx-conf) ⭐ 2,116 | 🐛 2 | 📅 2017-10-13 — A collection of useful Nginx configuration snippets

## Videos

* [Getting started with Lapis, the web framework](https://www.youtube.com/watch?v=Eo67iTY1Yf8)
* [Building an HTTP request router with NGINX and Lua - Shopify](https://www.youtube.com/watch?v=Cw6Ci9AF23k) (Nginx Conf 2015)
* [Enabling TLS Cross host Session Resumption with Forward Secrecy via ngx lua](https://www.youtube.com/watch?v=JDNJTkDCH0c) (Nginx Conf 2015)
* [The Latest and Greatest from ngx\_lua: New Features & Tools](https://www.youtube.com/watch?v=Z0fQabvVhIk) (Nginx Conf 2014)

## Conferences, Workshops and Events

* [OpenResty Con 2016, Shenzen, China](http://con.openresty.org/cn/2016/)
  * New Development of OpenResty in 2016 ([Slides](http://openresty.org/slides/New-development-of-OpenResty-in-2016.pdf), [Video in Chinese](https://youtu.be/H5UFGDaf9Xk))
* [Lua Workshop 2016, San Francisco, USA](http://www.luasf2016.org/) ([Lua.org](https://www.lua.org/wshop16.html))
  * Writing Optimal Lua Code for LuaJIT and OpenResty ([Slides](https://www.lua.org/wshop16/Zhang.pdf), [Video](https://www.youtube.com/watch?v=FfhEdF40nhQ))
* [Bay Area OpenResty Meetup 2016 / 3](http://www.meetup.com/Bay-Area-OpenResty-Meetup/)
  * adobe.io ([Slides](http://openresty.org/slides/adobe-io-openresty-meetup.pdf), [Video](https://www.youtube.com/watch?v=EsLO4aE4TWQ))
  * KONG ([Slides](https://openresty.org/slides/kong_openresty_slides.pdf), [Video](https://www.youtube.com/watch?v=QubcdsDsq_k))
  * What's new in OpenResty for 2016 ([Slides](https://openresty.org/slides/Whats-new-in-OpenResty-for-2016.pdf), [Video](https://www.youtube.com/watch?v=fUGXEkdiqmk))
* [OpenResty Con 2015, Beijing, China](http://www.iresty.com/)
  * The Past, Present, and Future of OpenResty 2015 ([Slides](http://www.iresty.com/download/ebook/2015_con/zhangyichun.pdf), [Video](https://www.youtube.com/watch?v=vUgTHeXM5m8)) (In Chinese)
  * Developing OpenResty Framework ([Slides](http://www.slideshare.net/AapoTalvensaari1/developing-openresty-framework-57404012), [Video](https://www.youtube.com/watch?v=VqBt5icKCI8))
  * Be a Microservice Hero ([Slides](http://www.iresty.com/download/ebook/2015_con/zhangshuai.pdf), [Video](https://www.youtube.com/watch?v=gqRMX8BQD98)) (In Chinese)

## Demo Applications

* [Chat Application presented at OpenResty Conference 2015](https://github.com/bungle/iresty) ⭐ 50 | 🐛 0 | 🌐 JavaScript | 📅 2016-06-15 by [@bungle](https://github.com/bungle)

## See Also

* [awesome-lua](https://github.com/LewisJEllis/awesome-lua) ⭐ 4,554 | 🐛 47 | 📅 2024-08-11 by [@LewisJEllis](https://github.com/LewisJEllis)
* [A collection of resources covering Nginx, Nginx + Lua, OpenResty and Tengine](https://github.com/fcambus/nginx-resources) ⭐ 3,803 | 🐛 0 | 📅 2026-08-04
* [awesome-lua](https://github.com/forhappy/awesome-lua) ⭐ 410 | 🐛 4 | 📅 2024-06-11 by [@forhappy](https://github.com/forhappy)
* [Where Lua is Used](https://sites.google.com/site/marbux/home/where-lua-is-used) and [Lua Uses](http://lua-users.org/wiki/LuaUses)

***

> _Enhansomed by [enhansome](https://github.com/enhansome) on 2026-08-19._
