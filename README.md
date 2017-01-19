# inspec-metaprofile

This profile scans Windows and Linux nodes with either the base-os-hardening tests:
Tests:  https://github.com/dev-sec/tests-os-hardening
Fix:    https://github.com/dev-sec/chef-os-hardening
Or the windows profile:
Tests:  https://github.com/dev-sec/windows-hardening-benchmark
Fix:    https://github.com/dev-sec/chef-windows-hardening

There is a skip for two of the tests to illistrate how to skip tests (and these tests don't currently pass when 'chef-windows-hardening' is applied).


Audit block of base role (base.json)
"audit": {
  "collector": ["chef-server-visibility"],
  "owner": "automate-org",
  "insecure": true,
  "fail_if_not_present": true,
  "profiles": [
    {
      "name": "meta-profile",
      "git": "https://github.com/yrros/inspec-metaprofile"
    }
  ]
} 
