# Project 7 - WordPress Pentesting

Time spent: **6** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: Authenticated Cross-Site Scripting (XSS) in post/page (text editor mode). Editor user and up.
    - Vulnerability types: Stored XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [ ] GIF Walkthrough: ![](https://github.com/cboyd0319/cpw7/blob/master/gifs/CVE-2015-5622.gif)
  - [ ] Steps to recreate: An Editor user or above creates a post with the exploit link in text (not WYSIWYG) mode.
  - [ ] Affected source code: https://core.trac.wordpress.org/changeset/33359
    - [NVD](https://nvd.nist.gov/vuln/detail/CVE-2015-5622)
    - [WPVulnDB](https://wpvulndb.com/vulnerabilities/8111)

2. (Required) Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: Publish Post & Mark as Sticky Permission Issue
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.3.1
  - [ ] GIF Walkthrough: ![](https://github.com/cboyd0319/cpw7/blob/master/gifs/CVE-2015-5715.gif)
  - [ ] Steps to recreate: Similar to the isue above. An Editor user or above creates a post with the exploit link in text (not WYSIWYG) mode.
  - [ ] Affected source code: https://github.com/WordPress/WordPress/commit/9c57f3a4291f2311ae05f22c10eedeb0f69337ab
    - [Debian.org](https://security-tracker.debian.org/tracker/CVE-2015-5715)
    - [WPVulnDB](https://wpvulndb.com/vulnerabilities/8188)

3. (Required) Internal GET SSRF via CSRF with Press This scan feature
  - [ ] Summary: Wordpress installations can send unwanted scrape/scan requests on behalf of their user invoked by the attacker. Including private connections via 0.0.0.0
    - Vulnerability types: SSRF
    - Tested in version: 4.2
    - Fixed in version: 4.4.1
  - [ ] GIF Walkthrough: ![](https://github.com/cboyd0319/cpw7/blob/master/gifs/SSRF.gif)
  - [ ] Steps to recreate: Phishing link to logged in admin
  - [ ] Affected source code: http://wpdistillery.vm/wp-admin/press-this.php?u=URL&url-scan-submit=Scan
    - [HackerOne](https://hackerone.com/reports/110801)

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)
- [Kali Linux](https://www.kali.org/)
- [WPScan](https://wpscan.org/)
- [WPVulnDB](https://wpvulndb.com)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright 2018 Chad Boyd

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
